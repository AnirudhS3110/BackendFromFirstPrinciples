# HTTP Caching:
- Method to Copies of RESPONSES for Re-Use , reducing the need to Keep on requesting to server which inturn reduces Load time, User Bandwidth and Reduces Server Load and Better User Experience.
- browser caches based on the HTTP Headers from the Servers.
- We control Cache by:

| Header          | Purpose                                    |
| --------------- | ------------------------------------------ |
| `Cache-Control` | How long to cache + caching rules          |
| `Expires`       | Old legacy way (use Cache-Control instead) |
| `ETag`          | “Is this file changed?”                    |
| `Last-Modified` | “When was this changed?”                   |

## How Caching Works under the Hood:
- For every Cached Response there will be ETag associated with it, which is genrated by Hashing the Contents of the Response given by the Server 
- Now after Recieving the ETag, the Client browser stores it for the Request
- Now when the Client Wants the Same Resource, it sends request to the server along with the ETag in the ``If-None-Match`` header field, the server responds with Code 304 that is Resource not modified, which implies teh cached resource is still valid
- Now the Client will use the Cached Response.

## Note:
- nowadays we have React Query, which is Client Side Caching, it gives more power to Developers in terms of caching the responses.
- It 
- much bettter option than HTTP Caching

## Types of Caching:
### 1) Strong Caching (Browser MUST cache):
- Tells the browser to Cache for X amount of time and the client should not request for this resource for X mins.
- used to Store Static Files like CSS, Logos, fonts, Static JS, Images
- Code Example(Cache static files (images, CSS, JS) for 1 year):
```js
app.use("/static", express.static("public", {
  maxAge: "1y",       // cache duration
  etag: true,         // enable etags (default true)
  lastModified: true  // enable last-modified
}));
```
- this is represented in Dev Tools tab like:
```yaml
Cache-Control: public, max-age=31536000, immutable
ETag: "abcd1234"
Last-Modified: Mon, 15 Jan 2025 10:00:00 GMT
```


### 2) Short Caching:
- For responses from API or Dynamic Pages.
- Exmple: Caching APO respose for 60 s:
```js
app.get("/products",(req,res)=>{
    res.set("Cache-Control","public, max-age=60");
    res.josn({msg:"cached for 1 minute"})
})
```
- This code caches the response in the browser for 60s
- If client tries to hits the server, it take the value directly from the cached response in the broswer
- after 60s when the client send req, it is sent to the server.

### 3) No Cache
- used in login/signup pages, JWT response, Sensitive data.

```js
app.post("profile",(req,res)=>{
    res.set("Cache-Control","no-store");
    res.json({user: "usr1"});
})
```

| Mode       | Meaning                            |
| ---------- | ---------------------------------- |
| `no-cache` | Browser MUST revalidate every time |
| `no-store` | Do NOT cache at all                |


## <a href="../4) Response Codes/readme.md">Previous: Response Codes</a>
## <a href="../6) Content Negotiation/readme.md">Next: Content negotiation</a>



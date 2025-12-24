# Types of Request:
## 1) Simple Request

## 2) Preflighted Request:
- most of the requests are considered as Preflighted Request
- It consists of Options Method.
- example: <br>
![alt text](image.png)
#### Conditions for a requested to be Preflighted Request :
- 1) The Request must be Cross Origin
- 2) One of the three:
- - 1) It must be Either **PUT or DELETE** Request, should not be GET, POST or HEAD
- - 2) The request content type should be other than: application/ , multipart/form-data or text/plain
- - 3) the Request should have Non simple headers like: Authorization, Custom Header.


- Each server has ```Access-Control-Allow-Orgins``` which is list of allowed Origins from which The server Accepts Request. If the Request is from the Domain/origin which is not specified in the  ```Access-Control-Allow-Orgins```, then Server declines the request and in the client side it shows CORS(Cross Origin Resource Sharinf) error
- We can also assign ```Access-Control-Allow-Methods```  and ```Access-Control-Allow-Headers```
- ```Access-Control-Allow-Headers``` this implies the types of headers allowed, example Content-Type, Authorization
## <a href="../2) HTTP Methods/readme.md"> Previous </a>
## <a href="../4) Response Codes/readme.md">Next: Response Codes</a>

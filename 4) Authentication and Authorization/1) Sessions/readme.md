# Sessions:
## Need for Stateful Interactions:
- Intially Web mostly had Static pages, therefore the web could Manage with jsut HTTP's stateless property
- But soon, many pages began to have Dynamic Content , now teh Statelessness of HTTP became a bottleneck
- For example, websites like E Commerce websites, need to remember what are Items in YIUR cart. and How cld user Remain LOGGED IN while navigating bewtween the pages
- This led to the Beginning of Statedful interactions in Web, which HTTP was not
- This Led to the Concept of SESSION

## Session:
- Session Provided a way to Establish  **Server Side Context** in the browser for each user
- Whenever teh user logged in , the Server Created a Session ID which was stored along with teh metadata of the user in a **persistent store**, which can be a DB or Redis.
### How Sessions Worked:
- The Session ID was Sent to the Client as a cookie and all the Requests made by the Cient needs to have the cookie as it has the Session ID, 
- This Session ID enabled the Server to have some kind of memory for the user.
- These Sessions were Short Lived, like 15 mins
- Initally Session iNformations were stored as FILES in Server, but resulted in Scalability Issues
- This led to use of DBs to store Session Information, which gave persistent look ups across SERVER RESTARTS.
#### In the Distributed Storage Era
- Session Infos were Stored in Redis/Memcache, as in memory looks ups are faster than DB look ups
## <a href= "../readme.md">Prev: History of auth</a>
## <a href="../2) JWTs/readme.md">Next: JWT</a>
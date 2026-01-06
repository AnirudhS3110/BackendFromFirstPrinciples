## 1) Security:
- We have CORS middleware, Security Headers middlware, Authentication Middleware and Rate Limitting Middleware.
- ``` CORS``` is the first middleware to be Executed for any request
- The CORS checkws whether the Request is from the Allowed Domain, if yes, it adds some header to it and Passes to the next middleware.
- IN authentication Middleware, we first authenticate the user, if failed, the middleware sends Response to the Client with Status code 401.
- If the User is Authenticated, then we extract the UserID, the USerRole and add these info about the user to the ```Request Context```.and foward it to the next Middleware.
- Rate Limmitting is done to avoid High number of request from the Same IP address within short period of time, We can set the PEriod of time and the max Number of Requests. Error code is 429

## 2) Logging and Monitoring
- Everytime we get a Request , we can log in our server saying at this time we got request to this end-point.
- It helps us to Debug and report
- We can extract infos like what is the ROute, what is the Request method, What is the Query parameter.

## 3) GLobal Error Handling:
- This middleware gets error from any handler, and we can classify whether the caused error was Client Side or Server Side, based on that we can send a Structured Response, which consist of  {message , code} to the CLient
- It takes Unstructred Error from ANYWHERE FROM THE APP
- Usually we keep Error Handling Middleware at the last.
- This is because Error can happen in any Middleware or Handler, so when kept at last, it can easily catch all the errors and gracefully respond to the client by properly structuring the error.


## 4) Compression MIddleware:
- If we have a LARGE JSON, we can use some Compression Algos like  GZIp, compress the response and send the response back.
- Modern Browsers have the capability to De-Compress the Response back to Format which can be understood by the client
- This happens during Client Deserialization Process.

## 5) Data Parsing:
- The process of Serialzation and Deserialization can be delegated to the middleware so that the handlers dont do the things.


## Order of Executing Middlwares:
- 1) CORS
- 2) Logging Middlewares
- 3) Authentication
- At the End, ```Global Error Handling Middleware```.
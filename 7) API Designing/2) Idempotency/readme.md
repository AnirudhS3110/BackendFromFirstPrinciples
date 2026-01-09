# Idempotency:
- The property of Certain actions where, even after doing the actions many times, has the same effect when it performed once. The Side Effect to the Environment Remains the same
- In Servers Concept,  this means, How much ever times the Client makes calls to the Server, the Outcome/Result of the Server Environment Remains the same.```https://api.example.com```
- GET method is idempotent
- PATCH or PUT method with EXACTLY same payload as with each request, is Idempotent, as there is no change/ side effect is made to the server environment.
- DELETE method with exactly same payload with every request is IDEMPOTENT, bcos fromt eh first request, teh object will be deleted, for teh 2nd req the server wld send back 404 error, but there is NO SIDE EFFECT CAUSED TO THE SERVER ENVIRONMENT, THE ELEMENT STILL DOESNT EXIST, therefore DELETE With same payload is idempotent.
- POST is non-Idempotent, even if we send he same payload, a new instance/resource is created on each request
### NOTE(POST is a Custom Actions):
- Whhenever you want ot performa an operation which cant be put in any of the existing methods, just put it as POST method
- For example there is ```/sendemail``` route, this API endpoint is to send email to particular person, this is not a FETCH operation , but we should use POST.
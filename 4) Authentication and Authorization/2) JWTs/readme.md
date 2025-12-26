# JWT(JSON Web Tokens):
- Came upto use in 2015
- JWTs transfer CLAIMS in STATELESS way between 2 Systems.
- They are self- contained TOkens
![alt text](image.png)
- JWT has 3 parts
- 1) Header part:
- - Has the information about what type of Hashing algo was used to create this JWT token
- 2) PAYLOAD DATA:
- - Has the Data/metadata of user, based on which parameters this JWT token was created
- - SUB field has the info of USer ID
- - iat(Full Form: Issued At) has the info of teh data/tiem in which this JWT was issued
- - name: gives info odf name/role of the 
- 3) Verify Signature:
- - 


- So JWT authentication is Stateless

## Birth of JWTs:
- Its very lightweight and Saves lot of Storage Cost
- At mid 2000's Web Services bcame a Global thing
- 1) Maintaining Sessions caused a bottleneck as, Companies need to store Session Data of Millions of Users
- 2) Replication caused Latency: As intro do multi geographic servers, needed to store and update the User Session data in each one which caused Latency.This also lead to Consistency Challenge(Synchronization Need)
- 3) This lead to birth of JWT, as this divides the problem of Securing State from the Server while maintaing  Security and Integrity

## Pros of using JWT:
- Its statless, so it reduces the Server cost of Saving the Session data
### Scalability:
- In Microserice Architecute, COOKIES issued by one server cant be validated by the Server in Another Domain
- But when the Servers use JWT, all the Servers will have the Secret KEy for making the JWT, using this each server can DECODE teh JWT abnd VERIFY the user's Identity

### Portability:
- It has light weight nature
- has url friendly nature
- Its encoded in base64 string format
- They can be stored Either in Local Storage or cookies or small memory space systems
- Storiing is local Storage is bad practice, should store in cookies instead.

## Cons of using JWT:
### Server Doesnt have power to Disqualify a JWT token:
- They can only do ths by changing the shared SECRET KEY
- But if they change, they need to update the ne JWT token for each user, which is not feasible.

## Best Approach:
- Use Auth Providers.
- In small scale its fine to go with your own Auth Systems
- For medium and Large Scale, please go with Auth Providers like OAuth,Its their headache to deal with Authentication.

## <a href="../2) JWTs/readme.md">Prev: Sessions</a>
## <a href="../3) Cookies/readme.md">next: Cookies </a> 

# Request COntext:
- Every Framework / Library provides some implementation of Request Context.
- Its a Kind of State / Storage / Context which is scoped for a Perticular Request, which is accessible across all the middlewares or Handlers.
- Context is generally a Key -Value pair DS.
- Metadata about the user is stored in the Request COntext.
- Handlers can access these informations, instead of taking authentication info from the payload, we can take from Request Context.
- This is safer because, if we wanna get info from the DB for the user, anyone with the just USER ID can access teh contents if the userID was shared in the Payload.s
- If it was taken through the Request context, which is created as a result of Authentication, we can keep track of who is accessing the data.
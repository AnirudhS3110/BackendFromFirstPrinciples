## Methods:
- This specify the Intent of the Request to the Server
![alt text](image.png)
- GET to get info, without modifying anything on server
- POST write/create data in server, rquest has a Body 
- PATCH to Update Data, it can just **APPEND** the data
- PUT is used to update Data by completely **REPLACING** the Data.
- DELETE is used to Delete the Data.

## Idempotent and Non-Idempotent methods:
- Tdempotent methods are the ,methods t which the Server gives same output for same request irrespective of no. of times. eg: get, put delete
- Non-Idempotent- POST, there are 2 different kinds of Result for Same request, so POST is Non-Idempotent

## OPTIONS method:
- Wont use as a developer, but will see in Developer tab in Browsers
- IT Fetches the Capability of a SERVER for a CROSS ORIGIN Requests


## <a href="../2) HTTP Methods/readme.md">Previous</a>
## <a href="../3) Types of Request/readme.md"> Next: 3. Types of Request and CORS </a>
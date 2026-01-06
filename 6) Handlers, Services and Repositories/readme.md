## Request Life Cycle Inside  Server.
### Handlers/Controllers:
- Requests Coming to a Route in the Server, is handled by specific Functions based on the ```METHOD``` through which the Request is sent.
- Two Objects: Request & Response
#### 1) Deserialization of the Data from Serializable standard to Understandable format by the Server.
- In Node.js backend we done need to do it manuallly, as there are middlewares (JSON.bodyparser) which converts JSON into JavaScript Objects.
- In languages like GO and Python, we have to do this Step Explicitly, we have to Deserialize the JSON
- In GO need to Deserialise into Native_Struct, in Pythonn into Dictionary, Rust into Struct.
- This is called ```BINDING``` the Standard format into native format.
- If the DESERIALIZATION FAILS, WE SEND RESPONSE WITH CODE ```400 Bad Request``` and TERMINATE the request.
- Now the language can make sense of the Data.

#### 2) Data Validation and Transformation Pipeline

#### 3) The Controller Layer makes call to the Service Layer:
- As of now the Data is completely Validated and  Required Transformations are made to the Data so that it can be Easily used by the server.
- Now the Validated and Transformed data is present in Service layer.
- All Actual Process of the API endpoint happens in the Service Layer of the API endpoint/handler
- The service layer MUST NOT DEAL ANYTHING WITH HTTP CALLS, it should handle only the Business logic.
- The function in the servicee layer should be Programmed such that, it's function should not be easily deciphered/understood by the reader
- It Must be in an Isolated Layer, such that it only accepts the data, does all the processing and returns the data, whithotu caring about how the data will be sent to the client or any other HTTP calls.
- It can call the Repository Layer, if it wants to persist any data.
- Can send External API calls.
- It also Orchestrates the Repositoryb layer. 
- i.e it can get different datas from different Repositoy Methods and Merge those Datas to return the required Response to the Handler.

#### 4) Repository Method:
- It takes the data given by Service layer, Constructs necessary queries, retrieves results from the DB and returns the result
- One Repository method should return only one type of response, i.e **it must have one single Responsibility**
- For example: Lets say we have 2 repository methods: one to retrieve all the books in the DB, another for getting a single book
- We should not give a optional Parameter and design the function like it will return BOTH types of the Results, we should have 2 different functions.
### Intro
- The Client Communicate with Server through HTTP requests
- We are gonna understand How client and server makes understands the data which is being transferred between them
- The client can be JS app while the Server can be RUST app
- Lets assume this Client Sends the Request as JSON
- Lets understand how does this server understands the JSON in its own DataTYpes
- NOTE: JS is loosely typed whereas RUST is very strict when it comes to types, it is a Compile language

## What is Serialization Standard?
- Before Sending an Request the client and the Server should Agree upon the Standard Format in which the data should be transferred so that it is understandable by both.
- the data is converted from JS to the standard format and it is sent over the network, when the Server Recieves it, it converts the standard format into format understood by it.
- then it understands the data creates response, then again converts the Response into the STANDARD FORMAT and is again sends it over the internet to the client
- The client Reads and Parses it into JS
- THis standard is called **Serialization Standard**


## Definition
- Serialization and Deserialization involves converting data from one format to Standard format (accepted by the clietn and Server), while transmission so that it is Domain Agnostic or Language Agnostic

## Note: 
- Data Transmission can be done through HTTP ,  Websockets, Grpc
- in this we just see about HTTP

## Types of Serialization Standards:
- 1) Text Based
- 2) Binary format

## Most popular Serialization and Deserialization Standard: **JSON**
## Other Serializaton and Deserialization Standards:
- YAML  
- XML
- JSON, XML,YAML are together called **TEXT BASED SERIALIZATION**

## BINARY FORMAT SERIALIZATION:
- TYpes of Binay Format Serialization:
- - **Protobuff (MOST POPULAR)**(Developed by Google to reduce Serialization adn Deserialization time)
    -  1) It serializes data into a compact binary format, which uses less bandwidth and is faster to parse compared to text-based formats like JSON or XML.
- - aviro



## JSON(JavaScript Object Notation)
- Its is used even to Log files, Send data betweeen  client and Server and lot of otehr use cases
- It is Human Readable
-  KEYS should always be inside doubvle quotes
- The value can be anything, number string, another JSON(Nested JSON), boolean, array
- In terms of OSI model, the data gets converted to bits in PHYSICAL LAYER then in the APPLICATION layer it gets converted back to JSON.

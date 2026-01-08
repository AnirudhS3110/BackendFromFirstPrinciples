# API Designing:
- At the time  where the STATUS CODES were introduced, The Internet was mostly Using Multi-Page Wesbites/WebPages.
- These times we use Single page , and the Routing is performed in Client Side

## History:
- in 1990, Tim Berners Lee The project World Wide Web, was created to share Knowledge to Everyone!.
- This led to creation of the FIRST:
    - the concept of URI.
    - HTTP
    - HTML
    - Web Server
    - Web Browser
    - What You See is What You Get(WYSIWYG)(First HTML Editor built in in the Browser)
- All these things were done in about an year.
- But this  project led to a breakdown due to Exponential Growth of Userbase in it
- They dint do this project keeping in mind of Scaling this
- To Scale the Web, new Techniques, Components had to be Inroduced
- This existing concepts at that time was not enough to scale the Web.
- In 1993, The Co-Founder of APACHE HTTP Server, In  order to make this project Scalable, he proposed certain COnstraints:
    - 1) He proposed Client Server model, this model Creates Seperationm of Concern between the Client and the model.The client handles the User Interface to the users, the Server handles the data storage and the business logic
    - 2) Uniform Interface
    - 3) Layered System: Architecture composed Systems as Layers and each layer can Communicate only to the layer below them, this allows better scalability, security and ability to add Intermediate components like Load balancers, Proxy servers
    - 4) Cache: The serve must label the different responses that whether it should be Cached or not.
    - 5) Statelessness of HTTP req.
    - 6) Code on Demand: Servers can extend Client Functionalit by extending het JS code to the client

## Why REST Architecture?
1) In REST Architecture, the Resources are REPRSENTed by certain FORMAT
2) STATE of the resources is transferred through the predetermined Format
3) TRANSFER of these formatted resources ensures communication between the server and the client.
### 1) Representeational (RE):
- This means that Resources are REPRESENTED in specific Format
- Different Format is Chosen based on the Context.
- If the Resource is shared between Server and Server, then its JSON
- If its between Server and Client its HTML.
- Same Resource can haver Different Representation based on the COntext/ Client Needs.

### 2) State:
- Resource has State, this what defines the value for each property in the JSON or HTML.
- And the State of the Resources can be Transferred through JSON or HTML.

### 3) Transfer:
- The movement of Resource representations between the client and the server.
- Client and Server Communicate with each other through TRANSFER of these resources.

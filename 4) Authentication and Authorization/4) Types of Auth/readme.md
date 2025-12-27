# Types of  Authentication:
### 1) Stateful
### 2) Stateless
### 3) API Key
### 4) OAuth 2.0

## Stateless VS Stateful Auth:
- In case of Stateful Auth, we need to look up Persistent Store(Either Redis/DB), in order to get the information of the Session or the USers.
- In case of Stateless AUth, All the Information regarding the Sesssion/user is provided in the JWT Token itself, which rediuces Unnecassary Storage Calls. It is a **Self-Contained Signed Token**
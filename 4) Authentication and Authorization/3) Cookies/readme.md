# Cookies:
- Using Cookies SERVERS can store some data in Client's Browsers, given:
- - The cookie is used by only  the ISSUED SERVER
- - Therefore the cookie can only be sent to that single Server.

## Flow:
- Client sends req with Usernaem and Password to login
- Server checks and iof Authentication is succcesful , it sets a cookie with AUTHORIZATION TOKEN, it maybe JWT or Session ID and it is stored in CLient's cookies
- In Subsequent reqs, Clients sends the Request along with the Stored cookies, so that it validates the Authenticity of the token and Identify the user ND authorize the user.

<a href="../2) JWTs/readme.md">Prev: JWT</a>

Client <-> Server Comms and data transfering.

Request Components:
-Method: GET, POST, DELETE, PUT, ...
-Data/Uniform Resource Identifier(URI) -> data itself(image, webpage, json, etc..)
-HTTP version: HTTP/1.1 or HTTP/2
-Headers: Provide additional infosabout the request or client. 
-Authentication(Token, can be included in data or headers)
-Body(optional): used when additional data needs to be sent to the server, typically with methods like POST or PUT. the body can contain various types of data, such as form data, JSON, or XML.

Types of Headers:
-General Headers: These headers are present in both request and response msgs, but not related to the data being sent in the body of msg. Ex: Date, Connection, Cache-Control, Transfer-Encoding
-Request headers: Provide more infos about the resource or the desired action to be performed. Some common req headers include Accept, Accept-Language, Host, User-Agent, and Referer. for instance, the Accept header specifies the media types accepted by the client, User-Agent header provides infos about the user agent that initiated the req.
-Response Headers: Provide additional infos about the server's response or about the resource that is being sent. Ex: Server, Content-Type, Content-Length(size), and Set-Cookie.

Purpose of Headers:
-Caching and Optimization: Headers like Cache-Control, Expires, and ETag help in controlling the caching behaviour of resources, which improves the performance of webapps.
-Security: Content-Security-Policy(CSP) and X-Frame-Options help protect against certain types of attacks such as XSS(Cross-Site Scripting) and clickjacking.
-Authentication and authorization: Headers like Authorization are used to pass credentials or tokens for auth purposes.
-Content Negotiation: Headers liek(mudkips) Accept and Content-Type allow the client and server to negotiate the content format that is acceptable for both parties. 

Response Components:
-Status Code: `HTTP/1.1 200 OK` 200 being status code, and OK being status msg.
-Headers: Additional infos about server resp. Ex: details about the server, content being sent, and various instructions for the client. Common response headers: `Server`, `Content-Type`, `Content-Length`, `Set-Cookie`, among others.
-Data: basically the data defined by `Content-Type` header.

Status Codes:
- 1XX - Information
- 2XX - Success
- 3XX - Redirect
- 4XX - Client Error
- 5XX - Server Error

Resources:

https://requests.readthedocs.io/en/latest/ -> Documentation

https://reqres.in/ -> tool for request/response, fake api with fake data for testing

https://httpbin.org/ -> same as above

https://pipedream.com/requestbin -> inspect HTTP requests


Addendum:

/api/users?page=2 : end point

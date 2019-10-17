# Objective
Understand the mechanics of HTTP protocol and commands.
## Instructor Notes


## Required Resources


## I Do
HTTP is the common language of the web. Applications use HTTP to communicate. To frame this topic in terms of our OSI network model, HTTP lives in the application layer. Consequently, HTTP is layered on top of TCP (remember: TCP lives at the transport layer). HTTP uses TCP to transport its message data. IP and Ports fall below these at the Network layer and Data Link layer, respectively. 

On the surface, HTTP is a simple 'request-response' protocol. The client makes a request, and the server responds with an OK message code or an error message code. You might be familiar with the error code: 404, if you've ever seen a message like this: 
![enter image description here](https://lh3.googleusercontent.com/hw7DDpu_ZwSxFNIWDQHGUaIV-2ZAtc-I6hLpnsKyV9qtZsPbAoW5VJuJZ_8zOIUZmSRsQNyvwXj-)

Under the hood, HTTP is using scripting terms - GET, POST, PUT, and DELETE. If you've ever used or studied REST APIs you may  be familiar with these terms, or have maybe even used them in a scripting language like Python or Javascript. Definitions can be found below: 
|Word|Definition  |
|--|--|
| Get | A request for the server to 'get' a specified file or script and return it to client.   |
| Post | Return of the specified file or script sent back to the client.  |
| Put | Updates file or script if there is a discrepancy between the local information and remote information.  |
| Delete | Deletes files or scripts, rarely used. |

With this vocabulary and knowledge of OK/error codes we can inspect the HTTP request-response process at a more detailed level:   
1. Client makes a request using 'GET'. This request includes a startline and headers, but no body.
2. Server responds with an 'OK' (200) message. This response includes a startline, headers, and body. 


Including knowledge of other layers in the process we get a fuller picture of the HTTP process: 



---

### not sure if we need the following: 
Proxies are intermediaries or middlemen between clients and servers. Proxies work to secure data on the client side by filtering blocked content and on the server side to prevent malicious requests. For example, on the client side, a proxy might be set up on a elementary school network to only allow access to educational websites. On the server side, a proxy might be set up to only allow requests from known IP addresses, or with certain credentials. 




## We Do

## You Do



## Additional Resources
- Video: [How Does HTTP Work? ](https://www.youtube.com/watch?v=M_oTNuVNkms)
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTk3NzIwMjk4LC0xNDIxMzI2MTEwLC0xMj
k1MjA5NjIsMTc4MzkzMjc4OSwtNTQzMzE2NDY3LC0xNjYwMjI5
NjI5XX0=
-->
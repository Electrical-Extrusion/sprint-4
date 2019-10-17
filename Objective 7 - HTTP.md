# Objective
Understand the mechanics of HTTP protocol and commands.
## Instructor Notes


## Required Resources


## I Do
HTTP is the common language of the web. Applications use HTTP to communicate, much 

Basic steps in HTTP are as follows. 
1. Client makes a request using 'GET'. This request includes a startline and headers, but no body.
2. Server responds with an 'OK' (200) message. This response includes a startline, headers, and body. 


HTTP lives in the application layer and is thus is layered over TCP, which lives at the transport layer. HTTP *uses* TCP to transport its message data. IP and Ports fall below these at the Network layer and Data Link layer. 

Proxies are intermediaries or middlemen between clients and servers. Proxies work to secure data on the client side by filtering blocked content and on the server side to prevent malicious requests. For example, on the client side, a proxy might be set up on a elementary school network to only allow access to educational websites. On the server side, a proxy might be set up to only allow requests from known IP addresses, or with certain credentials. 




## We Do

## You Do



## Additional Resources
- Video: [How Does HTTP Work? ](https://www.youtube.com/watch?v=M_oTNuVNkms)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc4MzkzMjc4OSwtNTQzMzE2NDY3LC0xNj
YwMjI5NjI5XX0=
-->
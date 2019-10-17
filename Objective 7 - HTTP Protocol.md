# Objective
Understand the mechanics of HTTP protocol and commands.
## Instructor Notes


## Required Resources


## I Do
HTTP is the common language of the web. Applications use HTTP to communicate requests and responses between a user (or client) and a server.

On the surface, HTTP is a simple 'request-response' protocol. The client makes a request, and the server responds We'll add to this later on, but for now think of the steps as follows: 
1. Client request
2. Server response

The server response usually contains an OK message code or an error message code. You might be familiar with the error code: 404, if you've ever seen a message like this: 
![enter image description here](https://lh3.googleusercontent.com/hw7DDpu_ZwSxFNIWDQHGUaIV-2ZAtc-I6hLpnsKyV9qtZsPbAoW5VJuJZ_8zOIUZmSRsQNyvwXj-)
Other important codes include 200 and 202 (OK), 201 (new resource being created), 204 (no content), 301 (moved permanently), 307 (temporary redirect), 400 (bad request), 401 (unauthorized), and 500 (internal server error). For a full list and explanation of these codes, see the "Status Code Definition" reference under additional resources. 

Under the hood, HTTP is using scripting terms - GET, POST, PUT, and DELETE - to comunicate between client and server. If you've ever used or studied REST APIs you may  be familiar with these terms. You have potentially even used them in a scripting language like Python or Javascript. Definitions can be found below: 
|Word|Definition  |
|--|--|
| Get | A request for the server to 'get' a specified file or script and return it to client.   |
| Post | Return of the specified file or script sent back to the client.  |
| Put | Updates file or script if there is a discrepancy between the local information and remote information.  |
| Delete | Deletes files or scripts, rarely used. |

With this vocabulary and knowledge of OK/error codes we can explain the HTTP request-response process at a more detailed level:   
1. Client makes a request using 'GET'. 
2. Server responds with an 'OK' (200) message. 

 To frame this topic in terms of our OSI network model, HTTP lives in the application layer. HTTP is thus layered on top of TCP (remember: TCP lives at the transport layer) and uses TCP to transport its message data. IP and Ports fall below these at the Network layer and Data Link layer, respectively. You can think of the HTTP/TCP relationship like you think of the IP/Port relationship where the latter takes care of details that the former is not conerned with. 

Including knowledge of other layers in the process we get a fuller picture of the HTTP process: 

1. Client makes a request using 'GET'.  That request is transported using TCP/IP protocols to a known port, usually 443 - HTTPS server - and the server looks up the requested URL.
![enter image description here](https://lh3.googleusercontent.com/4SuF0TSYAWp4lF6p3dA6m_UV7otb0C42gmgWWd5ftpQV-3l8i05wmYqhEX5CeHiW__H_s_UfPTQ-)

2. Server returns the requested URL with 'POST' and an 'OK' (200) message. That return is, again, transported through TCP/IP and makes its way through the OSI layers until it reaches the client again. 
![enter image description here](https://lh3.googleusercontent.com/aiVXI9y8RX3y1DBkOwlP9wdUvWzQ4K5x4ktpklnv9bTeNYFDM2LWtA1TU3d48aBGoGSy4KEU2kLK)


---

### not sure if we need the following: 
Proxies are intermediaries or middlemen between clients and servers. Proxies work to secure data on the client side by filtering blocked content and on the server side to prevent malicious requests. For example, on the client side, a proxy might be set up on a elementary school network to only allow access to educational websites. On the server side, a proxy might be set up to only allow requests from known IP addresses, or with certain credentials. 




## We Do
Follow HTTP stream in Wireshark. 

## You Do
Run a packet capture on your own, generate a list of all the URL's accessed in a 60 second period. 



## Additional Resources
- Video: [How Does HTTP Work? ](https://www.youtube.com/watch?v=M_oTNuVNkms)
- Reference: [Status Code Definitions](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk3MjU1MjM1NiwtOTM3NDMwODgwXX0=
-->
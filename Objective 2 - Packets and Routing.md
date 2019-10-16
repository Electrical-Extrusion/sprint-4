# Objective Statement


Understand and explain how packets are constructed and transmitted on a network.

## Instructor Notes


## Required Resources


## I Do
Cybersecurity is concerned with the protection of data. Though they can occur anywhere, breeches most commonly occur when data is moving around from one place to another in the Transport layer of OSI. Data that isn't properly secured or broken up can be easily intercepted by hackers in a process that we'll learn later on. In order to understand what's going on under the hood with packet trannsportation, we need to understand the protocol governing this layer, which is Transmission Control Protocol (TCP). 

In addition, you'll need a strong understanding of the term "packets." In short, a packet is a chunk of data. When a user makes a request to send or receive information, it takes the form of data. In order to move from the client to the server, data must be placed (and sometimes broken apart) into packets. These packets may all take different routes through the world wide web, but eventually end up at the same destination and, when pieced back together, complete the user's request. Scanning through unencrypted packets is one-way hackers can obtain sensitive information: like usernames and passwords. 


**Packet Construction**
When a user sends a request, the TCP on the user end breaks the data into payloads, and labels each with the needed header, creating a multitude of packets. 

Regardless of the type of security, or data included, packets always contain the following three parts. When learning this concept it can be helpful to use an analogy of literal packages, and consider how these find their way through a postal system. 
|Packet Part|Definition| Analogy|
|--|--|--|
| **Header** | The header contains instructions like the sender's IP address, receiver's IP address, Protocol, and Packer number |Front of an envelope - addresses, shipping label or stamp. |
|**Payload** | The payload is where the actual data is stored |The letter inside the envelope.|
| **Trailer**  | The trailer contains data to show that the interpreter has reached the end of the packet, or, throws an error when needed  |Signature at the end of the letter. |

This whole thing is kind of like a big amazon order being broken into different packages. Each box contains different objects (the payload), but has the same shipping label (header) as the others, and all are united through an order number, tracked by Amazon to make sure you get your order on time (Trailer).  



**Packet Transmission**
Packages, letters, and packets alike need a way to get from point A to point B. In our analogy, UPS, USPS, and FedEx, all optimize routes and who physically move the packages. Packet transmission, works very similarly. As packets are built and labeled they travel through the network on **routers**. Routers are simply devices that forward along packets. Packets keep moving from router to router, following the lowest-traffic path they can find, until they reach the receiving end. Eventually, all of the packets should arrive, but they might be out of order, or delayed. That's where the other TCP comes into play, checking to make sure all of the packets have arrived, and moving to the next step in OSI, or returning an error message to the sender. 

On a more technical level, once a connection is established between two ports, one on the user (initiator) side and one on the reciever side, TCP sends a series if signals back and forth, hard coded with special codes (sequence and acknowledgement numbers), until a 'FIN' code is reached to end the process. 

**Transmission Control Protocol**
Packet construction and transmission are dictated by TCP. TCP exists at both the sending and receiving end of a process. Both TCP entities work together to ensure timely, accurate data transfer using something called the 3-way-handshake. In the 3-way handshake, the client sends a packet "SYN", indicating a desire to open communication with the recieving server. If the recieving server accepts, it sends back another "SYN" followed by an "ACK." The client sends another "ACK" to aknowledge that the connection has opened, and packets containing real information can start to flow back and forth. 

![enter image description here](https://lh3.googleusercontent.com/9sRO80ifa3IzSP4OPzDdcmH4zmVnMx7s71UYDmWMmQ-KcFOx22cL7eEA55PUOgWVWTi_621xrUo)
*Need to make a Lambda graphic* 

![enter image description here](https://lh3.googleusercontent.com/TnoaLUVjrOHY8EjLbJpZauIFcKLfDyL5RkzqCn1qDGok5SxwwZ0b8FHKCeLqJ_iuC7pKYyTW6l4)


## We Do


This video and the next one in the series visually break down how TCP transmission works. Not sure exactly how to turn this into a we do (other than *another* whiteboarding activity) but I think something like this is useful to walk through. 
[https://www.youtube.com/watch?v=4IMc3CaMhyY&list=PLowKtXNTBypH19whXTVoG3oKSuOcw_XeW&index=13&t=0s](https://www.youtube.com/watch?v=4IMc3CaMhyY&list=PLowKtXNTBypH19whXTVoG3oKSuOcw_XeW&index=13&t=0s)


## You Do

Explain it like I'm five (ELI5). Your closest five year old friend asks you what you're learning at Lambda School - explain how packets are constructed and transmitted on a network. 

ELI5 examples: [https://www.reddit.com/r/explainlikeimfive/](https://www.reddit.com/r/explainlikeimfive/)


## Additional Resources

- Video Walkthrough (technical): [TCP](https://www.youtube.com/watch?v=4IMc3CaMhyY&list=PLowKtXNTBypH19whXTVoG3oKSuOcw_XeW&index=13&t=0s)
- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAyMzI0OTk3NywxNjg3NTIzNjg1LDEwND
IxNDQyOSw3MjI0MjkwNjBdfQ==
-->
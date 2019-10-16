# Objective Statement


Understand and explain how packets are constructed and transmitted on a network.

## Instructor Notes


## Required Resources


## I Do
Cybersecurity is concerned with the protection of data. Though they can occur anywhere, breeches most commonly occur when data is moving around from one place to another in the Transport layer of OSI. Data that is unencrypted can be easily intercepted using techniques we’ll learn about later on. In order to understand what's going on under the hood with packet trannsportation, we need to understand the protocol governing this layer, which is Transmission Control Protocol (TCP). 

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

While the analogy is helpful for understanding on a conceptual level, as a cybersecurity professional, you may be tasked with inspecting specific packets - we'll spend the rest of this objective tackling those components. 

An actual packet is configured something like this. It contains 32 bits of data and always has the following information. With the exception of the Data field, all are helping get the information from the client to the server. 

![enter image description here](https://lh3.googleusercontent.com/EGkPMWtfmCytOWdQPvofoHYAbiSv8-FL6fvAXm526xjmPQsZ7dLW7Y1QoRmFn8l8P0sL5ctVlAI)

Before we begin inspecting real-life packets, we need a working definition of what each field represents. 
*The following is borrowed from: [Tech Republic](https://www.techrepublic.com/article/exploring-the-anatomy-of-a-data-packet/)*
-   **Source Port**  and  **Destination Port fields**  (16 bits each) identify the end points of the connection.
-   **Sequence Number field**  (32 bits) specifies the number assigned to the first byte of data in the current message. Under certain circumstances, it can also be used to identify an initial sequence number to be used in the upcoming transmission.
-   **Acknowledgement  Number field**  (32 bits) contains the value of the next sequence number that the sender of the segment is expecting to receive, if the ACK control bit is set. Note that the sequence number refers to the stream flowing in the same direction as the segment, while the acknowledgement number refers to the stream flowing in the opposite direction from the segment.
-   **Data Offset  (a.k.a. Header Length) field**  (variable length) tells how many 32-bit words are contained in the TCP header. This information is needed because the Options field has variable length, so the header length is variable too.
-   **Reserved field**  (6 bits) must be zero. This is for future use.
-   **Flags field**  (6 bits) contains the various flags:  
    URG—Indicates that some urgent data has been placed.  
    ACK—Indicates that acknowledgement number is valid.  
    PSH—Indicates that data should be passed to the application as soon as possible.  
    RST—Resets the connection.  
    SYN—Synchronizes sequence numbers to initiate a connection.  
    FIN—Means that the sender of the flag has finished sending data.
-   **Window field**  (16 bits) specifies the size of the sender's receive window (that is, buffer space available for incoming data).
-   **Checksum field**  (16 bits) indicates whether the header was damaged in transit.
-   **Urgent pointer field**  (16 bits) points to the first urgent data byte in the packet.
-   **Options field**  (variable length) specifies various TCP options.
-   **Data field**  (variable length) contains upper-layer information.


**Packet Transmission**
Packages, letters, and packets alike need a way to get from point A to point B. In our mail analogy, UPS, USPS, and FedEx optimize routes and physically move the packages. Packet transmission, works very similarly. As packets are built and labeled they travel through the network on **routers**. Routers are simply devices that forward along packets. Packets keep moving from router to router, following the lowest-traffic path they can find, until they reach the receiving end. Eventually, all of the packets should arrive, but they might be out of order, or delayed. That's where the other TCP comes into play, checking to make sure all of the packets have arrived, and moving to the next step in OSI, or returning an error message to the sender. 

On a more technical level, once a connection is established between two ports, one on the user (initiator) side and one on the reciever side, TCP sends a series if signals back and forth, hard coded with special codes (sequence and acknowledgement numbers), until a 'FIN' code is reached to end the process. 

**Transmission Control Protocol**
Packet construction and transmission are dictated by TCP. TCP exists at both the sending and receiving end of a process. Both TCP entities work together to ensure timely, accurate data transfer using something called the 3-way-handshake. In the 3-way handshake, the client sends a packet "SYN", indicating a desire to open communication with the recieving server. If the recieving server accepts, it sends back another "SYN" followed by an "ACK." The client sends another "ACK" to aknowledge that the connection has opened, and packets containing real information can start to flow back and forth. 

Conceptually, looks like this: 
![enter image description here](https://lh3.googleusercontent.com/TnoaLUVjrOHY8EjLbJpZauIFcKLfDyL5RkzqCn1qDGok5SxwwZ0b8FHKCeLqJ_iuC7pKYyTW6l4)

Technically, looks more like this: 
![enter image description here](https://lh3.googleusercontent.com/9sRO80ifa3IzSP4OPzDdcmH4zmVnMx7s71UYDmWMmQ-KcFOx22cL7eEA55PUOgWVWTi_621xrUo)




## We Do
 Using tools like Wireshark, which we will work closely with later on, packets can be captured and inspected for component parts. Together, let's annotate the following packet data. It may give a glimpse into what is happening on the network in question. 
![enter image description here](https://lh3.googleusercontent.com/BxWSReZ0wbBW3u0QZDZpWNkwOWfUkDL8ZQW9eVrZNPeYxp0ePfGhtLRd9bTG9i9hnIAwStrFV48)
Thankfully, this packet printout is fairly straightforward. Reading from top down, we start to notice some of the packet components discussed above. For now, we'll focus on: IP addresses, ports, sequence numbers, acknowledgement numbers, flag, cheksum, and data. 
![enter image description here](https://lh3.googleusercontent.com/68F2hIAa_tmkDwtwggDtLc26B8JPjMco0TBe-l3gq0Q9DPRl4CbZ57why7G-A0nw39mmltbCUvc)
- IP addresses aren't technically part of a TCP packet, but they are always sent in tandem. 
- Port numbers tell us the end points of the connection. Here, 443 indicates that the user is connecting to a secure site via HTTPS, and 57880 indicates a private port on the user's end. Since 443 is listed as source, we know that this packet is traveling from the secure site, server, to the client. 
- Sequence number is the number assigned to the first byte of data in the current message. It tells us where in the overall data flow this packet belongs. 
- Acknowledgment number contains the next sequence number that the is expected in flow of data. In and of itself it doesn't tell us much, but combined with packets around it, might be helpful. 
- Flag tells us what type of packet this is - here, an ACK packet, designates that this packet is acknowledging reciept of some information. Maybe an email was sent? 
- A checksum of 0 indicates that the data was not damaged in transit. The fact that it is unverfied only means that the software used for packet sniffing has not completed the data transfer, and that damage can't be confirmed. 
- Finally, our packet contains the encrypted data, not much for us to see, but the Data Link and Physical layers will make use of that later on. 


## You Do
Using the example above as a guide, answer the following questions about this packet: 
1. Where is it coming from? 
2. Where is it going to? 
3. What type of packet is it? 

![enter image description here](https://lh3.googleusercontent.com/KVm2qjJeQBYaPaf30ybA1BdpwlWM_GeCpoFM7EkJ7Q7ZYnTYAHnT9xGi9MtE7D2vykPzHWgkJ14)


## Additional Resources

- Video Walkthrough (technical): [TCP](https://www.youtube.com/watch?v=4IMc3CaMhyY&list=PLowKtXNTBypH19whXTVoG3oKSuOcw_XeW&index=13&t=0s)
- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMDM3OTcwOTYsODYxNjgxODcxLC0xNj
g1MTE4Mzc0LDIxMDE1NDUyOTYsNTExODQxNTE5LC0xMTAyMjQ4
MDcyLC0xNDAyMTE5OTc1LDEzNDI1NTY1MzcsMjA2NzI3NjAzLD
M5OTAxNDg1Myw5MTM5NTE2MzAsMTY4NzUyMzY4NSwxMDQyMTQ0
MjksNzIyNDI5MDYwXX0=
-->
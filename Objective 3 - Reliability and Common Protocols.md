# Objective
Understand the basic mechanics of ethernet, IP, TCP, UDP, ICMP, and ARP
## Instructor Notes


## Required Resources



## I Do

Before computers, important information was transmitted in all sorts of ways: word of mouth, song, dance, cave drawings, railroads, postmen on horses, even carrier pigeons. Each of these prior methods of data transmission required some element of human interaction - a postman needed to sort letters by zip code, an orator needed to use the correct inflection and tone, a pigeon handler needed to tie the note to the bird's leg, you get the idea. The invention of computers and the internet meant that tons of data could be quickly transported, without the need for human intervention! This was huge! But it meant that very specific rules needed to be developed. We call these rules 'protocols' and they dictate exactly how your computer connects to google.com, how it sends an email to your boss, and how humans were able to finally step back from the business of information transmission. 

This objective deals with 6 important protocols involved in data transmission. Like OSI, these protocols can be organized into layers. Here, we'll focus on the Physical Network Layer, Internet Layer, and Transport Layer. In this framework, the Application Layer also exists but isn't the focus of today's objective. Each protocol is connected to another, and all work together to get data from point A to point B. Simple definitions are below: 
|Acronym| Meaning | Layer |Definition  |
|--|--|--|--|
|IP|Internet Protocol| Internet Layer | Basis for communication between devices.  |
|TCP|Transmission Control Protocol |Transport Layer | Ensures accurate communication between devices.  |
|UDP|User Datagram Protocol|Transport Layer|Ensures accurate communication between devices when TCP cannot be used. |
|ICMP|Internet Control Message Protocol |Transport Layer| Blocks inaccurate communication between devices when TCP and UDP fail. |
|ARP|Address Resolution Protocol|Physical Network Layer| Makes sure communication goes to the correct device on a network.|
|Ethernet|Ethernet|Physical Network Layer| Connects all the devices on a network (computers and routers). |

You've heard of IP, and at the very least know that every device in the world has a unique IP address. In a broader context, IP is a set of rules that govern and standardize how packets move from one router to another. IP is great, but IP isn't perfect, and sometimes, packets can get lost. This is where TCP comes in. TCP works with IP to ensure that 1) no packets get lost or duplicated, 2) packets are assembled correctly, and 3) delays aren't significant. In cases where delays are significant, a less sophisticated protocol called UDP can be used to ensure similar packet delivery promises are kept. Sometimes, UDP is used instead of TCP where massive amounts of data need to be sent and reliability isn't as important. 

The ICMP is triggered when UDP or TCP fails and offers suggestions (never seen by the user) to fix the issues, often when ICMP is triggered, the user doesn't know, and TCP/UDP finds another way to get the packets to their destination. Finally, we need to consider ARP and ethernet. Both are working on the physical, network layer level. That means in your home, at the coffee shop, wherever connectivity exists. When data gets to its final network, it needs the ARP to find the specific device (computer, phone, tablet) that it should arrive at. It moves through the ethernet (more commonly, wifi*) until the message is finally received. 

*Ethernet and wifi are _not_ the same thing, but they accomplish the same goal in the communication process. Namely, communicating between all devices on the same network. 


Slightly more technical definitions might be easier to digest with that background: 

|Acronym| Meaning | Definition  |
|--|--|--|
|IP|Internet Protocol|Host or network interface identification and location addressing. |
|TCP|Transmission Control Protocol |Breaks down data into packets and manages delivery from one system to another |
|UDP|User Datagram Protocol|Alternate to TCP, used for establishing low-latency and loss-tolerating connections |
|ICMP|Internet Control Message Protocol |Error Reporting activated when there is an issue with TCP/IP|
|ARP|Address Resolution Protocol|Links MAC addresses and IP addresses to ensure each computer has unique network identification|
|Ethernet|Ethernet|A system for connecting several computer systems to form a local area network, with protocols to control the passing of information and to avoid simultaneous transmission by two or more systems.  |

## We Do
Let's expand on our OSI model whiteboarding activity by placing each protocol into an OSI layer. 

Recall that our OSI model contains 7 layers, and looks like this:
![source: [https://www.webopedia.com/quick_ref/OSI_Layers.asp](https://www.webopedia.com/quick_ref/OSI_Layers.asp)](https://lh3.googleusercontent.com/iMnsbSRP1rAS3MgO3u_A2BhOBz1OXgPNzhkd-Xi6awQnsktyU0Iulyark66HuXaHVOfWuSAj2G0) *need to make a lambda-approved graphic*
 
In the first objective, we talked about OSI on a conceptual level, without knowledge of protocols. Now, we can start to add on to that understanding, by placing protocols into specific layers. 


*Whiteboarding should include this information!
Ethernet isn't included in this diagram but belongs on the Data Link layer
Note that all of the protocols we're worried about are in the 'moving data around' layers* 
![enter image description here](https://lh3.googleusercontent.com/VlhP4wEeA5VqVRrgEqmUoECuTq28G9UFdMcRQZuTwu0GJSJqaNHFYhWLR1-xOeIY9nxg5LAs63Y)

## You Do
Summarize your current understanding of what happens when you type google.com into your internet browser. Be prepared to share in breakout rooms. 


## Additional Resources

- Tech Dictionary: [Techterms.com]((https://techterms.com/))
- Animated Video: [The Internet: Packets, Routing, and Reliability]([https://www.youtube.com/watch?v=AYdF7b3nMto](https://www.youtube.com/watch?v=AYdF7b3nMto)) *the whole series on Internet is likely helpful*
- Reading (IP/TCP): [What IP means and How It Works](https://www.lifewire.com/internet-protocol-explained-3426713)
- Reading (UDP vs TCP): [User Diagram Protocol](https://www.lifewire.com/user-datagram-protocol-817976)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk1ODMwNzM2MiwtMjcwMDg4MjgwXX0=
-->
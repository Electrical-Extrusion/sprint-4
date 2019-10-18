# Objective Statement

Understand the Open Systems Interconnection (OSI) seven-layer model for networks.
  
## Instructor Notes

## Required Resources

- [Video: What is OSI Model?]([https://www.youtube.com/watch?v=Ilk7UXzV_Qc](https://www.youtube.com/watch?v=Ilk7UXzV_Qc))

## I Do

 A common interview question for new software engineers is "what happens when you type in google.com to your web browser?". A seemingly simple exercise is actually hiding an incredibly complex process, most commonly explained by the **Open Systems Interconnection (OSI)** seven-layer model for networks. In this conceptual framework, there are seven distinct layers working together to connect you (the user) to google.com. 

Generally speaking, in this process, information is moving from a user (often referred to as a client) to a place with information (a server) and then returning new information to the client. For this to happen, the client request has to be translated into a common computer language *and* transported to the server, which happens, conceptually speaking, in seven steps. We call these steps 'layers' since lots of sub-steps occur at each.  These sub-steps, called protocols, are grouped by the function performed into layers. Every layer preforms some job and passes the information along, transmitting and receiving the information as data in some form or another. The seven layers are pictured below.

![source: [https://www.webopedia.com/quick_ref/OSI_Layers.asp](https://www.webopedia.com/quick_ref/OSI_Layers.asp)](https://lh3.googleusercontent.com/iMnsbSRP1rAS3MgO3u_A2BhOBz1OXgPNzhkd-Xi6awQnsktyU0Iulyark66HuXaHVOfWuSAj2G0) *need to make a lambda-approved graphic*

Let's take a look at the layers, broken into the 'Application Level' layers (5-7) and the 'Moving Data around' layers (1-4). If you've ever used the internet you are familiar with layer 7, the application layer because it is where you interact with data (think: sending an email or performing a google search) but, the rest are equally important. If anyone layer was skipped or broken, the information could not move between devices. As shown in the diagram, both devices (client and server) involved in the data transfer will go through these steps. For now, let's explore what happens on the user end when you make a request. Information is moving down the layers, starting with Application.  Some of the examples may not make sense until later on in this module.

### Application-level layers

| Layer| Name | Explanation |Example|
|--|--|--|--|
| 7 |Application |The user (human) puts in a request for information. | Chrome, Outlook, Skype, any HTTP request |
|6|Presentation|Data is transformed and translated so it can be read. Encryption also happens here. |"Send Email" -> 11001001 -> !@&sh12#!@|
| 5 |Session|Connection between user and receiving server is opened and maintained. Authentication happens here. | Streaming channel is opened. |

### Moving data around layers

| Layer| Name | Explanation |Example|
|--|--|--|--|
| 4 |Transport|Data moves from end to end, transfer is completed. Dictates how fast data is sent, where, and when. |Email moves through outerspace, TCP, UDP |
| 3 |Network|Data moves through switching and routing pathways on multiple local networks. | Email is directed to the correct wi-fi network, IP addresses |
| 2 |Data Link| Data is chunked into packets, encoded and decoded at switches within a single local network. | Email is directed at the correct computer on the network, MAC, LLC |
| 1 |Physical  |Data is converted to bits and sent through hardware, pins, volts, and cables through electricity.  | Electricity traveling through ethernet cord, power cord.  |

A real-life analogy might look something like this

#### Application Level

7. Write a letter in German for a Russian friend.
6. Translate the letter into a universal language.
5. Place the letter in an envelope and label the sender/return address.

#### Moving Data Around

4. The letter moves through international postal service.
3. The letter moves around local Russian postal service.
2. The letter is placed in the Russian mailbox.  
1. Recipient reads the letter.  

In this analogy, the user (presumably German-speaking), needs to communicate with a Russian-speaking friend. If they didn't translate the letter, it wouldn't make sense to them. If they didn't put the letter in an envelope, it would never get to them. If the letter got lost in the international postal service... you guessed it, it wouldn't get to them! In the same way, all 7 layers of the OSI model are crucial for data transmission. We'll learn more about the technicalities of each layer in upcoming objectives, but for now, let's continue to focus on the overall theory in a common interview exercise: whiteboarding.

## We Do

Okay, so that still doesn't answer the question - what actually happens when you type in google.com? We will synthesize those steps with a whiteboarding activity, and this time, consider both the transmission and receipt of data. Keep this drawing handy, because you'll need it again throughout the unit.

  *Whiteboarding should walk through the 7 steps and visually display the transfer from application to device to routers to physical components and back again. Include sketches of a computer, router, power cord, etc.
The required video animates the process well:*[https://www.youtube.com/watch?v=Ilk7UXzV_Qc&t=192s](https://www.youtube.com/watch?v=Ilk7UXzV_Qc&t=192s) *

## You Do

Using the German/Russian correspondence example as a guide, develop a new analogy to link the OSI model to a process in everyday life.

## Additional Resources

- Blog: [You won't Believe what the OSI Model and Pizza Have in Common](https://www.versatek.com/blog/you-wont-believe-what-the-osi-model-and-pizza-have-in-common/)
- Blog: [OSI Model Layers - "Explained"](https://medium.com/learn-with-the-lean-programmer/osi-model-layers-explained-ee1d43058c1f)
- Tricks to Memorize OSI Layers: [The OSI model explained: How to understand (and remember) the 7 layer network model](https://www.networkworld.com/article/3239677/the-osi-model-explained-how-to-understand-and-remember-the-7-layer-network-model.html)
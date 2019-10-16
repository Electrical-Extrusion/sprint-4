# Objective Statement
Understand the Open Systems Interconnection (OSI) seven layer model for networks.
  
## Instructor Notes


## Required Resources

- [Video: What is OSI Model?]([https://www.youtube.com/watch?v=Ilk7UXzV_Qc](https://www.youtube.com/watch?v=Ilk7UXzV_Qc))

## I Do

 A common interview question for new software engineers is "what happens when you type in google.com to your web browser?". A seemingly simple exercize is actually hiding an incredibly complex process, most commonly explained by the **Open Systems Interconnection (OSI)** seven layer model for networks. In this conceptual framework, there are seven distinct layers ultimately connecting you (the user) to google.com. 

Generally speaking, information is moving from a user (often reffered to as a client) at a point of interaction (an application), to a place with information (a server) and then returning back to the client. In order for this to happen, the client request has to be translated and transported, which happens, conceptually speaking, in seven steps. We call these steps layers, since lots of sub-protocols occur at each.  These sub-protocols are grouped into layers by the function preformed. Each layer has its own job, and passes information to the next layer, transmitting and receiving data in some form or another. The seven layers are pictured below. 

![source: [https://www.webopedia.com/quick_ref/OSI_Layers.asp](https://www.webopedia.com/quick_ref/OSI_Layers.asp)](https://lh3.googleusercontent.com/iMnsbSRP1rAS3MgO3u_A2BhOBz1OXgPNzhkd-Xi6awQnsktyU0Iulyark66HuXaHVOfWuSAj2G0) *need to make a lambda-approved graphic*
 
Let's take a look at the layers, broken into the 'Application Level' layers (5-7) and the 'Moving Data around' layers (1-4). If you've ever used the internet you are familiar with layer 7, the application layer, because it is where you interact with data (think: sending an email, or preforming a google search) but, the rest are equally important. If any one layer was skipped or broken, information could not move between devices. As shown in the diagram, both devices (client and server) involved in the data transfer will go through these steps. For now, let's explore what happens on the user end when you type in 'google.com'. Information is moving down the layers, starting with Application. 

**Application level layers:** 
| Layer| Name | Explanation |Example|
|--|--|--|--|
| 7 |Application |The user (human) puts in a request for information. | Chrome, Outlook, Skype, any HTTP request |
|6|Presentation|Data is transformed and translated so it can be read. Encryption also happens here. |"Send Email" -> 11001001 -> !@&*()|
| 5 |Session|Connection between user and receiving server is opened and maintaned. | |

**Moving data around layers:** 
| Layer| Name | Explanation |Example|
|--|--|--|--|
| 4 |Transport|Data moves from end to end, transfer is completed. (TCP, UDP). | |
| 3 |Network|Data moves through switching and routing pathways. (IP addresses). | |
| 2 |Data Link| Data is chunked into packets, encoded and decoded at switches within the local network.  | |
| 1 |Physical  |Data is converted to bits and sent through hardware, pins, volts, and cables through electricity.  | |


**Application Level**
 7. Application - The user (human) puts in a request for information.
 6. Presentation - Data is transformed and translated so it can be read.
 5. Session - Connection between user and receiving server is opened and maintaned.

**Moving Data Around**
 4. Transport - Data moves from end to end, transfer is completed. (TCP, UDP).
 3. Network - Data moves through switching and routing pathways. (IP addresses).
 2. Data Link - Data is chunked into packets, encoded and decoded at switches within the local network.  
 1 Physical - Data is converted to bits and sent through hardware, pins, volts, and cables through electricity. 

A real life analogy might look something like this: 
**Application Level**
 7. Write a letter in German for a Russian friend. 
 6. Translate letter into a universal language. 
 5. Place letter in envelope and label sender/return address. 

**Moving Data Around**
 4. Letter moves through international postal service. 
 3. Letter moves around local Russian postal service. 
 2. Letter is placed in Russian mailbox.  
 1 Recipient reads letter.  

In this analogy, the user (presumably German-speaking), needs to communicate with a Russian-speaking friend. If they didn't translate the letter, it wouldn't make sense to them. If they didn't put the letter in an envolope, it would never get to them. If the letter got lost in the international postal service... you guessed it, it wouldn't get to them! In the same way, all 7 layers of the OSI model are crucial for data transmission. We'll learn more about the technecalities of each layer in upcoming objectives, but for now let's continue to focus on the overall theory in a common interview excercize: whiteboarding. 

## We Do
Okay, so that still doesn't answer the question - what actually happens when you type in google.com? We will synthesize those steps with a whiteboarding activity, and this time, consider both the transmission, and reciept of data. Keep this drawing handy, because you'll need it again throughout the unit. 

  *Whiteboarding should walk through the 7 steps and visually display the transfer from application to device to routers to physical components and back again
The required video animates the process well:*[https://www.youtube.com/watch?v=Ilk7UXzV_Qc&t=192s](https://www.youtube.com/watch?v=Ilk7UXzV_Qc&t=192s) *

## You Do
Using the German/Russian correspondence example as a guide, develop a new analogy to link the OSI model to a process in every day life. 


  

## Additional Resources
- Blog: [You won't Believe what the OSI Model and Pizza Have in Common](https://www.versatek.com/blog/you-wont-believe-what-the-osi-model-and-pizza-have-in-common/)
- Blog: [OSI Model Layers - "Explained"](https://medium.com/learn-with-the-lean-programmer/osi-model-layers-explained-ee1d43058c1f)

  


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY0NTY0NTQ3MiwxNjMzODU4NTQwLDE3OT
YzODM2OTEsMTQwMzY1NjY1MF19
-->
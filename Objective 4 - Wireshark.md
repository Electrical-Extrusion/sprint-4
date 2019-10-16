# Objective
Install a packet capture utility (wireshark) to capture and view packets on student's local computer.

## Instructor Notes
*Video for We Do is probably really important here*

## Required Resources
- Software Download: [Download Wireshark](https://www.wireshark.org/download.html)

## I Do
One tool security professionals use to make sure data is being transmitted securely is called a packet analyzer. Packet analyzers intercept and log traffic over a network, functioning in many ways like a microscope, to allow users to see what's going on 'under the hood' of the internet. Today we will install a  popular and free packet analyzer called wireshark (linked in required resources above).

Once downloaded, we can look at the familiar packet details coming in and out of our local devices, including source IP, destination IP, length (in bytes), source port, destination port, payload data, and more. 

In the 'real world' of cybersecurity, Wireshark is popularly used to diagnose network problems by locating the exact packets that are not properly transmitting. 


## We Do
Let's download wireshark together and use it to finally figure out what happens when we type in 'google.com'.

1.  Download the stable release version for your OS .![enter image description here](https://lh3.googleusercontent.com/90C_FSB0VJC6y3wJY3TCEsyh7XX1HxDaMk-VhJiYtSFE4YfXjyUI3MBZbHBnUMyBu2jMBDqL_4Y)

2. Open the instaler and follow on-screen prompts
![enter image description here](https://lh3.googleusercontent.com/c7zrf23CYMID1YtgDdeOpJvqKOZG7YRJSGUp630N1u6fXjlguwD-JBMhmtT0iyZFmUS52Dk5h2Q)

3. On the home screen, all network connections (wired, wireless, and external capture) are visible, like so: ![enter image description here](https://lh3.googleusercontent.com/g3S1RZdPUBUiv9CconEabQgG_SzMQvyGLUaCbJmyqSHHxROIx0qxPxmE9xPXRqsiWB9p9YaWFGA)

4. Click the blue fin to begin capturing packet data: 
![enter image description here](https://lh3.googleusercontent.com/jNPSyRABImjqZurXCpzdvF6LFcJSXnBxhz5KqX4y0xYBQEp7RJv1XKOm13N9lOSzTVjBJnRyR-c)

5. You'll notice data being captured right away, these are background tasks, open windows, network upkeep, and the like. To answer our question we will need to visit an internet browser and type 'google.com'. 
![enter image description here](https://lh3.googleusercontent.com/UH0WFdg60NKDDZ9WdUHQp-_9_-YMQEzbcZESzoEZoHN1HUlidLmUpl5TFH5os-0JdM3TnZ7xd4I)
6. Once google.com has loaded, return to wireshark and stop the capture using the red square. 
![enter image description here](https://lh3.googleusercontent.com/InG6MRduYa4jUKrwm2QgFaBXC9__XRi9vo3PONGTqHmJDSLvXQqJPB_UhcpFEnhSboSPnzBTBkI)

7. We can now view all packet data, including familiar information like protocol, size, and IP addresses. Click on a packet to inspect data it carries. Since google.com is a secure site using https/:/ we can't make much of what we see. ![enter image description here](https://lh3.googleusercontent.com/TXlLQWRG5cs7UtA5g2yVvppyJKoARoJmh_cgzymxNJ4YDu0ibBMe1dAPG5Xqq3f0mjHttIE4GEQ) 

8. Analyze Data using the Statistics tool - the true power of wireshark comes in it's ability to breakdown and analyze massive amounts of packet data. For now, we'll just view the Capture File Properties. 
![enter image description here](https://lh3.googleusercontent.com/7qb_r25BQyrmXdICWNNGKf3KDVa4nK22Fb80Kuhxc4XDoaO0I2_tBFwMrXJmTKzodQK3VOeTBSo)
![enter image description here](https://lh3.googleusercontent.com/1Cdc5loX_z6dI1Qs0uHlQygK3M5lJp6d7s7P4fKN6AGgvZi35tttwxCE73KAEC9TxvyTLWAwkAg)
File capture properties shows a nice summary of all the packets captured. This specific screenshot is from a relatively short capture, 5.939 seconds but still shows nice data about drop rate (0%), packet size, and more. 

## You Do
Use the statistcs tool to figure out the average packet size sent and recieved when trying to connect to different websites. Connect to at least 10 websites. Be prepared to come to class with your observations. 

## Additional Resources

- Official Documentation: [Wireshark User's Guide]([https://www.wireshark.org/docs/wsug_html_chunked/](https://www.wireshark.org/docs/wsug_html_chunked/))
- Blog: [How to Use Wireshark](https://www.varonis.com/blog/how-to-use-wireshark/)
- Blog: [What is Packet Sniffing](https://www.comparitech.com/blog/information-security/what-is-packet-sniffing/)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMzMwNTAxNDJdfQ==
-->
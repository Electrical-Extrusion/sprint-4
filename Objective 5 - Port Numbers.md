# Objective

Know the port numbers for common application-layer protocols (HTTP/S, FTP, SSH, DNS, RDP).

## Instructor Notes

## Required Resources

## I Do

A port is a destination endpoint for data being transported by TCP or UDP. Sometimes, port numbers are referred to as "logical addresses," because they represent a place for data to go.

At any one time, a device will be running many different tasks. Just like a human brain, a computer needs to compartmentalize these tasks in order to complete them all. That's why an IP address alone (the device level address) is not sufficient to direct packets where they need to go.

The IP/port relationship is best explained with an analogy. If an IP address represents the street name and city, a port number is like the house number. Using the wrong port number is like trying to visit your parent's house, by ringing a doorbell down the street. You'd be close to where you needed to be, but your parents would never know you were looking for them! (Unless their neighbor called them, but computers don't do that!).

Using the wrong port number, similarly, will move data to the correct server or device, but ultimately return an error, as the data isn't where it needs to be. Basically, TCP would get confused if all packets for all tasks came to the same place. Having unique port numbers for different types of tasks (load a web page vs. transfer a file vs. send an email) ensures that all tasks can be successfully and securely completed.

Later on, we'll see how this works for ourselves. For now, know that under the hood of a URL both an IP address and a port number exist. The port number operated in the data link layer by directing packets on the local network level.

Well known ports include:
|Protocol| Function |Port Number  |
|--|--|--|
| HTTP |Web Pages| 80  |
| HTTPS | Secure Web Pages| 443  |
| FTP |File Transfer| 20 (data), 21 (command)  |
| SSH |Secure Shell|22  |
| DNS |Domain Name System Service|53  |
| RDP |Remote Desktop Connection |3389  |

Some of the more self explanatory functions include HTTP and HTTPS to access web pages, and FTP which assists in file transfer. SSH is used to manage network devices in a secure channel. DNS does a lot of things, but primarily translates domain names (like 'google.com') into IP numbers that a computer can understand.  Finally, RDP allows a user to control another desktop remotely, primarily for IT type support, but of course there are many other uses.

## We Do

### Example #1

To demonstrate, lets use what we learned above to try to connect to 'google.com'. If you type 74.125.127.147 into your web browser, you'll be directed to google.com with the default port number. Under the hood of an IP address is a port number that can be easily changed.

1. In your web browser type 'google.com:80', this indicates that you are trying to access google.com's server, at port #80, designated for web pages. Since google.com is indeed a webpage, this should load the google homepage.
![enter image description here](https://lh3.googleusercontent.com/EAMuSfgyh0YgEerTK7ja2fNMI34RDT6jVZ1VrhXnMO_Rs_APnlwBQBOuHwX0CvWZ2JX0saluozzG)
2. Now try typing 'google.com:443'. This indicates you  are trying to access google.com's server at port #443, designated for *secure* web pages. Should still work, since google.com is a secure webpage.
![enter image description here](https://lh3.googleusercontent.com/EAMuSfgyh0YgEerTK7ja2fNMI34RDT6jVZ1VrhXnMO_Rs_APnlwBQBOuHwX0CvWZ2JX0saluozzG)

3. Finally, let's try typing in google.com:20, the port number designated for file transfer. You'll get an error message. Why? You're trying to load a web page using a file transfer port. It's like trying to go to your friend Ada's house, but ringing Grace's doorbell. ![enter image description here](https://lh3.googleusercontent.com/EvpwydO-jfWMAz4ybs2169H8lTEFg6V1KYJtxiEr_DIGDPvIHZQX7EryJ-aniY7dTk1FqRKCZU8M)

### Example #2

1. Look at more packet streams in Wireshark - screen recording of how to apply column and view all the port numbers in TCP. Most will be 443/some private port.

## You Do

Run your own capture in Wireshark and take not of the port numbers used. Apply source and destination port numbers as columns and sort results accordingly.

## Additional Resources

- Reference: [Well Known Port Numbers](https://www.webopedia.com/quick_ref/portnumbers.asp)
- Blog: [TCP/IP Ports and Protocols](http://www.pearsonitcertification.com/articles/article.aspx?p=1868080)  

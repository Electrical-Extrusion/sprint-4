# Objective

Search packet streams for strings. 
Search for string information in packet data.

## Instructor Notes

## Required Resources

## I Do

Alongside simply extracting data, it can sometimes be helpful to search for specific strings within packets. Packets containing certain URL information, usernames, passwords, and more represent significant network vulnerabilities.  

Wireshark's user interface makes it easy to search for strings within packets. Let's say you want to search for the term 'pdf' within packets, you could simply follow the steps below to isolate packets that discuss pdf.

1. Edit -> Find Packet (or command F)
![Find Packet](https://i.imgur.com/h9cIkDk.png)

2. Change 'Display Filter' to 'String.'
![Screen Shot 2019-10-18 at 10.58.21 AM](https://i.imgur.com/8bFVf0w.png)

3. Enter a string you want to search for, for example, you could enter a username, an IP address, or simply a word like 'password'. Here, our interest is finding packets containing the term pdf, so the network administrator entered the term pdf.![Screen Shot 2019-10-21 at 12.54.38 PM](https://i.imgur.com/RwSB6sm.png)

In this case, the return was a list of TCP and HTTP packets which were involved in the transmission of application/pdf files.
![Screen Shot 2019-10-21 at 12.54.46 PM](https://i.imgur.com/v0oAuu4.png)

## We Do

Together, we'll walk through how wireshark can be used to search for strings within packets. As we practice, you'll notice that the quality of this tool is only as strong as the terms you search for. Later on, we'll work on building higher quality scanning systems and filtering for suspicious activity.

Here, a simple video exercise that follows what we did in the 'I do' section seems to make the most sense. 

## You Do

Consider strings that a cyber security expert might want to search for to ensure the network is safe. Generate a list of these terms. Next, search through a packet capture to find those terms.

## Additional Resources

- Documentation: [Finding Packets](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkFindPacketSection.html)

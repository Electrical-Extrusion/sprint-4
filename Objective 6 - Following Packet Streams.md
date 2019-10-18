# Objective

Identify and reconstruct packet streams in packet capture utility.

## Instructor Notes

## Required Resources

## I Do

In any one capture, Wireshark will capture tens or even thousands of transmissions. The majority of these transmissions deal with background activity or normal network tasks, things that may not be of interest. With that much noise, how can you follow a single packet along? After all, packet data is really only useful when it can be combined with the other packets in a transmission. To this point, our best tool to look through a large packet capture was to manually identify packets from the same transmission, and attempt to piece them together offline. Thankfully, there is a better way to aggregate packet data and capture a fuller understanding of the data being transmitted.

Using a packet capture utility (Wireshark), you can easily easily track a stream from inititiation to close and follow the data within. Most of the time, the payload will be encrypted, but we can still gather usesful information looking at other elements of the TCP header. Frequently, cybersecurity analysts develop algorithms that detect anomoiles in  number of packets sent, sum of bytes, start time, or end time. Other times IP addresses and port numbers can give insight to the transmission in question.

Occasionally packet streams can lead to deeper insight, mostly when payload data is not secure or encrypted.

## We Do

1. Open Wireshark.
2. Start packet capture by clicking on the blue fin.
![enter image description here](https://lh3.googleusercontent.com/gv-Gzf2Crp2AlJsLnrwG7wR2CQSbAMu41kLjpdJpi9yYOCedhxRSxcVG1LQxeKCO9SM50GTWnmqN)
3. Let packet capture run for a while.
![enter image description here](https://lh3.googleusercontent.com/KrlQbXu9LY0yN4DE0VFKrE5wlZ1J11rvHuxjm2NDByNZpDRjj-KuEdwdLRDVc9TuQWTQS4Qx_NdX)
4. find a TCP packet of interest. Right Click -> Follow -> Follow TCP Stream
![enter image description here](https://lh3.googleusercontent.com/WMnVZJcCr2k4CsGRkneiF6DzaXIheXjHk7RuU2-94d2Qxd5wrdpRf_e3DfP-JFrhIyBSUGblmxfN)
5. TCP Stream report will show sender (red) and reciever (purple) messages from the whole connnection. This conversation can be viewed in different data styles (ASCII, hexcode, and others), and parsed to view each side of the conversation.
![enter image description here](https://lh3.googleusercontent.com/-sI_dMFhd4R7ire9I_YqLDnAw6sm01UytCIp5eQjEXR1w-O7E4u_1tU68CCpElvaYjVeR67HczFj)

## You Do

Gather and inspect 5 different packet streams. Identify the number of packets sent in each, and the total conversation size.

## Additional Resources

- Documentation: [Following Protocol Streams](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvFollowStreamSection.html)
- Video: [Wireshark 101: TCP Streams and Objects](https://www.youtube.com/watch?v=yb2YSv_QtAQ)
- Blog: [Working with Packet Streams](https://hub.packtpub.com/wireshark-working-packet-streams/)

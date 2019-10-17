# Objective
Identify and reconstruct packet streams in packet capture utility.

## Instructor Notes

## Required Resources

## I Do
Packet data is really only useful when it can be combined with the other packets in a transmission, to give a full understanding of the data being transmitted. 

Using a packet capture utility (Wireshark), you can easily easily track a stream from inititiation to close and aggregate the data within. Of course, this data will be encrypted, but we'll deal with that later on. 

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
Inspect 5 different packet streams. Identify the number of packets sent in each, and the total conversation size. 

## Additional Resources
- Documentation: [Following Protocol Streams](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvFollowStreamSection.html)
- 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NTE5ODY4MDYsMTg0MzcwMzU3OSw5OD
gwMjk3NjksMTgxNjAwMjM3LC0xMDY1MzAwNTgzLC0xNDcwNTI4
MjU3LC0xMzAyMzgxMjk3XX0=
-->
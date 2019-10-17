# Objective
Identify and reconstruct packet streams in packet capture utility.

## Instructor Notes

## Required Resources

## I Do
Packet data is really only useful when it can be combined with the other packets in a transmission, to give a full understanding of the data being transmitted. 

Using a packet capture utility (Wireshark), you can easily easily track a stream from inititiation to close and aggregate the data within. Of course, this data will be encrypted

## We Do

1. Open Wireshark.
2. Start packet capture by clicking on the blue fin. 
3. Let packet capture run for a while. 
4. find a TCP packet of interest. 
5. Right Click -> Follow -> Follow TCP Stream
6. Ta-da!

## You Do
Inspect 5 packet streams. Identify the number of packets sent in each. 

## Additional Resources
- Documentation: [Following Protocol Streams](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvFollowStreamSection.html)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjEwMTQ5NzczMSwxODE2MDAyMzcsLTEwNj
UzMDA1ODMsLTE0NzA1MjgyNTcsLTEzMDIzODEyOTddfQ==
-->
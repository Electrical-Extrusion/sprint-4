---


---

<h1 id="objective">Objective</h1>
<p>Understand the basic mechanics of ethernet, IP, TCP, UDP, ICMP and ARP</p>
<h2 id="instructor-notes">Instructor Notes</h2>
<h2 id="required-resources">Required Resources</h2>
<h2 id="i-do">I Do</h2>
<p>Before computers, important information was transmitted in all sorts of ways: word of mouth, song, dance, cave drawings, carrier pigeons,  railroads, postmen on horse, postmen on foot. Each of these prior methods of data transmission required some element of human interaction - a postman needed to sort letters by zip code, an orator needed to use the correct inflection and tone, you get the idea. The invention of computers and the internet meant that tons of data could be quickly transported, without the need for human intervention! This was huge! But it meant that very specific rules needed to be developed. We call these rules ‘protocols’ and they dictate exactly how your computer connects to <a href="http://google.com">google.com</a>, how it sends an email to your boss, and how humans were able to finally step back from the business of information transmission.</p>
<p>This objective deals wth 6 important protocols involved in data transmission. Like OSI, these protocol can be organized into layers. Here, we’ll focus on the Physical Network Layer, Internet Layer, and Transport Layer. In this framework, the Application Layer also exists, but isn’t the focus of today’s objective. Each protocol is connected to another, and all work together to get data from point A to point B. Simple definitions are below:</p>

<table>
<thead>
<tr>
<th>Acronym</th>
<th>Meaning</th>
<th>Layer</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr>
<td>IP</td>
<td>Internet Protocol</td>
<td>Internet Layer</td>
<td>Basis for communication between devices.</td>
</tr>
<tr>
<td>TCP</td>
<td>Transmission Control Protocol</td>
<td>Transport Layer</td>
<td>Ensures accurate communication between devices.</td>
</tr>
<tr>
<td>UDP</td>
<td>User Datagram Protocol</td>
<td>Transport Layer</td>
<td>Ensures accurate communication between devices when TCP cannot be used.</td>
</tr>
<tr>
<td>ICMP</td>
<td>Internet Control Message Protocol</td>
<td>Transport Layer</td>
<td>Blocks inaccurate communication between devices when TCP and UDP fail.</td>
</tr>
<tr>
<td>ARP</td>
<td>Address Resolution Protocol</td>
<td>Physical Network Layer</td>
<td>Makes sure communication goes to the correct device on a network.</td>
</tr>
<tr>
<td>Ethernet</td>
<td>Ethernet</td>
<td>Physical Network Layer</td>
<td>Connects all the devices on a network (computers and routers).</td>
</tr>
</tbody>
</table><p>You’ve heard of IP, and at the very least know that every device in the world has a unique IP address. In a broader context, IP is a set of rules that govern and standardize how packets move from one router to another. IP is great, but IP it isn’t perfect, and sometimes, packets can get lost. This is where TCP comes in. TCP works with IP to ensure that 1) no packets get lost or duplicated, 2) packets are assembeled correctly, and 3) delays aren’t significant. In cases where delays are significant, a less sophisticated protocol called UDP can be used to ensure similar packet delivery promises are kept. Sometimes, UDP is used instead of TCP where massive amounts of data need to be sent and reliability isn’t as important.</p>
<p>The ICMP is triggered when UDP or TCP fails, and offers suggestions (never seen by the user) to fix the issues, often when ICMP is triggered, the user doesn’t know, and TCP/UDP finds another way to get the packets to their destination. Finally, we need to consider ARP and ethernet. Both are working on the physical, network layer level. That means in your home, at the coffee shop, wherever connectivity exsists. When data gets to its final network, it needs the ARP to find the specific device (computer, phone, tablet) that it should arrive at. It moves through the ethernet (more commonly, wifi*) until the message is finally recieved.</p>
<p>*Ethernet and wifi are <em>not</em> the same thing, but they accomplish the same goal in the communication process. Namely, communicating between all devices on the same network.</p>
<p>Slightly more technical definitions might be easier to digest with that background:</p>

<table>
<thead>
<tr>
<th>Acronym</th>
<th>Meaning</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr>
<td>IP</td>
<td>Internet Protocol</td>
<td>Host or network interface identification and location addressing.</td>
</tr>
<tr>
<td>TCP</td>
<td>Transmission Control Protocol</td>
<td>Breaks down data into packets and manages delivery from one system to another</td>
</tr>
<tr>
<td>UDP</td>
<td>User Datagram Protocol</td>
<td>Alternate to TCP, used for establishing low-latency and loss-tolerating connections</td>
</tr>
<tr>
<td>ICMP</td>
<td>Internet Control Message Protocol</td>
<td>Error Reporting activated when there is an issue with TCP/IP</td>
</tr>
<tr>
<td>ARP</td>
<td>Address Resolution Protocol</td>
<td>Links MAC addreses and IP addreses to ensure each computer has unique network identification</td>
</tr>
<tr>
<td>Ethernet</td>
<td>Ethernet</td>
<td>A system for connecting a number of computer systems to form a local area network, with protocols to control the passing of information and to avoid simultaneous transmission by two or more systems.</td>
</tr>
</tbody>
</table><h2 id="we-do">We Do</h2>
<p>Let’s expand on our OSI model whiteboarding activity by placing each protocol into an OSI layer.</p>
<p><strong>Video?</strong></p>
<h2 id="you-do">You Do</h2>
<p>Summarize your current understanding of what happens when you type <a href="http://google.com">google.com</a> into your internet browser. Be prepared to share in breakout rooms.</p>
<h2 id="additional-resources">Additional Resources</h2>
<ul>
<li>Tech Dictionary: <a href="(https://techterms.com/)">Techterms.com</a></li>
<li>Animated Video: <a href="%5Bhttps://www.youtube.com/watch?v=AYdF7b3nMto%5D(https://www.youtube.com/watch?v=AYdF7b3nMto)">The Internet: Packets, Routing, and Reliability</a> <em>the whole series on Internet is likely helpful</em></li>
<li>Reading (IP/TCP): <a href="https://www.lifewire.com/internet-protocol-explained-3426713">What IP means and How It Works</a></li>
<li>Reading (UDP vs TCP): <a href="https://www.lifewire.com/user-datagram-protocol-817976">User Diagram Protocol</a></li>
</ul>


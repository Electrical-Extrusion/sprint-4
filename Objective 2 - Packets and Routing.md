---


---

<h1 id="objective-statement">Objective Statement</h1>
<p>Understand and explain how packets are constructed and transmitted on a network.</p>
<h2 id="instructor-notes">Instructor Notes</h2>
<h2 id="required-resources">Required Resources</h2>
<h2 id="i-do">I Do</h2>
<p>Cybersecurity becomes important when data is moving around from one place to another. Data that isn’t properly secured or broken up can be easily intercepted by hackers in a process that we’ll learn later on. For now, we’ll focus on defining the term “packets” and understanding how those are transmitted on a network.</p>
<p><strong>Packet Construction</strong><br>
A packet, as you may have guessed, is a chunk of data. When a request is made by a user to send or receive information, it takes the form of data. This data is broken into packets, which may all take different routes, but eventually end up at the same destination to complete the request. Intercepting unencrypted packets is one-way hackers can obtain sensitive information: like usernames and passwords. Regardless of the type of security, or data included, packets always contain the following three parts. When learning this concept it can be helpful to use an analogy of literal packages, and consider how these find their way through a postal system.</p>

<table>
<thead>
<tr>
<th>Packet Part</th>
<th>Definition</th>
<th>Analogy</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Header</strong></td>
<td>The header contains instructions like the sender’s IP address, receiver’s IP address, Protocol, and Packer number</td>
<td>Front of an envelope - addresses, shipping label or stamp.</td>
</tr>
<tr>
<td><strong>Payload</strong></td>
<td>The payload is where the actual data is stored</td>
<td>The letter inside the envelope.</td>
</tr>
<tr>
<td><strong>Trailer</strong></td>
<td>The trailer contains data to show that the interpreter has reached the end of the packet, or, throws an error when needed</td>
<td>Signature at the end of the letter.</td>
</tr>
</tbody>
</table><p>Packet construction is dictated by something called the Transmission Control Protocol (TCP). TCP exists at both the sending and receiving end of a process. When someones sends a request, the TCP on the sender’s end breaks the data into payloads, and labels each with the needed header, creating a multitude of packets.</p>
<p>This whole thing is kind of like a big amazon order being broken into different packages. Each box contains different objects (the payload), but has the same shipping label (header) as the others, and all are united through an order number, tracked by Amazon to make sure you get your order on time (Trailer).</p>
<p><strong>Packet Transmission</strong><br>
Packages, letters, and packets alike need a way to get from point A to point B. In our analogy, UPS, USPS, and FedEx, all optimize routes and who physically move the packages. Packet transmission, works very similarly. As packets are built and labeled they travel through the network on <strong>routers</strong>. Routers are simply devices that forward along packets. Packets keep moving from router to router, following the lowest-traffic path they can find, until they reach the receiving end. Eventually, all of the packets should arrive, but they might be out of order, or delayed. That’s where the other TCP comes into play, checking to make sure all of the packets have arrived, and moving to the next step in OSI, or returning an error message to the sender.</p>
<p>On a more technical level, once a connection is established between two ports, one on the user (initiator) side and one on the reciever side, TCP sends a series if signals back and forth, hard coded with special codes (sequence and acknowledgement numbers), until a ‘FIN’ code is reached to end the process.</p>
<p><img src="https://lh3.googleusercontent.com/9sRO80ifa3IzSP4OPzDdcmH4zmVnMx7s71UYDmWMmQ-KcFOx22cL7eEA55PUOgWVWTi_621xrUo" alt="enter image description here"><br>
<em>Need to make a Lambda graphic</em></p>
<h2 id="we-do">We Do</h2>
<p>This video and the next one in the series visually break down how TCP transmission works. Not sure exactly how to turn this into a we do (other than <em>another</em> whiteboarding activity) but I think it is useful to see.<br>
<a href="https://www.youtube.com/watch?v=4IMc3CaMhyY&amp;list=PLowKtXNTBypH19whXTVoG3oKSuOcw_XeW&amp;index=13&amp;t=0s">https://www.youtube.com/watch?v=4IMc3CaMhyY&amp;list=PLowKtXNTBypH19whXTVoG3oKSuOcw_XeW&amp;index=13&amp;t=0s</a></p>
<h2 id="you-do">You Do</h2>
<p>Explain it like I’m five (ELI5). Your closest five year old friend asks you what you’re learning at Lambda School - using a different anaolgy than the packages/envelopes we discussed above, explain how packets are constructed and transmitted on a network.</p>
<p>ELI5 examples: <a href="https://www.reddit.com/r/explainlikeimfive/">https://www.reddit.com/r/explainlikeimfive/</a></p>
<h2 id="additional-resources">Additional Resources</h2>
<ul>
<li>Video Walkthrough (technical): <a href="https://www.youtube.com/watch?v=4IMc3CaMhyY&amp;list=PLowKtXNTBypH19whXTVoG3oKSuOcw_XeW&amp;index=13&amp;t=0s">TCP</a></li>
<li></li>
</ul>


---


---

<h1 id="objective-statement">Objective Statement</h1>
<p>Understand the Open Systems Interconnection (OSI) seven layer model for networks.</p>
<h2 id="instructor-notes">Instructor Notes</h2>
<h2 id="required-resources">Required Resources</h2>
<ul>
<li><a href="%5Bhttps://www.youtube.com/watch?v=Ilk7UXzV_Qc%5D(https://www.youtube.com/watch?v=Ilk7UXzV_Qc)">Video: What is OSI Model?</a></li>
</ul>
<h2 id="i-do">I Do</h2>
<p>A common interview question for new software engineers is “what happens when you type in <a href="http://google.com">google.com</a> to your web browser?”. A seemingly simple exercize is actually hiding an incredibly complex process, most commonly explained by the <strong>Open Systems Interconnection (OSI)</strong> seven layer model for networks. In this conceptual framework, there are seven distinct layers ultimately connecting you (the user) to <a href="http://google.com">google.com</a>. Importantly, each layer has its own job, and each passes information to the next layer, transmitting and receiving data in some form or another. The seven layers are pictured below.</p>
<p><img src="https://lh3.googleusercontent.com/iMnsbSRP1rAS3MgO3u_A2BhOBz1OXgPNzhkd-Xi6awQnsktyU0Iulyark66HuXaHVOfWuSAj2G0" alt="source: https://www.webopedia.com/quick_ref/OSI_Layers.asp"> <em>need to make a lambda-approved graphic</em></p>
<p>Let’s take a look at the seven layers, broken into the ‘Application Level’ layers (5-7) and the ‘Moving Data around’ layers (1-4). If you’ve ever used the internet you are familiar with layer 7, the application layer, but the rest are equally important. Each device involved in the process of data transfer will go through these steps. Let’s explore what happens on the user end when you type in ‘<a href="http://google.com">google.com</a>’:</p>
<p><strong>Application Level</strong><br>
7. Application - the user puts a request for information into some friendly application.<br>
6. Presentation - Transforms and translates request data so it can be read.<br>
5. Session - Opens and maintains connection between user and receiving server.</p>
<p><strong>Moving Data Around</strong><br>
4. Transport - Data move from end to end, transfer is completed. (TCP, UDP).<br>
3. Network - Data moves through switching and routing pathways. (IP addresses).<br>
2. Data Link - Data is chunked into packets, encoded and decoded at switches within the local network.<br>
1 Physical - Data is converted to bits and sent through hardware, pins, volts, and cables through electricity.</p>
<p>A real life analogy might look something like this:<br>
<strong>Application Level</strong><br>
7. Write a letter in German for a Russian host.<br>
6. Translate letter into a universal language.<br>
5. Place letter in envelope and label sender/return address.</p>
<p><strong>Moving Data Around</strong><br>
4. Letter moves through international postal service.<br>
3. Letter moves around local Russian postal service.<br>
2. Letter is placed in Russian mailbox.<br>
1 Recipient reads letter.</p>
<p>It’s more complicated than it looks!</p>
<h2 id="we-do">We Do</h2>
<p>Okay, so that still doesn’t answer the question - what actually happens when you type in <a href="http://google.com">google.com</a>? Let’s synthesize those steps with a whiteboarding activity, and this time, consider both the transmission, and reciept of data. Keep this drawing handy, because you’ll need it again throughout the unit.</p>
<p><em>Instructor notes</em><br>
*Whiteboarding should walk through the 7 steps *</p>
<h2 id="you-do">You Do</h2>
<h2 id="additional-resources">Additional Resources</h2>
<ul>
<li>Blog: <a href="https://medium.com/learn-with-the-lean-programmer/osi-model-layers-explained-ee1d43058c1f">OSI Model Layers - “Explained”</a></li>
</ul>


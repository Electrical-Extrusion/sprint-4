---


---

<h1 id="objective">Objective</h1>
<p>Install a packet capture utility (wireshark) to capture and view packets on student’s local computer.</p>
<h2 id="instructor-notes">Instructor Notes</h2>
<p><em>Video for We Do is probably really important here</em></p>
<h2 id="required-resources">Required Resources</h2>
<ul>
<li>Software link: <a href="https://www.wireshark.org/download.html">Download Wireshark</a></li>
</ul>
<h2 id="i-do">I Do</h2>
<p>One tool security professionals use to make sure data is being transmitted securely is called a packet analyzer. Packet analyzers intercept and log traffic over a network, functioning in many ways like a microscope, to allow users to see what’s going on ‘under the hood’ of the internet. Today we will install a  popular and free packet analyzer called wireshark (linked in required resources above).</p>
<p>Once downloaded, we can look at the familiar packet details coming in and out of our local devices, including source IP, destination IP, length (in bytes), source port, destination port, payload data, and more.</p>
<p>In the ‘real world’ of cybersecurity, Wireshark is popularly used to diagnose network problems by locating the exact packets that are not properly transmitting.</p>
<h2 id="we-do">We Do</h2>
<p>Let’s download wireshark together and use it to finally figure out what happens when we type in ‘<a href="http://google.com">google.com</a>’.</p>
<ol>
<li>
<p>Download the stable release version for your OS .<img src="https://lh3.googleusercontent.com/90C_FSB0VJC6y3wJY3TCEsyh7XX1HxDaMk-VhJiYtSFE4YfXjyUI3MBZbHBnUMyBu2jMBDqL_4Y" alt="enter image description here"></p>
</li>
<li>
<p>Open the instaler and follow on-screen prompts<br>
<img src="https://lh3.googleusercontent.com/c7zrf23CYMID1YtgDdeOpJvqKOZG7YRJSGUp630N1u6fXjlguwD-JBMhmtT0iyZFmUS52Dk5h2Q" alt="enter image description here"></p>
</li>
<li>
<p>On the home screen, all network connections (wired, wireless, and external capture) are visible, like so: <img src="https://lh3.googleusercontent.com/g3S1RZdPUBUiv9CconEabQgG_SzMQvyGLUaCbJmyqSHHxROIx0qxPxmE9xPXRqsiWB9p9YaWFGA" alt="enter image description here"></p>
</li>
<li>
<p>Click the blue fin to begin capturing packet data:<br>
<img src="https://lh3.googleusercontent.com/jNPSyRABImjqZurXCpzdvF6LFcJSXnBxhz5KqX4y0xYBQEp7RJv1XKOm13N9lOSzTVjBJnRyR-c" alt="enter image description here"></p>
</li>
<li>
<p>You’ll notice data being captured right away, these are background tasks, open windows, network upkeep, and the like. To answer our question we will need to visit an internet browser and type ‘<a href="http://google.com">google.com</a>’.<br>
<img src="https://lh3.googleusercontent.com/UH0WFdg60NKDDZ9WdUHQp-_9_-YMQEzbcZESzoEZoHN1HUlidLmUpl5TFH5os-0JdM3TnZ7xd4I" alt="enter image description here"></p>
</li>
<li>
<p>Once <a href="http://google.com">google.com</a> has loaded, return to wireshark and stop the capture using the red square.<br>
<img src="https://lh3.googleusercontent.com/InG6MRduYa4jUKrwm2QgFaBXC9__XRi9vo3PONGTqHmJDSLvXQqJPB_UhcpFEnhSboSPnzBTBkI" alt="enter image description here"></p>
</li>
<li>
<p>We can now view all packet data, including familiar information like protocol, size, and IP addresses. Click on a packet to inspect data it carries. Since <a href="http://google.com">google.com</a> is a secure site using https/:/ we can’t make much of what we see. <img src="https://lh3.googleusercontent.com/TXlLQWRG5cs7UtA5g2yVvppyJKoARoJmh_cgzymxNJ4YDu0ibBMe1dAPG5Xqq3f0mjHttIE4GEQ" alt="enter image description here"></p>
</li>
<li>
<p>Analyze Data using the Statistics tool - the true power of wireshark comes in it’s ability to breakdown and analyze massive amounts of packet data. For now, we’ll just view the Capture File Properties.<br>
<img src="https://lh3.googleusercontent.com/7qb_r25BQyrmXdICWNNGKf3KDVa4nK22Fb80Kuhxc4XDoaO0I2_tBFwMrXJmTKzodQK3VOeTBSo" alt="enter image description here"><br>
<img src="https://lh3.googleusercontent.com/1Cdc5loX_z6dI1Qs0uHlQygK3M5lJp6d7s7P4fKN6AGgvZi35tttwxCE73KAEC9TxvyTLWAwkAg" alt="enter image description here"></p>
</li>
</ol>
<h2 id="you-do">You Do</h2>
<p>Use the statistcs tool to figure out the average packet size sent and recieved when trying to connect to different websites. Connect to at least 10 websites. Be prepared to come to class with your observations.</p>
<h2 id="additional-resources">Additional Resources</h2>
<ul>
<li>Official Documentation: <a href="%5Bhttps://www.wireshark.org/docs/wsug_html_chunked/%5D(https://www.wireshark.org/docs/wsug_html_chunked/)">Wireshark User’s Guide</a></li>
<li>Blog: <a href="https://www.varonis.com/blog/how-to-use-wireshark/">How to Use Wireshark</a></li>
</ul>


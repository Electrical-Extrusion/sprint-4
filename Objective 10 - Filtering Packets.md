# Objective

Filter packets by port, protocol, source, destination and subnet.

## Instructor Notes

Skills - students will be able to:

- A list of the DNS requests made by 172.16.1.126\
- A list of all DNS queries to domain names in Finland.

## Required Resources

## I Do

### Creating Filters

You can create filters in Wireshark two ways: using the visual interface, or using the built-in display filter language. We'll spend most of our time today focused on the written language, since it more directly translates to setting up on your own networks in bash (which you will do in Sprint 5).

First though, lets consider why filtering packet captures might be a helpful tool. As a cybersecurity analyst, you will be tasked with identifying suspicious network activity. By filtering a packet capture, you can hide 'normal' network activities to view undefined activity. Similarly, if a specific activity is defined, you can view only packet transmissions marked as suspicious.

You can filter a packet capture by any of the fields we've looked at so far. These include, but are not limited to port number, protocol, source, destination, and subnet.

Wireshark has a great user interface with built in tools to help users define filters. On any selected field in Wireshark, you can right click and "apply selected" as a filter. For example, if you wanted to view only HTTP packets, it would be as easy as finding a HTTP packet, right-clicking and applying the filter to 'selected.'

The same can be achieved by simply typing ```http``` into the expression bar and hitting enter. As you can see, this filter hides all packets that didn't use the HTTP protocol.
![Screen Shot 2019-10-21 at 10.47.14 AM](https://i.imgur.com/iCM4nJ0.png)

Similarly, you can use filters to view all coming from a specific source IP address using the label ```ip.src``` and ```==``` operator. That might look something like the below.

``` bash
ip.src==10.0.0.5
```

You can filter on any protocol Wireshark supports - over 2,000 protocols with almost 200,000 unique field labels. A full list of supported labels can be found in the Wireshark navigation menu under View -> Internals -> Supported Protocols. ![Supported Protocols](https://i.imgur.com/jscsg2l.png)

Beyond just 'is equal to' there are several ways to filter packets. Common display filter comparison operators should look familiar from Unit 1.

|English | C-like | Meaning | Example |
|--|--|--|--|
|```eq```|```==```|Equal| ```ip.src==10.0.0.5 ```|
|```ne```|```!=```|Not Equal| ```ip.src!=10.0.0.5```|
|```gt```|```>```|Greater Than| ```frame.len > 10```|
|```lt```|```<```|Less Than| ```frame.len ```|
|```contains```|n/a|Protocol, field or slice contains a value| ```sip.To contains "a1763"```|
|```matches```|```~```|Protocol, field or slice contains a value|```http.host matches "acme\.(org|com|net)"``` |
|bitwise_and|```&```| Bitwise AND is non-zero|```tcp.flags & 0x02```|

### Combining Expressions

Filters can also be combined using logical operators in English or C-like language; for example, and, or, xor, not, [...], and in. Note that both the English and C-like languages will work to generate a proper filter.

``` bash
tcp.srcport == 443 and ip.address ==  10.10.100.139
```

The above ```and``` works just like the ```&&``` below.

``` bash
tcp.srcport == 443 && ip.address ==  10.10.100.139
```

A full list of these operators can be found below.

|English | C-like | Meaning | Example |
|--|--|--|--|
|```and```|```&&```|Logical AND| ```ip.src==10.0.0.5 and tcp.flags.fin```|
|```or```|```||```|Logical OR| ```ip.src==10.0.0.5 or ip.src == 192.1.1.1```|
|```xor```|```^^```|Logical Exclusive OR| ```itr.dst[0:3] == 0.6.29 xor tr.src[0:3] == 0.6.29```|
|```not```|```!```|Logical NOT| ```not llc```|
|```[...]```|n/a|Subsequence| See slice operator below|
|```in```|n/a|Set Membership - Filter within a range of values.|```tcp.port in {80 443 8080}``` |

There are nearly infinite ways filters can be applied and combined to generate powerful analytical tools. In this week's sprint project you'll get to think like a professional cybersecurity analyst and get creative to find suspicious network activity.

## We Do

Filter a pcap stream for packets sourced at port number 443.

The first method we could use takes advantage of Wireshark's visual user interface. First, find a packet with the source port of interest. Then, right click and apply the selected port number as filter.

![Filter Packets Port 1](https://i.imgur.com/XxOxiPL.png)

The same process can be completed in the expression bar using the language learned above. To write this filter ourselves we need to know the label for port numbers, referencing the documentation we know that ```tcp.srcport``` will filter through TCP packets for a specified source port. To look at just those coming from a secure port, we would use ```tcp.srcport == 443```.
![Filter Packets Port 2](https://i.imgur.com/vHxcUic.png)

Next, we'll practice isolating our stream to the packets coming in and out of one computer. In order to do this we will need to combine expressions to view packets which match the specified IP address at either source or destination.

Again, this process can be effectively completed using visual interface, but we'll focus on utilizing the expression bar.

Let's say we wanted to target the IP address ```10.10.100.139``` - we would need to set a filter that shows all packets with ```10.10.100.139``` as the source or with ```10.10.100.139``` as the destination.

In order to do this we'll utilize the ```or``` operator and both ```ip.src``` and ```ip.dst```. While Wireshark command line is sensitive to capitalization, notice that it is not sensitive to spaces.

![Filter Packets Combined Expression](https://i.imgur.com/WbTlS2i.png)

## You Do

Use Wireshark to generate a list of all of the following.

- TCP packets coming from a secure (443) server.
- DNS requests made by your IP address.
- DNS queries to domain names in Cupertino, CA.

## Additional Resources

- Documentation: [Build Display Filter](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkBuildDisplayFilterSection.html)
- Wikiwireshark: [DisplayFilters](https://wiki.wireshark.org/DisplayFilters)
- Blog (Windows Interface): [Wireshark Display Filter Examples](https://www.thegeekstuff.com/2012/07/wireshark-filter/)
- Blog: [List of Wireshark Display Filters](https://networksecuritytools.com/list-wireshark-display-filters/)

# Objective

Extract URL information from HTTP stream.
Extract CGI metadata from HTTP stream.

## Instructor Notes

## Required Resources

## I Do

Until this point, we've focused heavily on the layers that make up a network. As a network security professional, you will need to not only understand these layers but also monitor your network for suspicious activity. 

The challenge for today will focus on utilizing packet sniffers to extract meaningful HTTP data from a .pcap session. Even encrypted packets contain, at the application level, URL information, file names, file types, and more. By aggregating and filtering this information, you can start to understand what is happening on your network.

### Extracting URL

As a cybersecurity analyst, you might want to identify threats to your network by looking at a list of previously accessed URLs. Packet analyzing tools can be used to look through HTTP streams and generate a list of all URLs accessed in any one period of time. Once network norms are established, these lists can be used to identify suspicious activity.

More than 99.5% of targeted fishing attacks begin with a cleverly disguised link in a spam email. Even though spam blockers filter out about 99% of those emails, if the malicious link finds its way to an employee inbox, there is about a 1 in 10 chance that the employee will click on it, opening up the network to malicious data transmission.

### CGI Metadata

Common Gateway Interface (CGI) is a protocol for web servers to move between what's done behind the scenes in command prompt and what a user sees in a dynamic application.

## We Do

### View all URLs accessed

You can use packet sniffers to view a list of all URL's accessed in a given file capture. You can also save this data for use in a later project or for additional filtering through a scripting software.  

1. File -> Export Objects -> HTTP
![enter image description here](https://lh3.googleusercontent.com/NaaRKH760WmicbwYadzCi-UFn_FyoInzcUoU-9ztSjstAer74ZVlph4xjTWbrWxRkhBlssiKK6XQ)
2. Wireshark wil generate a list with the hostnames of every HTTP request made during the file capture, and the type of content transferred. 
![enter image description here](https://lh3.googleusercontent.com/4ntuUWee_Pm3LP80PUiAqdSn5_BL8eNbM8G3lekF8s97RXyU9bYbZO08koGJxkpINNm9HimFdgTo)

### Use Wireshark to find all of the URLs requested from a specific website

There are some cases where you may want to find all of the URLs requested at a specific website, generating a list of every page accessed on that website. Wireshark has a built in tool that makes this fairly simple to do with an existing packet capture file.

1. Statistics -> HTTP -> Requests
![enter image description here](https://lh3.googleusercontent.com/zJY4n-0veK-35MAaWN6iETLctDwde4WQcL8BLTsnvjF7y4rAmfXrdtqayd-dxdynUlMuxsjW5fLa)
2. A window will pop up showing all of the HTTP requests made and categorize them by website. Here, you can see that the user visited a few pages on google.com, one page on facebook.com, and several on 'echoholidaydestinations.com'.
![enter image description here](https://lh3.googleusercontent.com/QIr1ri6gi0Kt4e84HCGFYDBO3h5cIetAqlHPoPKgITOspm7YGHQ-aJ3SSigU0M676Z2Ax7Y5ukbd)
3. You can also save this data for use in a later project or for additional filtering through a scripting software.  
![enter image description here](https://lh3.googleusercontent.com/kz2uhoNDBBRa8Ex8gp9alW-6VQ98MSyDoDWopyBtslOpK6fkF5_18Lxt2wfLWSchKQ-bVCXJoQ1u)

### Real File Name

1. File -> Export -> HTTP -> find pdf
![enter image description here](https://lh3.googleusercontent.com/If2wFeducWwoIyvEjKuk44ziA-olPcSEiruEZKaDW3ZeVSYI7o9J8lwZ7JDXSU1weg7o2PoUGaA_)
2. Double click packet
![enter image description here](https://lh3.googleusercontent.com/9Kd85Y7CKcXKNRVDQ741o84qIrd5oq_6DjSQhD7YZfrsIgXFvwF93J0oMdLghXQpAKBeOoG37jRD)
3. HTTP -> content-disposition: inline; look for filename. 
![enter image description here](https://lh3.googleusercontent.com/asKnHEexrNzeYzuMtn4vF744-qAywqmdBSdicONzfGu5lJOyMMZqmQ6MAQ-ytrSkxYrMc4sXw-yS)

## You Do

Use your packet analyzer to record a capture in which you access a website and download an image. Using wireshark, find the real file name for the image and verify using your downloaded file.

## Additional Resources

- Wikipedia: [Common Gateway Interface (CGI)](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

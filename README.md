# Wireshark Packet Analysis
Analyzing HTTP Packets using Wireshark tool.

<h1> Project Overview</h1>
In this project, I analyze basic information with a PCAP I captured while on a website using HTTP port: 80. I have been gradualy learning Wireshark, which is an important tool to use when analyzing network activity. I have been taking the time to study and understand what I am reading when given a PCAP.

The start of this project I went ahead and press start capture and enter the website httpforever.com.

![httpsforever](https://github.com/user-attachments/assets/1bb6398e-5f54-46fc-b13f-b2d94961e7fa)


Once I ended the capture, I had a ton of entries displayed on this PCAP that were other programs, such as Spotify, being captured as well. 

I wanted to just focus on my interaction with the httpforever.com site so I went ahead and used the filter ip.addr = = 146.190.62.39

146.190.62.39 is the IP address associated with the Domain Name. 

![Ipfilter](https://github.com/user-attachments/assets/391978f3-e84c-4f2d-9d9a-d47dd14d0b3c)

Alternatively, if I wanted to just see conversations with a specific port, I can use filter: tcp.port == 80 for HTTP.

![Ipfilter](https://github.com/user-attachments/assets/70fe210f-e8b7-47db-bfaf-bfbd181da3c2)

Now that I narrowed down the information I am looking for on this PCAP, I went ahead investigated the 3-way handshake under the TCP tab. Looking at the information, the site succesfully completed the 3-way handshake. 

![synack](https://github.com/user-attachments/assets/c6573118-5dc6-41ed-9c7a-5f93ea1a0e1f)

![Screenshot 2024-12-27 084745](https://github.com/user-attachments/assets/5de0a9a6-1a99-4d87-914d-a58f579c383f)

Wireshark has many tools to utilize when investigating pcaps to help narrow down conversations.

![Screenshot 2024-12-27 085339](https://github.com/user-attachments/assets/e882a95d-01bb-435a-8586-3de9244a64e5)


Hackers utilize tools like packet sniffers to investigate the traffic on a network and gather sensitive information on those packets. That is why employees or users should be more informed when navigating a website using port: 80 HTTP. Using specific filters, I can find inputted Username and Password information since port : 80 is not encrypted. It is safer to use Port: 443 HTTPS when inputting sensitive information, that is because port: 443 creates an encrypted tunnel during web sessions.

Wireshark is a great tool and I look forward to becoming an expert with it especially since I am working towards my career in Cybersecurity. At the moment, I know the fundamentals but would love to get better at identifying information over time. Right now, I am looking at the exercises provided on this site to improve my Packet Analyzing skills!

https://www.malware-traffic-analysis.net/training-exercises.html



# Introductory Networking

Difficulty: Easy

## Task 1 - Introduction

- Let's get started!

	  no answer needed

## Task 2 - The OSI Model: An Overview

- Which layer would choose to send data over TCP or UDP?

	- `4`

- Which layer checks received packets to make sure that they haven't been corrupted?

	- `2`

- In which layer would data be formatted in preparation for transmission?

	- `2`

- Which layer transmits and receives data?

	- `1`

- Which layer encrypts, compresses, or otherwise transforms the initial data to give it a standardised format?

	- `6`

- Which layer tracks communications between the host and receiving computers?

	- `5`

- Which layer accepts communication requests from applications?

	- `7`

- Which layer handles logical addressing?

	- `3`

- When sending data over TCP, what would you call the "bite-sized" pieces of data? 

	- `segments`

- [Research] Which layer would the FTP protocol communicate with?

	- `7`

- Which transport layer protocol would be best suited to transmit a live video?

	- `udp`

## Task 3 - Encapsulation

- How would you refer to data at layer 2 of the encapsulation process (with the OSI model)?

	- `frames`

- How would you refer to data at layer 4 of the encapsulation process (with the OSI model), if the UDP protocol has been selected?

	- `datagram`

- What process would a computer perform on a received message?

	- `de-encapsulation`

- Which is the only layer of the OSI model to add a trailer during encapsulation?

	- `data link`

- Does encapsulation provide an extra layer of security (Aye/Nay)?

	- `Aye`

## Task 4 - The TCP/IP Model

- Which model was introduced first, OSI or TCP/IP?

	- `tcp/ip`

- Which layer of the TCP/IP model covers the functionality of the Transport layer of the OSI model (Full Name)?

	- `transport`

- Which layer of the TCP/IP model covers the functionality of the Session layer of the OSI model (Full Name)?

	- `application`

- The Network Interface layer of the TCP/IP model covers the functionality of two layers in the OSI model. These layers are Data Link, and?.. (Full Name)?

	- `physical`

- Which layer of the TCP/IP model handles the functionality of the OSI network layer?

	- `internet`

- What kind of protocol is TCP?

	- `connection-based`

- What is SYN short for?

	- `synchronise`

- What is the second step of the three way handshake?

	- `syn/ack`

- What is the short name for the "Acknowledgement" segment in the three-way handshake?

	- `ack`

## Task 5 - (Networking Tools) Ping

- What command would you use to ping the bbc.co.uk website?

	- `ping bbc.co.uk`

- Ping muirlandoracle.co.uk
What is the IP address?

	- `ping muirlandoracle.co.uk`
	- `217.160.0.152`

- What switch lets you change the interval of sent ping requests?

	- `-i`

- What switch would allow you to restrict requests to IPV4?

	- `-4`

- What switch would give you a more verbose output?

	- `-v`

## Task 6 - (Networking Tools) Traceroute

- Use traceroute on tryhackme.com
Can you see the path your request has taken?

	no answer needed

- What switch would you use to specify an interface when using Traceroute?

	- `-i`

- What switch would you use if you wanted to use TCP requests when tracing the route?

	- `-t`

- [Lateral Thinking] Which layer of the TCP/IP model will traceroute run on by default (Windows)?

	- `internet`

## Task 7 - (Networking Tools) WHOIS

- Perform a whois search on facebook.com

	  no answer needed

- What is the registrant postal code for facebook.com?

	- `94025`

- When was the facebook.com domain first registered?

	- `29/03/1997`

- Perform a whois search on microsoft.com

	  no answer needed

- Which city is the registrant based in?

	- `Redmond`

- [OSINT] What is the name of the golf course that is near the registrant address for microsoft.com?

	- `Bellevue Golf Course`

- What is the registered Tech Email for microsoft.com?

	- `msnhst@microsoft.com`

## Task 8 - (Networking Tools) Dig

- What is DNS short for?

	- `domain name system`

- What is the first type of DNS server your computer would query when you search for a domain?

	- `recursive`

- What type of DNS server contains records specific to domain extensions (i.e. .com, .co.uk*, etc)*? Use the long version of the name?

	- `top-level domain`

- Where is the very first place your computer would look to find the IP address of a domain?

	- `local cache`

- [Research] Google runs two public DNS servers. One of them can be queried with the IP 8.8.8.8, what is the IP address of the other one?

	- `8.8.4.4`

- If a DNS query has a TTL of 24 hours, what number would the dig query show?

	- `86400`

## Task 9 - Further Reading

Links:
- [CISCO Self Study Guide by Steve McQuerry](https://www.amazon.co.uk/Interconnecting-Cisco-Network-Devices-ICND1/dp/1587054620/ref=sr_1_1?keywords=Interconnecting+Cisco+Network+Devices%2C+Part+1&qid=1583683766&sr=8-1)

- Read the final thoughts

	  no answer needed

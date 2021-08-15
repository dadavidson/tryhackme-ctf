# Wireshark 101

Difficulty: Easy

## Task 1 - Introduction

- Read the above and move on to Installation.

	  no answer needed

## Task 2 - Installation

- Read the above, and ensure you have Wireshark installed.

	  no answer needed

## Task 3 - Wireshark Overview

- Read the above and play around with Wireshark.

	  no answer needed

## Task 4 - Collection Methods

- Read the above and practice collecting captures, as well as understand the various capture techniques available

	  no answer needed

## Task 5 - Filtering Captures

- Read the above and understand the basics of packet filtering.

	  no answer needed

## Task 6 - Packet Dissection

- Read the above and move on to analyzing application protocols.

	  no answer needed

## Task 7 - ARP Traffic

- What is the Opcode for Packet 6?

	- `request (1)`

- What 4 packets are Reply packets?

	- Apply as filter: `arp.opcode==2`
	- `76,400,459,520`

- What IP Address is at `80:fb:06:f0:45:d7`?

	- The first found previously (``10.151.23.1`).

## Task 8 - ICMP Traffic

- What is the type for packet 4?

	- `8`

- What is the type for packet 5?

	- `0`

- What is the timestamp for packet 12, only including month day and year? note: Wireshark bases it’s time off of your devices time zone, if your answer is wrong try one day more or less.
	
	- `May **, 2013`

- What is the full data string for packet 18?

	- `08090a0b0c0d0e0f101112131415161718191a1b1c1d1e1f202122232425262728292a2b2c2d2e2f303132*********`

## Task 9 - TCP Traffic

- Read the above and move into Task 10.

	  no answer needed

## Task 10 - DNS Traffic

- What is being queried in packet 1?

	- `8.8.8.8.in-addr.arpa`

- What site is being queried in packet 26?

	- `www.wireshark.org`

- What is the Transaction ID for packet 26?

	- `0x2c58`

## Task 11 - HTTP Traffic

- What percent of packets originate from Domain Name System?

	- Into `Statistics` tab
	- `4.7`

- What endpoint ends in .237?

	- Into `Statistics` tab
	- `145.254.160.237`

- What is the user-agent listed in packet 4?

	- `Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.6) Gecko/20040113`

- Looking at the data stream what is the full request URI from packet 18?

	- `http://pagead2.googlesyndication.com/pagead/ads?client=ca-pub-2309191948673629&random=1084443430285&lmt=1082467020&format=468x60_as&output=html&url=http%3A%2F%2Fwww.ethereal.com%2Fdownload.html&color_bg=FFFFFF&color_text=333333&color_link=000000&color_url=666633&color_border=******`

- What domain name was requested from packet 38?

	- `www.ethereal.com`

- Looking at the data stream what is the full request URI from packet 38?

	- `http://www.ethereal.com/download.html`

## Task 12 - HTTPS Traffic

- Looking at the data stream what is the full request URI for packet 31?

	- Add the key as described.
	- `https://localhost/icons/apache_pb.png`

- Looking at the data stream what is the full request URI for packet 50?

	- `https://localhost/icons/back.gif`

- What is the User-Agent listed in packet 50?

	- `Mozilla/5.0 (X11; U; Linux i686; fr; rv:1.8.0.2) Gecko/20060308 Firefox/1.5.0.2`

## Task 13 - Analyzing Exploit PCAPs

- Read the above and analyze the PCAP yourself  to piece together the events that occurred.

	  no answer needed

## Task 14 - Conclusion

- Check out the provided links and keep learning!

	  no answer needed

Links:
- [https://dfirmadness.com/case-001-pcap-analysis/](https://dfirmadness.com/case-001-pcap-analysis/)


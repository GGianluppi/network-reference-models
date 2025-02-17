## Overview

In this guided exercise, I will explore the TCP/IP and OSI model layers using the Wireshark protocol analyzer. Wireshark displays encapsulated packet details in its Packet Details pane. However, it does not strictly conform to either the TCP/IP or OSI model, but instead uses a combination of both.

Notably, Wireshark combines OSI layers 5-7 (Application, Presentation, Session) into a single category while keeping layers 1-2 (Physical and Data Link) separate, rather than merging them into a Network Access layer as seen in the TCP/IP model.

Additionally, Wireshark displays encapsulated layers in an inverted order, with lower layers (Physical, Data Link) appearing at the top and higher layers (Application) at the bottom.


### 1. What channel is the Wireless Access Point broadcasting on in this capture?

  • First, I locate a Beacon packet in the Packet List pane.<br>
  • Then, I go to the Packet Details pane and expand the Radiotap Header v0 row.<br>
  • Next, I find and expand the 802.11 radio information row.<br>
  • Here, I look for the channel information.<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/fc360d67-d9f0-46ac-a70b-82111d81f70e">
</p>

  **Answer:** 36
  
  
### 2. What TCP port is the web server listening on (the receiver of the HTTP request) in this capture?

  • I locate an HTTP packet in the Packet List pane.<br>
  • I expand Internet Protocol Version 4 in the Packet Details pane to collapse it.<br>
  • Then, I expand the Transmission Control Protocol row.<br>
  • I look for the destination port, which is typically a well-known port for web servers.<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/49701592-dce7-4c41-b934-5672e3173540">
</p>

  **Answer:** 1337
 
### 3. What is the Network/Internet Layer address of the machine making an HTTP request?

  • I locate an HTTP request packet in the Packet List pane.<br> 
  • I select the second HTTP packet to view its details. <br>
  • I expand the Internet Protocol Version 4 section in the Packet Details pane.<br> 
  • Here, I identify the source IP address, which belongs to the machine making the request.<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/b613607d-ec78-4750-b03c-4534f08da7e3">
</p>

  **Answer:** 10.45.0.2

### 4. What is the flag discovered in the Application layer data returned by the web server?

  • I locate an HTTP response packet in the Packet List pane.<br>
  • I expand the Hypertext Transfer Protocol section in the Packet Details pane.<br>
  • Then, I find and expand the Line-based text data row.<br>
  • Here, I locate the flag<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/56abc36b-abfd-47a8-bc6e-91338d009c2e">
</p>

  **Answer:** {CLAB_C3RT}
 

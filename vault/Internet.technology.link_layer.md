---
id: 00H3cZGuU3AR2ZkUfbK6z
title: link_layer
desc: ''
updated: 1641558080204
created: 1641558025616
---

# Link Layer (or Physical Layer)
Deals with the problems connecting one computer to another computer. 
- Only worries about data across one **_hop_**. 
- Like what voltages to use, 
- How to send data. 
- How to deal with multiple computers using the same wire.

The tech that came out of this are
- Ethernet
- WiFi
- Cable Modem
- DSL
- Satellite
- Optical

#### Link Layer Addresses
All link devices like Wireless Modules have a specific address built into them by the manufacturer. **MAC Address**
> Q: How do we ensure that, in an environment where multiple devices are hooked to something like an Ethernet Hub or like a WiFi Network, if two devices want to talk to each other, they can so.

> A: The address of the sender and receiver is encoded into the packet

#### Avoiding Chaos
For Ethernet, it uses **Carrier Sense Media Access with Collision Detection (CSMA/CD):**

0. We have a data ready to go
0. "**_Listen_**". If there is already data being transferred, wait.
0. Once it goes silent, send.
0. Listen again to see if your own data is coming back. If so, great.
0. If a collision does happen, the data needs to back off. "[[Complex math|complex math]]" makes it so that fairness is maintained.


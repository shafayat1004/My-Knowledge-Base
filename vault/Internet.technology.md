---
id: SRJpDqbWI5BPydkk6Wal2
title: technology
desc: ''
updated: 1641324546358
created: 1641313602955
---

# Internet Technology

## Store and Forward Networking (BITNET)
The idea of hopping between computers. Queues were formed. If a computer was down, the messages would remain on the disk until the next computer was back up.

## Research Networks (1960s-1980s)
Packet Networks were used. 
- How to share one link so a long message doesn't block the flow?
- How to deal with outages more dynamically.

The goal was **Half a second** to send a message across US.

The 20 year period was about **Efficient Message Transmission** like perfecting **Packet Switching**.

## Packet Switching
> Q: How do we move data simultaneously?

> A: Break it into packets $\to$ label each packet for sequence $\to$ add a **to** and **from** address. 
> $\therefore$ the receiver has everything they need to reconstruct the message even if the packets don't arrive in sequence.

This lead to a shared network infrastructure where the computers no longer had to have lots of disk space or compute power. They only needed to forward packets. **A Router** 

$\therefore$ They only focus on packets. Not reliability.

## Layered Network Protocol
> This approach was taken to break the problem of designing a network into smaller subproblems.

|The Layers|
-
|Application Layer (Web, email, file transfer)|
|Transport Layer (TCP)|
|Internetwork Layer(IP)|
|Link Layer|

We currently follow the **TCP/IP** model.
Also existed was a 7 layer **OSI (Open System Interconnection)** model.

## Link Layer (or Physical Layer)
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

#### Internetwork Layer
It is the notion of forwarding each each of the packets with to and from addresses enough times so that the reach their destination.

The Link Layer only works on one link.
The Internet Layer worries about all the links and the proper sequence to follow to get from host to destination.

**We don't worry about reliability**

They introduce a new type of address **IP Address**.
>**IP Address:** It is the worldwide number which  is associated with one particular workstation or server. 

They are not controlled by a single organization. Address ranges are assigned. They are based on where the station is connected.

They [[change|Internet.technology.ip]] their addresses, get reorganized once a while.

**Routers** maintain **[[Router Tables|Internet.technology.ip]]** which are based on: 
- the destination network address
- bandwidth on adjacent links
- state of the neighbor nodes (up or not)
- .....
- .....
    
Routers use these to determine the best outbound route to each network number.
They are also dynamic in adjusting their best paths by "asking" other routers for the best path.
If they encounter a new Network Address, they can ask their neighbor routers and their neighbor routers for the information.

#### Problem of Computers that move around
> Q: How is it so that a single device can send and receive data from the Internet even if it changes Network Addresses when being in different places?

> A: When a device tries to enter a network, it asks for an IP address. The Access Point provides an IP address to the device that corresponds to the Network Address of the Access Point.

This is known as the **Dynamic Host Configuration Protocol (DHCP)**

**But there are a lot of devices!**

Don't fret for there are special addresses known as :

#### Non-Routable Addresses
Moving from one house to another, we see that our IP is typically 192.168.\*.\*.

- The ISP provides the home router a real global routable address.
- But the router gives out local addresses with 192.168 as suffix.
- This doesn't make sense in the internet and only the router knows what device the prefix maps to.
- When a home device needs to access the internet, the router/access point/base station changes the Network Address of the packet to the ISP provided, routable, one. 

This is done through a process called **Network Address Translation (NAT)**

#### Problem of packets cycling across routers infinitely
An improperly configured network of routers may cause packets to cycle through then indefinitely. Since the world of the router is narrow, it only determines which path is best to follow. So there is no way to tackle the fact that the packets may be cycling due to improper configuration.

**Solution:**
>**Time to Live (TTL):** is a number assigned to an IP Packet that goes down by one each time the packet passes through a router. Usually starting from a value of 25. Can start from 255.

The routers, when they encounter a packet with TTL 0 after decrementing, they throw the packet away.
**Then it sends a notification back to the sender indicating the packet was thrown away**

#### Traceroute
- Starts by sending a broken packet with a TTl of 1.
- First Router sends notification back
- Sends packet again with TTL of 2
- packet reaches second router and second router sends notification again.
- repeats until actual destination is reached
- $\therefore$ we can **trace** the **route** the packet took to reach the destination.

IP works through **Best Effort**. It tries to efficiently transfer packets.
**It does not guarantee delivery**.
But the flexible nature of it makes it so that its scalable to very large networks. Therefore "reliable"

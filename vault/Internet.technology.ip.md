---
id: oC7u1YeSbgDORb79xExMN
title: ip
desc: ''
updated: 1641576922858
created: 1641319146397
---

# Internetwork Layer (IP)
It is the notion of forwarding each each of the packets with to and from addresses enough times so that the reach their destination.

The Link Layer only works on one link.
The Internet Layer worries about all the links and the proper sequence to follow to get from host to destination.

**We don't worry about reliability**

They introduce a new type of address **IP Address**.
>**IP Address:** It is the worldwide number which  is associated with one particular workstation or server. 

They are not controlled by a single organization. Address ranges are assigned. They are based on where the station is connected.

## IP Address Format
- four numbers separated by dots.
- each number is 1 $\to$ 255, a 32-bit number
- broken into two parts:
    - Network Number (prefix), e.g 141.211.\*.\*
    - Computer Number (within the network) e.g \*.\*.144.188

When being packets are transmitted across the internet, only the prefix is looked at.
When it reaches the Station with the assigned network number, only then is the suffix looked at to send the packet to the actual computer.
    

They change their addresses, get reorganized once a while.

**Routers** maintain **Router Tables** which are based on: 
- the destination network address
- bandwidth on adjacent links
- state of the neighbor nodes (up or not)
- .....
- .....
    
<!-- ## Router Tables -->

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



---
id: SRJpDqbWI5BPydkk6Wal2
title: technology
desc: ''
updated: 1641566891458
created: 1641313602955
---

<!-- <style>
    .markdown-body{
        background-color: #FFFFDD;
        font-family:Latin-Modern;
    }
    h1,h2,h3,h4{
        text-align:center;
    }
    table{
        margin-left: auto;
        margin-right: auto;
    }
</style>

<div class="markdown-body"> -->


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
|-|
|Application Layer (Web, email, File Transfer) [[Internet.technology.application_layer]]|
|Transport Layer (TCP) [[Internet.technology.transport_layer]]. Reliable Connections|
|Internetwork Layer(IP) [[Internet.technology.ip]]. Simple, Scalable, Unreliable|
|Link Layer [[Internet.technology.link_layer]] (Ethernet, WiFi). Physical Connections|

We currently follow the **TCP/IP** model.
Also existed was a 7 layer **OSI (Open System Interconnection)** model.


## Domain Name System (DNS)
It converts user-friendly names like `www.umich.edu` to network-friendly names like `141.211.32.166`. 
It can be thought of as being in between the **[[IP|Internet.technology.ip]]** layer and the **[[Transport|Internet.technology.transport_layer]]** layer.
- IP Addresses reflect on technical "geography". Read left $\to$ right
- Domain names reflect on organizational structure. Read right $\to$ left.

So a Domain Name like `www.sets.iub.edu.bd` is read like:
In Bangladesh $\to$ an educational institution $\to$ IUB $\to$ SETS school of IUB $\to$ www, a particular server at the school.

Ownership of the Domain names are also right to left. 
Only the domain owners of `.edu` can decide who can use the name. Once they allow an organization to use it, like `.umich.edu`, committee within U Michigan can decide who can use their name. Once a school like School of Information requests for it, then they can use `.si.umich.edu`.


<!-- </body> -->


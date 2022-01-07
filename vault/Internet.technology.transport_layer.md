---
id: qKU8QoVj4cRq3osZ8yB8N
title: transport_layer
desc: ''
updated: 1641562024459
created: 1641558694574
---
# Transport Layer (TCP)

> **[[IP|Internet.technology.ip]]** makes it so that packets with to and fromm addresses can travel from one network to another through 5-20 hops by keeping track of the best paths to follow.

But there is no guarantee of delivery, if things go bad, the data vanishes.

This is where TCP comes in, to deal with such scenarios.
> **Purpose of TCP** is to compensate for the possible errors in the IP Layer and make best use of available resources.

It is built on top of IP.
The key thing it does is **keep a copy of the data** being sent **until** an **acknowledgement is received from the other end**.
Once that is received, only then the copy is thrown away.
If acknowledgement is taking too long, it sends the copy again.

One problem that was faced after it was first implemented was that packets were sent too slowly.
This was solved by [Van Jacobson](https://en.wikipedia.org/wiki/Van_Jacobson).


    
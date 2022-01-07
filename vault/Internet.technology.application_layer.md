---
id: iWfn8MMmzbBvOdallZAWH
title: application_layer
desc: ''
updated: 1641582433075
created: 1641561377966
---

# Application Layer

> **[[Link Layer|Internet.technology.link_layer]]** deals with how to transfer data with one hop and manage collisions.

> **[[Internet Layer|Internet.technology.ip]]** deals with the best way to move data across networks efficiently with multiple hops.

> **[[Transport Layer|Internet.technology.transport_layer]]** Deals with lost data by keeping copies of packets until it receives acknowledgement that a packet has been received successfully.

Having the technology of reliably transfer information lets us solve many problems like:
- Mail
- World Wide Web
- Video Streaming
- File Transfer
- .....


> Q: Which application gets the data?

> A: **Ports**. They allow a IP Address/Single Computer/Single Server to serve multiple services. The client can pick what services they want. Like a extension number in telephones.

Once a client selects a service, e.g the World Wide Web service, the client then needs to know the Application Protocol to talk to that service.

#### Ports
They are like telephone extension numbers.
While the Network Number in IP Addresses takes you to the LAN and the Host Number takes you to the destination machine, the port gets you to the specific application.

Some common ports include:

- Telnet (23) - Login
- SSH (22) - Secure Login
- HTTP (80)
- HTTPS (443) - Secure
- IMAP (143/220/993) - Mail Retrieval
- POP (109/110) - Mail Retrieval
- DNS (53) - Domain Name
- FTP (21) - File Transfer
- [Full List of TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)

#### Application Protocol
##### World Wide Web
The www clients (browsers) and the www servers communicate using [[HTTP|Internet.technology.application_layer.HTTP]] (Hypertext Transport Protocol).
It is used to retrieve HTML, Images, Documents, etc.
In addition to documents, RSS, Web Services, etc.

#### Summary
- We use a "pipe" abstraction where we can send and receive data on the same "socket".
- We can also add a security layer to [[TCP|Internet.technology.transport_layer]] using [[SSL|Internet.technology.transport_layer.SSL]] - Secure Socket Layer (aka TLS - Transport Layer Security).
- Port Numbers are used so that clients can find a particular application **within** a server. such as a mail server or web service, etc.

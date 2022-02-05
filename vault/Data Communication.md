---
id: Wmcrv6EMAzHxHPOY9Muwg
title: Data Communication
desc: ''
updated: 1643705348139
created: 1643699787707
---

For communication to happen, there needs to be **Data**, **Sender**, **Receiver**.

>**Simplex:** One directional data flow
```mermaid
graph LR
    Sender-->Receiver
```
>**Half-Duplex:** Two-Way communication but not at the same time.
```mermaid
graph LR
    A-->B
    B-->A
```
>**Full-Duplex:** Two-Way communication at the same time
```mermaid
graph LR
    A---B
```

### Effectiveness
- > **Delivery:** The data actually reaches its intended recipient.
- >**Accuracy:** The data received is not altered in any way.
- >**Timeliness:** The data reaches the recipient with an acceptable delay.
- >**No Jitter:** The data arrives all at the same time.

### Types of Connection
1. **Point-to-point:** 
    - Dedicated Link between two devices
    - The entire bandwidth is reserved for the two devices
1. **Multi-point:**
    - Multiple devices share a single link.
    - Bandwidth is shared. (Channels)?

### Physical Topology
#### Mesh Topology
```mermaid
graph LR
    A & B & C & D --- E
    A & C & D --- B
    A & D --- C
    A --- D
```
Each device is connected to all others through a point-to-point connection.
In this topology, $\frac{n(n-1)}{2}$ connections are required for `n` devices.
- Advantage:
    - If a connection is broken, all other devices can continue communication.
- Disadvantage:
    - A lot of wiring required.
#### Star Topology
```mermaid
graph TD
    HUB[[HUB]]---A
    HUB---B
    HUB---C
    HUB---D
```
- Advantage:
    - `n` connections/wiring required.
    - If a station/device is down, the network is intact.
- Disadvantage:
    - Centralized hub is a Single Point Of Failure. If it is down, the network breaks down.
#### Bus Topology
```mermaid
graph LR
    cable_start---tap_1([tap])
    tap_1---tap_2([tap])
    tap_2---tap_3([tap])
    tap_3---cable_continued
    tap_1---A
    tap_2---B
    tap_3---C
```
- Advantage:
    - `n` connections/wiring required.
    - If a station/device is down, the network is intact.
- Disadvantage:
    - The cable is still a Single Point Of Failure. If it is down, the network breaks down.
#### Ring Topology
```mermaid
graph LR
    A---B
    B---C
    C---D
    D---E
    E---A
```
- Advantage:
    - `n` connections required
    - If one device is down, the network is intact (Iff there is two-way communication).
- Disadvantage:
    - For One-Way Connections, if one connection is down, all devices cannot communicate.

### Hybrid
```mermaid
graph TD
    HUB[[HUB]]---tap_1([tap])
    tap_1---tap_2([tap])
    tap_2---tap_3([tap])
    tap_3---.
    tap_1---Device_A
    tap_2---Device_B
    tap_3---Device_C
    HUB---tap_4([tap])
    tap_4---tap_5([tap])
    tap_5---tap_6([tap])
    tap_6---..
    tap_4---Device_D
    tap_5---Device_E
    tap_6---Device_F
    HUB---tap_7([tap])
    tap_7---tap_8([tap])
    tap_8---tap_9([tap])
    tap_9---...
    tap_7---Device_G
    tap_8---Device_H
    tap_9---Device_I
```
### Network Criteria
>**Reliability:** Frequency of failure is minimal

>**Security:** 

>**Reliability:**

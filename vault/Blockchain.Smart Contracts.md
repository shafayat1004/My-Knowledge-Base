---
id: wP0TIxdGh6qyKbXlgi06p
title: Smart Contracts
desc: ''
updated: 1643016659663
created: 1643015078557
---
Smart Contracts allow people to engage in agreements without an intermediate third party or centralized governing force.

It was first proposed in 1994 by Nick Szabo.

These contracts are written in code.

Bitcoin also has smart contracts but **they are not [turing complete](https://stackoverflow.com/questions/7284/what-is-turing-complete)**. 
Ethereum is turing complete. [Not considering **Gas Limits???**]


### The Oracle Problem
Smart Contracts need real world data. But the [[determinism|Blockchain#Determinism]] of blockchains mean that there needs to be something that links outside world with Blockchain.
>**Oracles** are devices that bring data into a blockchain or execute some external computation.

Since the logic of Blockchains and Smart Contracts are Decentralized. Which means, to stay decentralized, they would have to get their data and perform external computations off-chain in a decentralized manner.

Combining the On-Chain and Off-Chain 

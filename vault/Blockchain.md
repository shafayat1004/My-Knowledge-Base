---
id: JA5NkomyZi5djSxGkwkGz
title: Blockchain
desc: ''
updated: 1644097216615
created: 1643014518434
---

### Bitcoin Blockchain
The [Satoshi Nakamoto White Paper](https://bitcoin.org/bitcoin.pdf) outlined how Bitcoin can be used to make P2P transactions in a decentralized network powered by cryptography. This allowed people to engage in censorship resistant finance.

There is a set amount of Bitcoin, making it scarce.

### Ethereum Protocol
It uses the same blockchain infrastructure but with additional features.

Using this, people can make decentralized applications/organizations. And make [[Smart Contracts|Blockchain.Smart Contracts]].

### Determinism
A "walled garden". Everything that happens in the blockchain happens inside it.

### Understanding Blockchains
First we need to know what [[hashing|Cryptography.Hashing]] means.

### A Block
A block consists of a **Nonce**, **Data**, **Hash**.
The Nonce is what the **Miners** have to find to solve a problem. Whenever a **node** mines a block, it gets paid. The problem can be anything. It can be a problem of finding a hash such that the first four values are `0000`.
The problems vary from blockchain to blockchain. The Nonce is the solution to the problem.

### A Blockchain
In a blockchain, in addition to the existing elements of a block, there is also an entry that stores the **Hash of the previous block**. Similar to a linked list.

Now, since hashes are unique for a specific given data, if any bad actor means to change the data in any previous block, the hash would change as well. And so, the blockchain will become invalid as the next block will be now referring to a hash that no longer exists.

So now, the bad actor has to change all the successive blocks' "previous hash" entry to make the chain valid. To do so, they must **mine** all the blocks again since the contents of the block has changed.

### Decentralized Blockchain
Even if the bad actor changes all the blocks and is able to make the chain valid, the decentralized nature of the blockchain means that they'd have to change the Blockchain in all other devices that have it. Which would be a hard thing to do.

So when one **peer** is corrupted, but the majority of peers are in sync (all have the same final hash), it would be easily known which peer was corrupted and then it would be considered an invalid from then on.

### Tokens
Instead of the abstract "data". We would have a **Transaction** section in the block.


|Block: 5|
|--------|
|Nonce: someNumber|
|Tx: list of some amount of money transfer from one person to another|
|Prev: hash of previous block|
|Hash: calculated/mined hash of this block|



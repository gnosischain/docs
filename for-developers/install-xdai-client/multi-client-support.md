---
description: Gnosis Chain is supported by OpenEthereum & Nethermind
---

# Multi-Client Support

A blockchain client is the software that runs on every node in the chain. It is responsible for connecting with other nodes, verifying transactions, and relaying and syncing blocks across the network. Some examples of popular Ethereum clients include [Geth](https://geth.ethereum.org/) and [OpenEthereum](https://github.com/openethereum/openethereum) (formerly Parity) and newer clients like [Hyperledger Besu](https://besu.hyperledger.org/en/stable/) and [Nethermind](http://nethermind.io/). If you want to run a blockchain node, you first need to setup a client on that node.

Ethereum clients are designed to implement the protocol correctly and support multiple consensus features. Each uses different methods to achieve this. The Gnosis Chain is an Ethereum-based stable sidechain with several unique consensus features in POSDAO, and client modifications are necessary for support. POSDAO consensus on GC can run with 2 open-source clients, **OpenEthereum and Nethermind.**

Gnosis Chain (then called xDai chain) was originally supported by Parity using the AuRa Authority Round consensus model. Parity is written in Rust, and recently transitioned to a DAO ownership model and rebranded as OpenEthereum. While Gnosis Chain with POSDAO uses the AuRa method to seal blocks in version 1, other changes were required to support validator selection, rewards, malicious reporting and other features in POSDAO. These were implemented in Parity stable version 2.7.2, then ported to the first OpenEthereum release 3.0+.

We've also collaborated with the Nethermind team to incorporate POSDAO consensus. The Nethermind client is written in .Net, and is fast, light-weight and user-friendly. POSDAO is now supported and [a majority of validators are running this client](https://dai-netstat.poa.network/).

Both clients fully support the underlying consensus, which is important for transaction verification and interoperability with the Ethereum Mainnet. Gnosis Chain offers 5 second blocks, and every transaction within a block is verified once the block is signed. The results of these transactions can then be immediately bridged to the mainnet with guaranteed accuracy. There is no need to wait for fraud proofs or other verification methods to interact with the Ethereum mainnet.

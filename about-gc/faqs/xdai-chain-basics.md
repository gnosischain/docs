# GC Chain Basics

## What is Gnosis Chain?

* Gnosis Chain was previously known as xDai Chain. Transactions on GC use the stable xDai token.
* Collaborators include [initial validators ](broken-reference)like MakerDAO, Gnosis, and SyncNode & [projects that support the ecosystem](../../for-developers/developer-resources/#dapp-management-and-developer-tools) like theGraph, Tenderly and AnyBlock Analytics.&#x20;
* Users are worldwide, from crypto veterans to first-time users.

## What is xDai?

* xDai is the name of the stable native coin that lives on the chain.&#x20;
* The xDai coin is used for stable transactions and low, stable fees. It can also be used to back on-chain tokens (use cases for this include [Event Currencies](../use-cases/cryptocurrency-for-events-and-conferences/) and [Community Currencies](../use-cases/community-currencies.md))
* The Gnosis Chain was previously called the xDai Chain.

## History?

* The xDai Stable Chain was [born in October, 2018](https://forum.poa.network/t/xdai-the-birth-of-the-stable-chain/2812). The name was changed to Gnosis Chain during a token merger (between the STAKE and GNO tokens) in December, 2021.
* POSDAO (Proof-of-Stake) consensus for selected validators was implemented April 1, 2020. It will continue until the merge of the Gnosis Chain and Gnosis Beacon Chain.

## How to Connect?

**Connecting to GC:**

* Network ID: 100&#x20;
* Primary RPC: [https://rpc.gnosischain.com](https://rpc.gnosischain.com)
* Explorer: [https://blockscout.com/xdai/mainnet](https://blockscout.com/xdai/mainnet)
* xDai Bridge: [https://bridge.xdaichain.com/](https://bridge.xdaichain.com/)

**Wallet Addresses:**

Since GC is an EVM chain, you can use the same wallet address you use for Ethereum and Ethereum testnets. Simply connect to the xDai network with your externally owned 0x address to get started.

## Why use GC?

GC supports a wide range of applications with low fees. GC transactions are fast, very inexpensive, and a stable token (xDai) is used for transactions.

The chain supports a decentralized, earth-friendly architecture with POSDAO consensus. It will transition to a mirrored beacon-chain environment with the planned [Gnosis Beacon Chain](https://www.gnosischain.com/) merge.&#x20;

## What is the TPS (transactions per second or tx/sec) for the GC?

It depends on the type of transaction being sent:

* Theoretical max: 119
* Standard txs: 70 tx/sec&#x20;

## Is the Gnosis Chain secure?

We have contracted 3rd party security firms to conduct [comprehensive audits ](../../for-developers/security-audits.md)on the xDai consensus, tokens, bridge and underlying architecture. We have resolved any issues they have found, and are committed to ongoing audits and comprehensive testing. However, we cannot anticipate all issues and users must assume risk when using any blockchain technologies.

## I accidentally transferred funds to a contract address - what should I do?

It depends on the nature of the contract. If you accidentally sent to a token contract on GC (for example [STAKE,](https://blockscout.com/xdai/mainnet/tokens/0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e/token-transfers) [LINK ](https://blockscout.com/xdai/mainnet/tokens/0xE2e73A1c69ecF83F464EFCE6A5be353a37cA09b2/token-transfers)or other bridged tokens), it may be possible for validators to retrieve these funds using the `claimTokens` functionality. However, this requires additional coordination and signature collection. **If we are able to claim, there is a 10% fee to claim your mis-sent tokens**.

If you accidentally sent to a contract, you can reach out to the [team on Discord](https://discord.gg/mPJ9zkq) to see if they can help you.

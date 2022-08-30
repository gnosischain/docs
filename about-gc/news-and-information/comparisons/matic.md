---
description: xDai & Polygon Differences and Similarities
---

# Polygon/Matic Network

{% hint style="warning" %}
Comparisons were completed when the chain was named xDai Chain. They are likely outdated as the Gnosis Chain pivots to a new Beacon Chain model.
{% endhint %}

|                                                 | xDai                                                                                                            | Polygon/Matic                                                                                                               |
| ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| 1. Chain Type                                   | Stable Chain (stable tx costs)                                                                                  | Volatile Chain (volatile tx costs based on market rate)                                                                     |
| 2. Token Structure                              | Dual token                                                                                                      | Single Token                                                                                                                |
| 3. Interoperability                             | xDai Bridge and OmniBridge                                                                                      | Plasma Bridge & PoS Bridge                                                                                                  |
| 4. Staking                                      | Staking Minimums, withdrawals after staking epoch (1 week)                                                      | No staking minimums, 21 day waiting period for validator exits                                                              |
| 5. Mainnet Launch                               | October 2018                                                                                                    | May 2020                                                                                                                    |
| 6. Block Time/TPS                               | 5 second blocks, 90 TPS with future scaling ability to meet demand                                              | 2 second blocks, 7000 TPS reported                                                                                          |
| 7. Block Gas Limit                              | 17M                                                                                                             | 20M                                                                                                                         |
| 8. Multisig for Bridge/Staking Contract Updates | <p><a href="../../../for-users/governance/#governance-board">7/13</a>*</p><p>2 addresses attributed to xDai</p> | <p><a href="https://docs.matic.network/docs/faq/commit-chain-multisigs/">5/8</a> </p><p>4 addresses attributed to Matic</p> |
| 7. Total Value Locked                           | [Dynamic](https://defipulse.com/xdai)                                                                           | [Dynamic](https://etherscan.io/address/0x40ec5b33f54e0e8a33a975908c5ba1c14e5bbbdf#tokentxns)                                |

_\*Updates in progress to add additional signers to bridge multisig._

## Similarities & Differences

### Similarities

As we compare chains, we see that xDai and Matic share several things in common:

1. Both are Ethereum-based Proof-of-Stake (PoS) sidechains designed to address Ethereum mainnet issues like slow transactions, high fees, and throughput concerns.&#x20;
2. Both are compatible with Ethereum 1.0, meaning smart contracts, tokens, and other functionality can be ported over from Ethereum with very few changes, and run with more efficiency.&#x20;
3. Both implement delegated staking.
4. Both chains incorporate multiple bridges for different use cases.

### Differences

Under the hood, the PoS consensus process between the two chains is quite different. Matic uses a plasma-based framework with Tendermint BFT consensus. xDai uses POSDAO with Authority Round consensus. xDai protocol follows the Ethereum patchset and is supported by 2 clients: Nethermind and OpenEthereum.

These different algorithms impact how each chain functions, but we will not go into the details here. Please see the links at the end of the article for more on the potential benefits and drawbacks of each.

Here we focus on key differences from a user perspective when interacting and or staking with Matic and xDai.

1. **Stable chain vs volatile chain**: xDai is a stable chain. Transactions as well as fees are paid with a stable token (xDai, which inherits the Dai peg to the US dollar). On xDai, buyers and sellers know that transactions retain their value, and developers and B2B operators can plan for costs related to micro-transactions. On Matic, users can send stable currencies but fees are still paid with MATIC tokens, and tx costs are unpredictable. \

2. **Single Token vs Dual Token structure.** The Matic token is used for both transactions and as a staking/delegation token. Token prices, supply, and market forces impact chain transaction prices as well as the underlying Proof-of-Stake consensus. The xDai chain separates these concerns, with a stable transactional coin and market-driven staking coin. The STAKE staking token is also a multi-chain staking token, and may be used for staking on other chains as well as for governance purposes and other utilities.\

3. **Asset transfers between chains:** Both chains are efficient when transferring assets from the Ethereum Mainnet, it takes a short amount of time to move ERC20 or ERC721 tokens from Ethereum to Matic or xDai.   In addition, both chains employ multiple bridges. Matic has recently introduced the[ PoS bridge](https://docs.matic.network/docs/develop/ethereum-matic/pos/getting-started) which provides faster transfers (with lower security guarantees) than the Plasma bridge, which requires a 7 day waiting period for withdrawals. The PoS bridge holds a vast majority of bridged assets on Polygon.\
   \
   The Matic POS bridge takes 10-30 mins to process a burn transaction. xDai transactions are typically finalized in 2-3 minutes.  \
   \
   xDai includes the xDai bridge for xDai <-> Dai transfers as well as the OmniBridge, where any ERC20 asset can be bridged immediately by anyone. While Matic's bridge also allows for asset transfers, users must request a specific asset be added to the setup through a mapping request. Both chains also allow for arbitrary messages (data calls) to pass between chains. \
   \
   The xDai bridge is more decentralized with additional bridge governors responsible for upgrades and bridge protection.   Currently, there is a [7/13 multisig on xDai with 2 project related signers and the remaining signers known and distributed](../../../for-users/governance/#governance-board). More signers are being onboarded to the xDai Governance Board in the near time. On [Matic it is a 5/8 multisig, with 4 known entities and 3 undisclosed](https://docs.matic.network/docs/faq/commit-chain-multisigs/).\
   \
   The xDai chain is currently researching an Optimistic OmniBridge model with plans to implement as an option for users in the future. [More info is available here](https://ethresear.ch/t/optimistic-bridge-between-mainnet-and-a-pos-chain/7965).   \

4. **Staking**: Both chains offer validator and delegated staking opportunities as well as a UI for staking. However, the functionality and underlying processes differ. With Matic, validators and delegators can stake with just 1 Matic token. Validators take a % of any delegators commission, and the reward pool of 1.2 Billion Matic tokens is designed to support the network for 5 years. After that time, rewards will transition to tx fees. Validators are chosen based on stake amounts, and when they want to exit the protocol, [must wait for 21 days before withdrawing their funds](https://docs.matic.network/docs/validate/validator/responsibilities).  \
   \
   xDai validators must have 20,000 STAKE in order to declare node candidacy, and delegators must have 200 STAKE. This makes potential collusion much more costly for any malicious actors. Validators do not charge commission, but are guaranteed 30% of staking rewards from their node. Reward emissions are created continuously as rewards and are based on how much STAKE is staked into the protocol. Validators can submit a withdrawal claim during a staking epoch (7 days) and can withdraw their funds once the epoch is over.  Since misbehavior is accounted for during the staking epoch, there is no need to wait for 21 days as with Matic to ensure there was no malicious activity. \

5. **Mainnet:** xDai has been in production since October 2018 and battle tested **** during that time. Security has been well tested in a live environment and xDai is a proven solution for scalability. Matic has been live since May of 2020, with less time in production.  \

6. **Transactions Per Second (TPS) and Block Times**. Matic processes 2 second blocks with a reported 7000 TPS (and theoretically up to 65,000 TPS). The xDai chain produces 5 second blocks with 90 transactions per second, which aligns with current transactional volume requirements. Gas limits have recently been increased from 12.5M per block to 17M per block to match increased user demand and reduce possible congestion. We believe in effective data and resource management where usage matches capacity, rather than an unnecessarily inflated TPS which can result in unmanageable state growth down the line.  xDai TPS is much faster than the Ethereum mainnet (15-20 TPS) and optimizations can be made to accommodate higher transaction rates as needed. The xDai chain is capable of scaling horizontally (by adding additional chains connected by bridges) or vertically (by optimizing node requirements).   Because the POSDAO Proof of Stake algorithm allows for a configurable consensus, there are plans to implement a HoneyBadger BFT consensus which will increase TPS by a factor of five. Additional research is being done around transaction prioritization, block parameter tuning and other optimizations to make sure tx capacity and usage requirements remain in alignment. We are also researching and applying state pruning techniques to ensure future data management capacity matches future usage.  _\*\*_\
   __
7. **Total Value Locked (TVL):** This is an ever changing proposition. Below we show ways to check the latest TVL.  **xDai:** The easiest way to find it on [BlockScout](https://blockscout.com/xdai/mainnet) where you can find the Marketcap. Hovering over the icon shows a breakdown of assets locked in the OmniBridge as well as Dai locked in the xDai Bridge. Below are contract which hold locked assets. \
   \
   xDai Bridge: [https://etherscan.io/address/0x4aa42145aa6ebf72e164c9bbc74fbd3788045016](https://etherscan.io/address/0x4aa42145aa6ebf72e164c9bbc74fbd3788045016) \
   OmniBridge: [https://etherscan.io/address/0x88ad09518695c6c3712AC10a214bE5109a655671](https://etherscan.io/address/0x88ad09518695c6c3712AC10a214bE5109a655671)

![](../../../.gitbook/assets/blockscout1.png)

**Matic:** Matic TVL can be viewed in their bridge contract address. [https://etherscan.io/address/0x40ec5b33f54e0e8a33a975908c5ba1c14e5bbbdf#tokentxns](https://etherscan.io/address/0x40ec5b33f54e0e8a33a975908c5ba1c14e5bbbdf#tokentxns)

## Chain Parameters / Features

| Component                              | xDai                                                                                                            | Matic                                                                                                      |
| -------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Mainet launch                          | October 2018                                                                                                    | May 31, 2020                                                                                               |
| Compatibility with Ethereum            | Following all Eth patchsets - Berlin HF complete                                                                | EVM compatible.                                                                                            |
| Client Support                         | Ethereum client support from 2 core clients - built into implementations for OpenEthereum and Nethermind        | Single client built on top of `geth` using `bor` consensus mechanism.                                      |
| Staking Token                          | STAKE                                                                                                           | MATIC                                                                                                      |
| Transactional Token                    | xDai stable coin                                                                                                | MATIC volatile coin - price impacts tx costs                                                               |
| Tx Stability                           | Stable                                                                                                          | Volatile                                                                                                   |
| Explorer                               | <p>BlockScout<br><a href="https://blockscout.com/xdai/mainnet">https://blockscout.com/xdai/mainnet</a></p>      | BlockScout [https://explorer.matic.network/](https://explorer.matic.network/)                              |
| Sidechain Structure                    | EVM sidechain: 100% Ethereum patchset                                                                           | Matic VM with More Viable Plasma                                                                           |
| Block Times                            | 5 seconds, 90 TPS (reported)                                                                                    | 2 seconds, 7000 TPS (reported)                                                                             |
| Asset withdrawal / Interoperability    | TokenBridge BiDirectional transfers                                                                             | <p>Matic PoS: 10-30 min withdrawals</p><p>Matic Plasma: 7 day withdrawal period from Matic -> Ethereum</p> |
| Sybil resistance                       |  Public delegated proof-of-stake                                                                                |  Public delegated proof-of-stake                                                                           |
| Consensus                              | AuRa, with roadmap to HBBFT                                                                                     | Peppermint (a forked version of Tendermint BFT)                                                            |
| Staking UI                             | Yes                                                                                                             | Yes                                                                                                        |
| Scalability                            | Horizontal (Additional chains) & Vertical (node scaling)                                                        | Horizontal (additional chains)                                                                             |
| Real World Use Cases                   | [Project / DApps List](../../project-spotlights/)                                                               | [Project/ DApps list](https://awesomepolygon.com/)                                                         |
| Meta-transactions                      | Yes                                                                                                             | Yes                                                                                                        |
| Validator / Delegator staking minimums | <p>20K STAKE Validator<br>200 STAKE Delegator</p>                                                               | 1 MATIC for either                                                                                         |
| Staking token emission                 | 8,765,000 STAKE + max 15% yearly emission                                                                       | 10,000,000,000 MATIC capped                                                                                |
| Micro transactions                     | Supported, costs in stable currency allow for accurate resource planning                                        | Supported, costs difficult to assess                                                                       |
| Randomness                             | Contained within the protocol                                                                                   | Oracle based                                                                                               |
| Wallet support                         | Multi-wallet support eg. Burner Wallet, Alpha Wallet, Nifty Wallet, Portis, Saturn, TrustWallet, Ledger, Trezor | Multi-wallet support eg. Matic Wallet, Atomic Wallet, Trust Wallet, Ledger, Trezor                         |

## Links:

* What is Matic Network: [https://medium.com/matic-network/what-is-matic-network-466a2c493ae1](https://medium.com/matic-network/what-is-matic-network-466a2c493ae1)
* Matic FAQs: [https://docs.matic.network/docs/validate/faqs](https://docs.matic.network/docs/validate/faqs)
* Matic Validator Staking: [https://docs.matic.network/docs/validate/validator/introduction](https://docs.matic.network/docs/validate/validator/introduction)
* Matic Validator Requirements: [https://docs.matic.network/docs/validate/validator/responsibilities](https://docs.matic.network/docs/validate/validator/responsibilities)

---
description: xDai Stable Chain and OMG Network comparison
---

# OMG Network

{% hint style="warning" %}
Comparisons were completed when the chain was named xDai Chain. They are likely outdated as the Gnosis Chain pivots to a new Beacon Chain model.
{% endhint %}

![](<../../../.gitbook/assets/Green and Black Corporate Comparison Chart.png>)

We’d like to talk about some of the key differences of some of our perceived competitors for a second layer solution to scaling Ethereum, while maintaining security. OMG network, a childchain of Ethereum, inherits the underlying security of Ethereum while allowing for faster and cheaper transactions. It uses More Viable Plasma construction to achieve this, yet lacks the flexibility and utility offered by xDai sidechains.

_Note: Comparison conducted 14 August 2020_

## Key Differences

|   | xDai                                                                                 | OMG                                                                                    |
| - | ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| 1 | Stable Chain                                                                         | Volatile Chain                                                                         |
| 2 | <p>500X+ cheaper than Ethereum</p><p>5X faster</p>                                   | <p>3X cheaper than Ethereum<br>100X+ faster</p>                                        |
| 3 | <p>Smart Contract Support</p><p>Tooling Support</p><p>Token Support (ERC721 etc)</p> | <p>Ether &#x26; ERC20 Support</p><p>No Smart Contract Support</p><p>No NFT Support</p> |
| 4 | <p>Standard Exit 2 minutes</p><p>No Exit Games</p>                                   | <p>Standard Exit 2 weeks</p><p>Exit Games</p>                                          |
| 5 | <p>In Production since 10/2018</p><p>Tx in last 24 hours: 20,000+</p>                | <p>Mainnet Beta 6/1/2020</p><p>Tx in last 24 hours: 20</p>                             |

1. **Stable vs volatile chains:** xDai, which is used to pay for fees in our network, inherits its value from the US dollar. Thus, all transactions through a buyer, seller, or even from an automatic contract perspective are infinitely more predictable versus a volatile payment token. We believe this creates a massive opportunity for planning a financial ecosystem related to micro-transactions (on-demand product usage, like streaming services, energy, etc), or even large scheduled services (regular remittances, such as paychecks, bills, dividends, and tax events therein).   Unfortunately, this is a major fault point for services offered by volatile chain solutions such as OMG, where fees are paid with their token, which can change value at any moment due to uncontrolled market forces. This creates unforeseen costs for all involved in real world applications, which can result in service slowdowns or passing costs along to customers.&#x20;
2. **Cost optimization:** While both chains offer the reduction of transaction costs, xDai achieves this at a significant advantage over its competitors. In brief, an Ethereum transaction costing approximately $5 would cost around $1.50 or so for OMG, whereas xDai is able to bring this cost down to less than $0.01, effectively reducing the cost of transactions by 500x.  **Speed:** xDai presents itself as a faster alternative to Ethereum while maintaining block and gas limit compatibility. We acknowledge that OMG is able to exceed our benchmarks considerably, however, this is still theoretical and not yet shown with real-world usage. Even so, xDai possesses horizontal and vertical scaling capability through chain addition, allowing it to meet much higher demands than our current estimates.&#x20;
3. **Token and Smart Contract Support:** Possibly the most powerful aspect that xDai maintains over its competition is its full compatibility with smart contracts on Ethereum, which can be directly imported to our network with little effort. ERC721s can also be bridged to xDai, as well as other token types. In doing so, the full Ethereum experience of niche currencies, dApps, finance protocols, games, DAO governance and more, can be integrated into xDai this very moment. Competitors such as OMG, however, are not designed to handle contract interactions, and thus are limited solely to payment operations.&#x20;
4. **2 minute exit vs 2 week exit**: Moving assets to either chain is easy. Moving them back to Ethereum is easy on xDai, and more difficult with OMG. Due to exit game challenge periods, OMG assets cannot be transferred back to Ethereum in a timely way. With the TokenBridge interoperability solution, tokens can be moved from xDai to Ethereum in minutes.&#x20;
5. **Production level quality vs an Open Beta:** One of our favorite aspects to flaunt about the xDai project is that we’re a proven, resilient, in-production solution for over two years! OMG makes their position clear as a disclaimer on their website: &#x20;

> **Please remember the OMG Network is in beta and may be subject to bugs or errors. The OMG Network team is committed to ensuring that these issues are resolved quickly. But we ask you to exercise caution and transact real value on the network at your own risk.**\
> \
> _Disclaimer from_ [_https://omg.network/omg-network-scales-ethereum/_](https://omg.network/omg-network-scales-ethereum/) _(bottom of page)_

Further, OMG’s own CTO Kasima has said:

> **As someone who’s running a business, I would be wary of anyone willing to put absolute faith in a research-grade solution or tool. There are a lot of unknowns, and it’s risky for customers.**\
> \
> _Quote from OMG AMA at_ [_https://omg.network/ama-30-omg-network-challenges/_](https://omg.network/ama-30-omg-network-challenges/)\_\_

Alternatively, we encourage you to stress test or push our network as hard as you’d like. We have been transacting real value on our network with good faith in a proven technology that’s been processing thousands of transactions a day. Whether it’s large scale or a micro-transaction, the thought of issuing a disclaimer or a word of caution such as those above hasn’t crossed our minds. No doubt, we’ve been live for two years, and haven’t had a problem since.

## Chain Parameters / Features

| Component                           | xDai                                                                                   | OMG                                                                                            |
| ----------------------------------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Mainet launch                       | October 2018                                                                           | June 2020                                                                                      |
| Compatibility with Ethereum         | 100%                                                                                   | Incomplete (no smart contract support, NFT support etc)                                        |
| Staking Token                       | STAKE                                                                                  | OMG (when launched)                                                                            |
| Transactional Token                 | xDai stable coin                                                                       | OMG volatile coin                                                                              |
| Explorer                            | [https://blockscout.com/xdai/mainnet](https://blockscout.com/xdai/mainnet)             | [https://blockexplorer.mainnet.v1.omg.network/](https://blockexplorer.mainnet.v1.omg.network/) |
| Chain Structure                     | EVM sidechain: 100% Ethereum patchset                                                  | Child chain with More Viable Plasma                                                            |
| Blocks                              | 5 second blocks, 70 TPS (reported)                                                     | Batched blocks, 1000+ TPS (reported)                                                           |
| Asset withdrawal / Interoperability | TokenBridge BiDirectional transfers                                                    | Exit games / Fraud Proofs                                                                      |
| Consensus                           | POSDAO/ AuRa  Roadmap to HBBFT                                                         | More Viable Plasma / AuRa                                                                      |
| Staking                             | EasyStaking available now, public POSDAO Q4                                            | Planned: Timeframe TBD                                                                         |
| Staking UI                          | Yes                                                                                    | No                                                                                             |
| Real World Use Cases                | Events, Conference Adoption, Burner Wallet, Community Currencies, DApps                | TBD Mainnet just launched  Tether Integration                                                  |
| Micro transactions                  | Supported, costs in stable currency allow for accurate resource planning               | Supported, costs 1/3 of Ethereum                                                               |
| Randomness                          | Contained within the protocol                                                          | Not within protocol                                                                            |
| Wallet support                      | Burner Wallet, Alpha Wallet, Nifty Wallet, Portis, Saturn, TrustWallet, Ledger, Trezor | OMG Web Wallet                                                                                 |

## Links:

* OMG childchain/sidechain comparison: [https://omg.network/plasma-childchain-sidechain/](https://omg.network/plasma-childchain-sidechain/)
* OMG AMA: [https://omg.network/ama-30-omg-network-challenges/](https://omg.network/ama-30-omg-network-challenges/)
* OMG Docs: [https://docs.omg.network/](https://docs.omg.network/)

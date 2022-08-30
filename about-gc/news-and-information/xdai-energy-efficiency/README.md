---
description: >-
  lab10Collective recently compiled energy usage stats for several blockchains
  as well as Visa.
---

# Energy Efficiency

In this article we present an overall energy usage overview (provided by [Lab10Collective](https://lab10.coop/)) of different blockchains as well as VISA. The data shows that the Gnosis Chain is extremely efficient while providing fast block times and a scaleable infrastructure.&#x20;

{% hint style="info" %}
This overview was done in 2020. In 2021 Energy Consumption for both Bitcoin and Ethereum has increased dramatically.

In addition, the chain was called xDai Chain at the time. It is now the Gnosis Chain.
{% endhint %}

![](../../../.gitbook/assets/energy-consumption.png)

## Energy Usage Overview

Energy usage equivalents (number of average US households consume the same amount of energy as the following chains/Visa). Note this figure is for 2020, **energy usage has increased dramatically for Ethereum and Bitcoin in 2021**.

| Chain / System              | # of US Households                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bitcoin                     | **5,250,408** :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: .......... |
| Ethereum 1.0                | **721,223** :homes: :homes: :homes: :homes: :homes: :homes: :homes: :homes: :house\_with\_garden: :house\_with\_garden: :house\_with\_garden: :house\_with\_garden:                      |
| Visa                        | **42,702** :homes: :homes: :homes: :house\_with\_garden: :house\_with\_garden:                                                                                                           |
| Ethereum 2.0 _\*speculated_ | **2,704** :house\_with\_garden:                                                                                                                                                          |
| Gnosis (xDai) Chain         | **2.1** :men\_with\_bunny\_ears\_partying:                                                                                                                                               |
| Artis                       | **0.8** :levitate:                                                                                                                                                                       |

## Bitcoin Footprints

A frequently mentioned concern about blockchain technology is energy consumption. Bitcoin is known to use incredible amounts of energy.  The annual footprint is alarming.&#x20;

![](../../../.gitbook/assets/bitcoin-1.png)

Ethereum currently consumes much less energy, but it is still equivalent to the energy needed to power 721,223 US homes. [https://digiconomist.net/ethereum-energy-consumption](https://digiconomist.net/ethereum-energy-consumption). This will change with Ethereum 2.0\*

![](../../../.gitbook/assets/ethereum.png)

Large centralized companies like VISA can process many transactions per second and require less energy: 42,702 US households. Keep in mind, however, this is just for transaction processing, not all of the power that VISA uses for things like offices, travel, banking infrastructure etc. Not to mention they are a giant centralized corporation that charges high transaction fees.

## Gnosis (xDai) Chain Efficiency

[lab10Collective](https://lab10.coop/), a project dedicated to a sustainable energy economy and also a validator, recently ran comparison data for their [Artis Chain](https://artis.eco/) and the xDai chain relative to other transaction processing chains/systems. They found that ARTIS and xDai are extremely efficient, consuming far less power than other chains as well as payment processing giant VISA.&#x20;

Efficiency is based on the number of operating nodes, hardware requirements, and TPS (Transactions per second) capacity.

The energy consumption required to run the ARTIS is equivalent to 0.8 US households annually. For xDai it is 2.1 households.  ARTIS is \~ 600x more efficient than Visa, and **xDai 300x+ more efficient than VISA**.

Visa does have a much higher TPS (7896 max vs 119 max for xDai) at them moment. If required however, xDai can scale to offer more TPS through bridging (horizontal scalability) or node improvements (vertical scalability). These solutions would slightly increase energy requirements, but these increases would be minor relative to VISA or POW blockchains. In addition, [HoneyBadger BFT](../../../for-validators/consensus/honeybadger-bft-consensus/) consensus will improve the TPS to 476 without vastly increasing the energy consumption per TX.

xDai is extremely efficient, and further decentralization with public POSDAO will improve security and usefulness for the chain.  &#x20;

## Energy Consumption Statistics

_Stats provided by Artis. Note that TPS capacity is the absolute max capacity with simple Txs, the actual TPS is considerably lower._

| TX Processor   | TPS Capacity | Tx / Yr                 | Energy Consumption kWh                           | Wh/Tx                                  | Wh/Tx Compared to Visa                                                                              | avg. # of US households                        |
| -------------- | ------------ | ----------------------- | ------------------------------------------------ | -------------------------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| Visa           | 7896         |      249,000,000,000    |                                 444,063,000      |                                 1.7834 |                                                                                                     |                                       42,702   |
| Bitcoin        | 3.5          |             109,500,000 |                            56,700,000,000        |                      517,808.2192      | <p>290351x worse<br>  <span data-gb-custom-inline data-tag="emoji" data-code="1f6d1">🛑</span> </p> |                                  5,452,447     |
| Ethereum       | 34           |          1,072,653,061  |                              7,500,000,000       |                          6,992.0091    | <p>3921x worse <br><span data-gb-custom-inline data-tag="emoji" data-code="1f6d1">🛑</span> </p>    |                                     721,223    |
| Ethereum 2.0\* | 2177         | 68,649,795,918          | 28,119,600                                       | 0.4096                                 | <p>4x better<br> <span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> </p>        | 2,704                                          |
| Gnosis (xDai)  | 119          |          3,754,285,714  |                                          21,900  |                                 0.0058 | 306x better :white\_check\_mark:                                                                    |                                           2.11 |
| ARTIS          | 95           |          3,003,428,571  |                                            8,760 |                                 0.0029 | <p>611x better</p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> </p>    |                                           0.84 |
| HBBFT          | 476          |        15,017,142,857   |                                          52,560  |                                 0.0035 | <p>510x better </p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> </p>   |                                            5.1 |

{% hint style="info" %}
\*Ethereum 2.0 will greatly reduce the Ethereum environmental footprint, although not enough is yet known to determine the total efficiency of the network. Numbers provided here are purely speculative. Lab10 estimates Eth2 will be similar to VISA in regards to energy consumption for transactions, but much more open and decentralized.  Also, VISA uses much more energy to fund their corporate enterprise vs minimal energy for a decentralized blockchain.
{% endhint %}

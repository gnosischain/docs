---
description: Dai is converted to xDai through the TokenBridge
---

# xDai Bridge: Dai to xDai

## xDai Bridge UI

{% hint style="success" %}
* [https://bridge.xdaichain.com/](https://bridge.xdaichain.com/)
* Additional bridge documentation is [available here](https://docs.tokenbridge.net/xdai-bridge/about).
* Quick video tutorial: [https://youtu.be/oKdh2cOOqUs](https://youtu.be/oKdh2cOOqUs)
* :question: Having issues? See our [troubleshooting guide](troubleshooting.md) or [FAQs](../../../about-gc/faqs/bridges-xdai-bridge-and-omnibridge.md) for more.
{% endhint %}

{% hint style="info" %}
There are currently multiple bridges on xDai with different purposes.

1. The xDai Bridge for converting xDai to Dai. This section covers this bridge
2. &#x20;The OmniBridge for bridging all other types of ERC20s. [Omnibridge section](../omnibridge/).
3. The [xDai - BSC Omnibridge](../omnibridge/binance-smart-chain-omnibridge/) for moving assets between these chains.
{% endhint %}

{% hint style="warning" %}
**Note: Transfers are non-reversible**. If you initiate and complete the first request transaction, you will need to complete the 2nd claim transaction at some time to receive your tokens on chain. This can be very expensive on Ethereum Mainnet. There is no time limit to complete the 2nd transaction - you can wait for gas prices to drop and claim at any time.
{% endhint %}

## What is the xDai Bridge

The [TokenBridge](https://docs.tokenbridge.net/) architecture is used to move and convert assets between chains.  With the xDai chain, the bridge converts Dai into xDai. Once converted, xDai is used as a native token (for transactions as well as transaction fees) on a chain where block times are fast and transactions are stable and extremely inexpensive. When a user is finished using xDai, they can convert it back to Dai using the same bridge.

The bridge uses smart contracts on both chains to process transfers, and a group of validators confirm bridge transactions. When a bridge transfer is initiated, the specified amount of Dai is locked in a smart contract on the Ethereum mainnet, and the same amount of xDai is minted on the xDai chain and sent to the user's wallet on the xDai chain.  When xDai is transferred back, xDai is burned, and the corresponding amount of Dai is unlocked in the contract and released to the user's wallet on the Ethereum mainnet.

The bridge mechanism ensures that the amount of xDai can never exceed the amount of Dai locked in the bridge contract.

## Dai/xDai Bridge Limits

| Type                 | Dai to xDai Bridge    | xDai to Dai Bridge |
| -------------------- | --------------------- | ------------------ |
| Daily Transfer Limit | 10,000,000 Dai        | 10,000,000 xDai    |
| Max Single Deposit   | 9,999,999 Dai         | 9,999,999 xDai     |
| Minimum Transfer     | 0.005 Dai             | 10 xDai            |
| Transaction Fees     | variable, paid in Eth | paid in xDai       |
| Transfer Fees        | 0%                    | 0%                 |

## User Interface

A simple UI allows for seamless transfers between chains. Instructions for [moving Dai to xDai](moving-dai-to-xdai.md) and [moving xDai to Dai ](moving-xdai-to-dai.md)are available.  The bridge can also be used without a UI, [instructions are available here](https://docs.tokenbridge.net/xdai-bridge/how-to-use-xdai-bridge-without-ui).

![](../../../.gitbook/assets/xDai-Bridge.png)


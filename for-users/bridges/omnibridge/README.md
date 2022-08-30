---
description: Cross Chain Bridge for Ethereum <-> GC and BSC <-> GC
---

# OmniBridge: ERC20 Token Transfers

## Basics

* Bridge any existing ERC20 between
  * **Ethereum and Gnosis Chain**
  * **Binance Smart Chain(BSC) and Gnosis Chain**
  * **POA Network and Gnosis Chain**
* The first time a token is bridged, a new ERC677 token contract is deployed on GC with an additional suffix to differentiate the token. It will say _token name on xDai_ as this was the original chain name..&#x20;
* If a token has been bridged previously, the previously deployed contract is used.&#x20;
* The requested token amount is minted and sent to the account initiating the transfer (or an [alternate receiver ](alternate-receiver.md)account specified by the sender).

{% hint style="success" %}
:bridge\_at\_night: OmniBridge is available at [https://omni.gnosischain.com](https://omni.gnosischain.com)\
\
&#x20;:link: Connect your wallet to the network you want to bridge from and set the chain to either ETH <-> GC,  BSC <-> GC or ETH <-> BSC from the dropdown menu. [Bridge Tutorial](https://honeyswap.org/xdai-bridges) _(refers to chain as xDai chain although name has changed to Gnosis Chain)_ \
\
&#x20;:stopwatch: Monitor the status of OmniBridge Transactions with the [ALM Monitor](https://alm-xdai.herokuapp.com/)
{% endhint %}

![](../../../.gitbook/assets/omni-UI.png)

1. **History**: See previous transactions and find claim functions for txs in progress.
2. **Settings**: Set custom RPCs, infinite unlocks and other settings.
3. **Bridge Selector:** change bridges to move assets between GC, Ethereum and BSC.
4. **Network Switch**: Click to switch network you are bridging to and from.
5. **Advanced Features**: Access the alternate receiver to bridge tokens to another address.

## **Features**

* [Alternate Receiver](../converting-xdai-via-bridge/alternate-receiver-send-dai-to-another-xdai-address.md): Bridge tokens from an address on one chain to a second address on another chain).
* [Define Custom RPCs:](set-custom-rpc-endpoints.md) Set your own RPC endpoints for bridge interaction.
* [Infinite Unlock](infinite-unlock.md): Approve all transfers of a token with a single tx rather than for each transfer.
* [Reverse Mode](reverse-bridging.md): Bridge tokens minted on xDai to Ethereum/BSC/POA

## Resources

* Video Tutorial - [Move STAKE between Ethereum to GC with the OmniBridge](https://youtu.be/qbuBqur9lcE)
* Instructions to [Bridge any ERC20 from Ethereum to GC](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension/ui-to-transfer-tokens/transfer-erc20)
* OMNI Bridged Token List on BlockScout: [https://blockscout.com/xdai/mainnet/bridged-tokens](https://blockscout.com/xdai/mainnet/bridged-tokens)
* OmniBridge Documentation Site: [https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension)
* 3rd party explainers
  * HoneySwap tutorials: Basics for swapping tokens and other information related to HoneySwap exchange - \
    [https://honeyswap.org/xdai-bridges](https://honeyswap.org/xdai-bridges)\
    [https://forum.1hive.org/t/1hive-101-beeginner-video-tutorials/217](https://forum.1hive.org/t/1hive-101-beeginner-video-tutorials/217)
  * Cross-Bridge Explainer by Yostari - [https://yostari.medium.com/traversing-the-eth-polygon-xdai-bsc-cross-chain-bridges-cfe3b29d49d4](https://yostari.medium.com/traversing-the-eth-polygon-xdai-bsc-cross-chain-bridges-cfe3b29d49d4)

{% hint style="warning" %}
**Transfers are non-reversible**. If you initiate and complete the first request transaction, you will need to complete the 2nd claim transaction at some time to receive your tokens on chain. This can be very expensive on Ethereum Mainnet. You can wait for gas prices to drop and claim at a later time if you like. In addition, MetaMask cost estimates may be inaccurate.

[**See this post for more information on the claims process and costs to claim**](https://forum.poa.network/t/request-and-claim-to-transfer-assets-from-xdai-chain/4495) **when transferring tokens from xDai to Ethereum using the OmniBridge.**
{% endhint %}

{% hint style="warning" %}
Note there are multiple bridges to Gnosis Chain, the OmniBridge is used for ERC20 cross-chain transfers. It is not used to mint Native xDai - to bridge Dai to xDai or xDai to Dai.\
\
**If you want to bridge xDai to Dai or vice versa, use the** [**xDai Bridge.**](../converting-xdai-via-bridge/)\*\*\*\*
{% endhint %}

---
description: Nethermind implements flashbots MEV  in v1.11.0
---

# MEV & Flashbots

## QuickStart

{% hint style="success" %}
💡 [This tutorial from Nethermind](https://medium.com/nethermind-eth/how-to-run-the-flashbots-auction-mechanism-on-nethermind-d6dd7b7b9962) includes all the information you need to get started with a flashbots MEV auction!

Considerations:

1. GC MEV Endpoint: **** [https://xdai-relay.nethermind.io](https://t.co/9X5lU6LWvr?amp=1) ****&#x20;
2. Tx chain id: **100**
3. Set appropriate gas price (gas in xDai not Eth)
4.  &#x20;Currently the **eth\_sendBundle** method is supported.&#x20;

    &#x20;eth\_callBundle is not supported, it will be implemented in a future release.
{% endhint %}

{% hint style="info" %}
If you are interested in decentralized trading with frontrunning protection, see [Cowswap](https://cowswap.exchange/#/swap), a Gnosis trading platform designed with MEV in mind.
{% endhint %}

## What is MEV

Miner - or Maximal - Extractable Value (MEV) refers to additional rewards block producers (miners or validators in xDai's case) realize by reordering transactions within a block. MEV incentives can increase chain congestion and gas prices as users and arbitrage bots compete for block space. In these scenarios, bots might continually submit txs with higher gas fees (bidding wars) in an attempt to capitalize on opportunities, and block producers will shift transactions to include txs with the highest gas prices first. &#x20;

Because transactions are viewable in the mempool before they are included in a block, MEV can also be used to frontrun certain transactions and opportunities.

For example, a user may locate a great arbitrage opportunity and submit a transaction. When the users sends the transaction, bots monitoring the mempool can see it before it is included in a block, create the same transaction with a higher gas price, and claim the opportunity for themselves.

To enable privacy, eliminate frontrunning, and reduce failed bids, Flashbots Auction uses a private transaction pool with sealed bids that other users cannot see before they are accepted. &#x20;

## Using Flashbots on xDai

* [Nethermind tutorial](https://medium.com/nethermind-eth/how-to-run-the-flashbots-auction-mechanism-on-nethermind-d6dd7b7b9962) to get started.\

* [Instructions for using the flashbots RPC endpoint](https://docs.flashbots.net/flashbots-auction/searchers/advanced/rpc-endpoint) to create and send transaction bundles are a good starting point. Note that the `eth_callBundle` method is not yet supported.\

* MEV Transactions can be bundled and sent to the Nethermind MEV relay on GC using the [https://xdai-relay.nethermind.io](https://t.co/9X5lU6LWvr?amp=1) endpoint. Validators running the Nethermind client on xDai will include these bundles if it is profitable for them. \

* MEV transactions are typically useful to maintain privacy or during times of increased congestion, such as a DarkForest Round. Use cases may include those using Perpetual Protocol and Dark Forest players. [This example shows an accepted bundle on BlockScout block 17663943](https://blockscout.com/xdai/mainnet/blocks/17663943/transactions). The first 2 included transactions were sent as a MEV bundle from 0x5b49B\

*   Other interested users may include the following as xDai chain usage grows (from the flashbots site).

    * Bot operators seeking fast, risk free access to blockspace.
    * DEX users looking for frontrunning protection on their transactions.
    * Dapps with use cases for account abstraction or gasless transactions.

    \
    See the [example searchers templates ](https://docs.flashbots.net/flashbots-auction/searchers/example-searchers/simple-arbitrage-bot)as a resource to begin creating your own.

## Additional Resources

* [Nethermind Discord](https://discord.com/invite/PaCMRFdvWT) for MEV Questions
* [Flashboys 2.0 paper that introduces MEV](https://ieeexplore.ieee.org/document/9152675)
* [Flashbots docs](https://docs.flashbots.net/)
* [Account Abstraction with Flashbots](https://medium.com/flashbots/flashbots-transparency-report-february-2021-8ac45b467d0a)

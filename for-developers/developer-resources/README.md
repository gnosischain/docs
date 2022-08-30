---
description: General Information and Links
---

# Developer Resources & Tools

{% hint style="info" %}
For assistance or questions please visit the [GC discord channel](https://discord.gg/mPJ9zkq).
{% endhint %}

## General Information

| Block Size | Block Speed | Gas price                                                | Patchset | Native token | Network ID |
| ---------- | ----------- | -------------------------------------------------------- | -------- | ------------ | ---------- |
| 30M Gas    | 5 sec       | \~1.22 GWei at baseline. Can rise with high usage (1559) | London   | xDai         | 100        |

## Blockchain Explorer

1\) **BlockScout** is the official blockchain explorer for the Gnosis Chain. With this full-featured, open-source explorer you can view transactions, accounts & balances, access data via the API, and read and verify smart contracts.

👉 [https://blockscout.com/xdai/mainnet](https://blockscout.com/xdai/mainnet)

2\) **AnyBlock Analytics Explorer** is convenient for exploring recent transactions and blocks and locating common information quickly**.**

👉 [https://explorer.anyblock.tools/ethereum/poa/xdai/](https://explorer.anyblock.tools/ethereum/poa/xdai/)

## JSON RPC endpoints

Main RPC is a load balancer with 4 nodes, health checks, and failover.

| Resource                | URL                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| JSON RPC endpoint(s)    | <p><a href="https://rpc.gnosischain.com">https://rpc.gnosischain.com</a><br><br><em>3rd party</em></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2714">✔</span><em>recommended</em> <a href="https://rpc.ankr.com/gnosis">https://rpc.ankr.com/gnosis</a></p><p><br><span data-gb-custom-inline data-tag="emoji" data-code="2714">✔</span><a href="https://gnosischain-rpc.gateway.pokt.network/">https://gnosischain-rpc.gateway.pokt.network/</a><br><br><span data-gb-custom-inline data-tag="emoji" data-code="2714">✔</span><a href="https://gnosis-mainnet.public.blastapi.io">https://gnosis-mainnet.public.blastapi.io</a></p> |
| WebSockets WSS endpoint | <p>wss://rpc.gnosischain.com/wss<br><br><em>3rd party</em><br><span data-gb-custom-inline data-tag="emoji" data-code="2714">✔</span><em>recommended</em> <br><em></em>wss://gnosis-mainnet.public.blastapi.io</p>                                                                                                                                                                                                                                                                                                                                                                                                                                      |

### **Additional resources to connect to Gnosis Chain**

| Resource                          | URL | Network ID hex |
| --------------------------------- | --- | -------------- |
| Network ID (Decimal, Hexadecimal) | 100 | 0x64           |

🚀 **QuikNode** supports GC. Devs can get their own custom endpoint for DApps or other needs. [https://blog.quiknode.io/xdai-network-is-live-on-quiknode/](https://blog.quicknode.com/xdai-network-is-live-on-quiknode/)

:anchor: **Ankr** offers API endpoint access available with a free tier up to 100K requests/day. Additional paid tiers are available for developers. [https://www.ankr.com/](https://www.ankr.com/)

:stop\_button: **GetBlock.io** provides fast and easy API connection services to a GC archive node. Both free and paid levels available. [https://getblock.io/nodes/stake](https://getblock.io/nodes/stake)

:earth\_americas: **AnyBlock Analytics** provides a JSON-RPC professional service for users. As GC validators, they have a deep understanding of the network as well as the broader Ethereum ecosystem. [https://www.anyblockanalytics.com/json-rpc](https://www.anyblockanalytics.com/json-rpc/?utm\_source=xDAI\&utm\_medium=Organic-Social\&utm\_campaign=forum)

:fast\_forward: **Pocket** decentralized infrastructure, 1-click endpoints and monitoring. [https://www.portal.pokt.network](https://www.portal.pokt.network/#1). Learn more about their [multi-chain infrastructure](https://www.blog.pokt.network/the-portal-to-private-multi-chain-infrastructure/).

:bomb:**Blast** infrastructure and dashboard for generating dedicated Gnosis Chain API endpoints. [Learn more here](https://medium.com/bware-labs/gnosis-support-added-in-blast-298590bbcc99).

### JSON-RPC Method Info

* Eth Wiki: [https://eth.wiki/json-rpc/API](https://eth.wiki/json-rpc/API)
* Postman: [https://documenter.getpostman.com/view/4117254/ethereum-json-rpc/RVu7CT5J?version=latest](https://documenter.getpostman.com/view/4117254/ethereum-json-rpc/RVu7CT5J?version=latest)
* BlockScout info
  * GraphQL: [https://blockscout.com/poa/xdai/graphiql](https://blockscout.com/poa/xdai/graphiql)
  * RPC: [https://blockscout.com/xdai/mainnet/api-docs](https://blockscout.com/xdai/mainnet/api-docs)
  * Eth RPC: [https://blockscout.com/xdai/mainnet/eth-rpc-api-docs](https://blockscout.com/xdai/mainnet/eth-rpc-api-docs)

{% hint style="info" %}
If using `eth_getLogs`to pull logs frequently WebSockets are recommended to push new logs as available.
{% endhint %}

### **Gas Price Oracle**

* Gas Price Oracle: [https://blockscout.com/xdai/mainnet/api/v1/gas-price-oracle](https://blockscout.com/xdai/mainnet/api/v1/gas-price-oracle)
* [More info & params](gas-price-oracle.md)

## POSDAO Contracts

POSDAO consensus is implemented in Solidity. Proxy contracts should be read for values such as [Random Numbers](../on-chain-random-numbers/) generated by the protocol.&#x20;

:white\_check\_mark: [List of current POSDAO contracts](https://github.com/poanetwork/poa-chain-spec/blob/dai/contracts.json#L9)

## TokenBridge

There are two bridge implementations connecting GC and the Ethereum Mainnet.

\*\*\*\*[**xDai Bridge**](https://docs.tokenbridge.net/xdai-bridge/about): ERC20-to-Native TokenBridge implementation, used for transferring Dai <-> xDai between Ethereum and the Gnosis Chain.

\*\*\*\*[**ETH-GC Arbitrary Message Bridge**](https://docs.tokenbridge.net/eth-xdai-amb-bridge/about-the-eth-xdai-amb): AMB between Ethereum and GC for data, token and message transfers. Includes the Ominibridge application for transfer of any ERC20 cross-chain.

#### xDai Bridge Access

* xDai Bridge UI at [https://bridge.gnosischain.com/](https://bridge.gnosischain.com/)
  * Interaction using method calls for smart contracts[ ](https://docs.tokenbridge.net/xdai-bridge/how-to-use-xdai-bridge-without-ui)[https://docs.tokenbridge.net/xdai-bridge/how-to-use-xdai-bridge-without-ui](https://docs.tokenbridge.net/xdai-bridge/how-to-use-xdai-bridge-without-ui)
* Bridge UI is built-in into AlphaWallet, BurnerWallet, BurnerFactory and other applications.

#### OmniBridge Access

* Omnibridge is located at [https://omni.gnosischain.com/](https://omni.gnosischain.com/). More information [including method calls here.](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension)

## Compatible Testnets

[POA Sokol Testnet](https://www.poa.network/for-developers/developer-resourses) is updated with similar specifications and runs the Nethermind Client.

## DApp Management & Developer Tools

{% hint style="info" %}
See the dropdown menu under Developer Resources and Tools for tutorials related to many of these tools.
{% endhint %}

* [Biconomy](https://medium.com/biconomy/biconomy-supports-xdai-chain-4d21d1f70222) allows for gasless transactions and improved DApp UX.
* [Gas Station Network](https://opengsn.org/) supports Gnosis Chain for Ethless Transactions.
* [TheGraph](https://thegraph.com) supports data indexing, querying and display.
* [CurveGrid MultiBaas](https://www.curvegrid.com/) provides smart contract deployment, interaction and updating capabilities through a web UI as well as a comprehensive REST API.
* [3Box](https://www.3box.io/):  Externally Owned Account (EOA) addresses are the same on GC as they are on other EVM networks, so no changes are needed to implement 3box functionality.
* [Blocknative](https://docs.blocknative.com/) supports real-time notification & transaction monitoring and mempool streaming with API and SDK tools.
* [Sourcify](https://sourcify.dev/) Smart Contract Source Verification. Contracts can also be verified with [BlockScout.](smart-contract-deployment.md)
* [Ethers.js](connect-to-xdai-with-ethers.js.md) lightweight javascript library - can be used as an alternative to [web3.js](https://web3js.readthedocs.io/en/v1.3.4/) for simple application development.
* [Remix IDE](https://remix-project.org/):  It's easy to deploy to GC with Remix, simply choose injected web3 and add the [GC custom RPC to your metamask](https://www.xdaichain.com/for-users/wallets/metamask/metamask-setup).
* [OpenZeppelin Defender: ](https://defender.openzeppelin.com/)Manage smart contract administration including access controls, upgrades, and pausing. Works with [Gnosis Safe](../../about-gc/project-spotlights/gnosis/gnosis-safe.md) Multisig.
* [Chainlink](https://docs.chain.link/docs/xdai-price-feeds): Price Feeds integration.&#x20;
* [Brownie](https://eth-brownie.readthedocs.io/en/stable/): Smart Contract Development tool suite. For a video overview of Brownie Features, see this [tutorial series by the Curve Finance team](https://www.youtube.com/playlist?list=PLVOHzVzbg7bFUaOGwN0NOgkTItUAVyBBQ).
* [Gelato](https://docs.gelato.network/introduction/readme): Automate smart contract executions with a decentralized network of bots.
* [Gnosis Safe](../../about-gc/project-spotlights/gnosis/gnosis-safe.md): Multisig management
* [Etherspot](https://docs.etherspot.dev/): Smart wallet SDK with multi-chain compatibility.

### **Dashboards & Monitoring**

* [Dune Analytics](https://www.duneanalytics.com/): Dune supports data queries and custom dashboards. Visualize and compare data between contracts and chains (GC and Ethereum support). Existing Dashboards:
  * [Staking Dashboard](https://duneanalytics.com/maxaleks/xdai-staking)
  * [Chain Usage Dashboard](https://duneanalytics.com/maxaleks/xDai-Usage)
* [Tenderly](https://tenderly.co/) dashboard supports transaction inspection - smart contracts can also be pushed to the dashboard for real-time monitoring.
* [Chainbeat](https://chainbeat.io/) provides monitoring and analytics tools for DApp developers.
* [Dappquery](https://dappquery.com/) analytics dashboard, customizable visualizations, smart contract alerts and scalable GraphQL API.

### **Token Faucets**

**Faucets for xDai transactions**

* Faucet #1 - [xDai, Optimism and Arbitrum on GC faucets](https://www.gimlu.com/faucet)
* Faucet #2 - [Stakely xDai Faucet](https://stakely.io/en/faucet/gnosis-chain-xdai)
* Faucet #3 - [Faucet for people with a verified BrightID ](https://unitap.app/)

**Test Token Faucets**

* [Token faucet](https://erc20faucet.com/) allows you to easily create ERC20 FAU tokens for testing purposes.
* [Weenus ERC20 ](https://github.com/bokkypoobah/WeenusTokenFaucet)is also available to use for testing purposes.

![Tenderly Dashboard Gas Profiler example](../../.gitbook/assets/tenderly.png)

## **Additional Resources**

* **General Migration Guide:** Published prior to the rebrand, this is a fun and easy xDai migration guide from DAOHaus: [https://medium.com/daohaus-club/daohaus-xdai-dapp-migration-83dca1fc590a](https://medium.com/daohaus-club/daohaus-xdai-dapp-migration-83dca1fc590a)
* **GasRelay tutorial** by Portis. With a few lines of code, gas fees are shifted to DApp owners rather than users, creating an intuitive user experience.\
  [https://docs.portis.io/#/gas-relay](https://docs.portis.io/#/gas-relay)
* **Chain** [**spec**](https://github.com/poanetwork/poa-chain-spec/blob/dai/spec.json) **files** and known [bootnodes](https://github.com/poanetwork/poa-chain-spec/blob/dai/bootnodes.txt) of the GC network\
  [https://github.com/poanetwork/poa-chain-spec/tree/dai](https://github.com/poanetwork/poa-chain-spec/tree/dai)
* **Netstats**, an overview of GC Chain nodes [http://dai-netstat.poa.network](http://dai-netstat.poa.network/)
* **Anyblock Index** (aka [http://eth.events](http://eth.events)), so you can query it via the Elasticsearch API or search in PostgreSQL: [https://account.anyblock.tools/status/](https://account.anyblock.tools/status/)
* **Gnosis Safe** [on GC.](../../about-gc/project-spotlights/gnosis/gnosis-safe.md)
* **Airdrops**: [Resources for creating airdrops](creating-airdrops/getting-airdrops/) on GC.

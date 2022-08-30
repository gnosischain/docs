---
description: Arbitrum Optimistic Rollup Deployment
---

# AoX: Arbitrum on GC

Arbitrum has been deployed to Gnosis Chain called **AoX**! This unofficial instance was deployed for research and development purposes, cultivating a broad ecosystem for  developers and users.

We are currently working on configs and bridge installation, [Blockscout is already configured for AoX](https://blockscout.com/xdai/aox/). Look for more info and instructions coming soon.

For information on Arbitrum and usage basics, see the [Arbitrum docs](https://developer.offchainlabs.com/docs/developer\_quickstart). Note that AoX is still being finalized, and some functionality is not yet available.&#x20;

## Basic Info

| Item                             | Value                                                                                                                                                                               |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RPC                              | [https://arbitrum.xdaichain.com/](https://arbitrum.xdaichain.com/)                                                                                                                  |
| WSS                              | [wss://arbitrum.xdaichain.com/wss](wss://arbitrum.xdaichain.com/wss)                                                                                                                |
| Chain ID                         | 200                                                                                                                                                                                 |
| Explorer                         | [https://blockscout.com/xdai/aox/](https://blockscout.com/xdai/aox/)                                                                                                                |
| Rollup Contract                  | [0xB17F1CaF8aceA14B9Bb877E67EAAde785E7D6F39](https://blockscout.com/xdai/mainnet/address/0xB17F1CaF8aceA14B9Bb877E67EAAde785E7D6F39/transactions)                                   |
| Inbox Contract                   | [0x9ab4bf8a231854ce5983c5fd69664859f717359d](https://blockscout.com/xdai/mainnet/address/0x9Ab4bf8A231854ce5983C5fd69664859F717359D/transactions)                                   |
| Outbox Contract                  | [0xD4319f5F233d907382911c5c3Ceea3cc68921c20](https://blockscout.com/xdai/mainnet/address/0xD4319f5F233d907382911c5c3Ceea3cc68921c20/transactions)                                   |
| Contracts version                | [7897c3](https://github.com/OffchainLabs/arbitrum/tree/7897c37760f38bd342a2c5d512fcfe74e082cf78)                                                                                    |
| Arb OS version                   | [48](https://github.com/OffchainLabs/arb-os/blob/7bfd973868c8a666fa51734c4cba5627df000f95/arb\_os/arbos.mexe)                                                                       |
| Sequencer/Validator docker image | [v1.0.0-2b628f8](https://hub.docker.com/layers/offchainlabs/arb-node/v1.0.0-2b628f8/images/sha256-be32b6cb1af726495bc40be5863931b145cb54b2ba5c95e3e4af950b19c23f38?context=explore) |

## MetaMask Custom Network

![](../../.gitbook/assets/xdai-arbitrum.png)

## Deposits to AoX

Simple deposit functionality for users / bridge implementation is still in development. Devs can use the following ABI to call the  `depositEth` method. Use 0 for `maxSubmissionCost` and attach an amount of xDai tokens to the transaction. It may take several minutes for execution finalization.&#x20;

* [Deposit Example Transaction](https://blockscout.com/xdai/mainnet/tx/0x2827e6b8c0c16b1a924910fb98488ebf2fb49303814773b252b16b7f67c0a83e)
* ABI :arrow\_down:&#x20;

```
[
  {
    "inputs":[
      {
        "internalType":"uint256",
        "name":"maxSubmissionCost",
        "type":"uint256"
      }
    ],
    "name":"depositEth",
    "outputs":[
      {
        "internalType":"uint256",
        "name":"",
        "type":"uint256"
      }
    ],
    "stateMutability":"payable",
    "type":"function"
  }
]
```

### BlockScout Deposit Example

1. Connect your wallet to blockscout.
2. Go to [the Write Proxy tab in the AoX Inbox contract](https://blockscout.com/xdai/mainnet/address/0x9Ab4bf8A231854ce5983C5fd69664859F717359D/write-proxy)
3. In the `depositEth` method
   1. Enter 0 for maxSubmissionCost field
   2. Enter the amount of xDai to deposit
   3. Click `Write` and confirm in MetaMask

![](<../../.gitbook/assets/bs-1 (1).png>)

{% hint style="success" %}
Once completed, it may take several minutes for the transaction to arrive at your address on the rollup. Switch to Arbitrum on xDai in Metamask to view the deposit.
{% endhint %}

### Withdrawals

_Instructions in process_

### Contract Deployment

#### Hardhat

To adjust deployment, simply use the xDai Arbitrum RPC url in your `hardhat.config.ts`:

```
module.exports = {
  solidity: '0.7.3',
  networks: {
    arbitrum: {
      url: 'https://arbitrum.xdaichain.com/',
      gasPrice: 0,
    },
  },
}
```

{% hint style="info" %}
For more info on Arbitrum and usage basics, please see the [Arbitrum docs](https://developer.offchainlabs.com/docs/developer\_quickstart). You can work with Arbitrum on xDai as you would on Ethereum.&#x20;
{% endhint %}

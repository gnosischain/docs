---
description: For Staking Utility and Governance
---

# POSDAO Staking and STAKE (archival staking method)

{% hint style="warning" %}
**Token Merger Completed**\
****STAKE to GNO swap has completed. xDai Chain is now Gnosis Chain. For further information, read more at: [https://www.gnosischain.com/evm](https://www.gnosischain.com/evm)

Info below and in this section is for archival purposes only. **DO NOT BUY OR TRADE FOR STAKE, IT IS NO LONGER ACTIVE FOR THE PROTOCOL.**
{% endhint %}

{% hint style="success" %}
STAKE token address on Ethereum [0x0Ae055097C6d159879521C384F1D2123D1f195e6](https://etherscan.io/token/0x0Ae055097C6d159879521C384F1D2123D1f195e6)

STAKE token address on xDai (STAKE from Ethereum)\
[0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e](https://blockscout.com/xdai/mainnet/tokens/0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e/token-transfers)
{% endhint %}

The STAKE token ([implemented as an ERC677](https://github.com/ethereum/EIPs/issues/677)) was designed to secure the on-chain payment layer and provide a mechanism for validators to receive multiple POS incentives. It was an ERC20-based staking token with a market driven value.

Users (stakers) provided STAKE as collateral when participating in the consensus process. In exchange for providing STAKE (and supporting a node), users received multiple rewards. The primary reward was in the form of additional STAKE tokens.

## Getting STAKE

There are [several ways to get STAKE](get-stake/) either on Ethereum or directly on GC.

## Staking STAKE

Individuals who own STAKE tokens on xDai (bridged from STAKE on Ethereum) can place them into the protocol through a [user friendly interface on BlockScout](https://blockscout.com/xdai/mainnet/validators). Functionality includes an [AMB Bridge extension](https://docs.tokenbridge.net/amb-bridge/about-amb-bridge) with the [OmniBridge U](../../../for-users/bridges/omnibridge/)I which allows users to move STAKE tokens between the Ethereum mainnet and the xDai chain.

In addition, exchanges may offer the opportunity to provide delegator staking on Ethereum directly from the exchange. Typically, this means STAKE holders select the option to stake the token, and the exchange processes the request (determining which validator to stake on, aggregating rewards and other tasks for a small percentage fee). Staking functionality is initiated by the participating exchange.

Validator candidates must meet certain requirements before placing STAKE (the ability to run a functional node and minimum STAKE amounts). Delegators can place additional STAKE on candidates and receive rewards when the candidates they have placed STAKE on are chosen as validators.

When STAKE is locked in the protocol, rewards for sealing blocks are generated in STAKE and xDai. In addition, fees for removing STAKE from the xDai chain are assessed and distributed among active stakers.

## STAKE Supply

The STAKE circulating supply is **decreasing due to the** [**STAKE/GNO swap**](stake-gno-swap.md)**. Supply does not include tokens sent to the following addresses** (burn or swap addresses). Current circulating supply can be queried at  [https://supply.xdaichain.com/](https://supply.xdaichain.com/). More details are also available at [https://www.coingecko.com/en/coins/stake#markets](https://www.coingecko.com/en/coins/stake#markets)

```
0x0000000000000000000000000000000000000000
0x0000000000000000000000000000000000000001
0x0000000000000000000000000000000000000002
0x00000000219ab540356cbb839cbe05303d7705fa
0x000000000000000000000000000000000000dead
```

## STAKE Governance Utility

Deprecated. GNO is now used for [community-based governance](../../../for-users/governance/community-governance.md).


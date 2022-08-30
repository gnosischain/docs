# STAKE Token Contracts

## Deployed STAKE Contracts

Contracts corresponding to STAKE and distribution roles have been deployed to the Ethereum Mainnet. All contracts are verified in Etherscan. Funds in contracts below are available according to the release schedule (e.g. a certain % is released each day).

The Distribution Contract is called with the corresponding number value below (e.g. 3 for private offering) to prepare/initialize funds for withdrawal. Once initialized, fund participants can pull available amounts to their wallets. See Private Investor claiming and Advisor claiming for details. All contracts below are on Ethereum mainnet with the exception of STAKE Token on xDai provided for reference purposes.

| Contract Type                                                                                                                           | Address                                                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **STAKE Token on Ethereum**                                                                                                             | [0x0Ae055097C6d159879521C384F1D2123D1f195e6](https://etherscan.io/address/0x0Ae055097C6d159879521C384F1D2123D1f195e6)                             |
| **STAKE Token on xDai (STAKE from Ethereum)**                                                                                           | [0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e](https://blockscout.com/xdai/mainnet/address/0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e/transactions) |
| <p><strong>Distribution Contract (DC)</strong><br><em>Prepares available withdrawal amounts in Investor/Fund Contracts</em></p>         | [0x9BC4a93883C522D3C79c81c2999Aab52E2268d03](https://etherscan.io/address/0x9bc4a93883c522d3c79c81c2999aab52e2268d03)                             |
| <p><strong>(3) Private Offering</strong></p><p>25% released at listing (492,737.75)<br>10% at day 28<br>65% daily for next 224 days</p> | [0x3cFE51b61E25750ab1426b0072e5D0cc5C30aAfA](https://etherscan.io/address/0x3cFE51b61E25750ab1426b0072e5D0cc5C30aAfA)                             |
| <p><strong>(4) Advisor</strong><br><em>Begins 84 days post listing Daily for 252 days</em></p>                                          | [0x0218B706898d234b85d2494DF21eB0677EaEa918](https://etherscan.io/address/0x0218B706898d234b85d2494DF21eB0677EaEa918)                             |

## Funds / Public Contracts

| Fund & Public Contracts                                                                                              | Address                                                                                                               |
| -------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| <p><strong>(1) Ecosystem Fund</strong></p><p><em>Begins 336 days post listing, continues daily for 336 days</em></p> | [0x5E78C09984bd6608f8E913F0924062C043eD6ad7](https://etherscan.io/address/0x5E78C09984bd6608f8E913F0924062C043eD6ad7) |
| <p><strong>(5) Foundation Reward</strong><br><em>Begins 84 days post listing, Daily for 252 days</em></p>            | [0x86edd0c110D1Fc7F8A5e1108623b3B1B4E3740f9](https://etherscan.io/address/0x86edd0c110d1fc7f8a5e1108623b3b1b4e3740f9) |
| <p><strong>(2) Public Offering</strong></p><p><em>100% released at listing</em></p>                                  | [0x0DF05ADaC0159e215111696339AD4998e5871B3D](https://etherscan.io/address/0x0df05adac0159e215111696339ad4998e5871b3d) |
| <p><strong>(6) Liquidity Fund</strong></p><p>100% released at listing</p>                                            | [0x0DF05ADaC0159e215111696339AD4998e5871B3D](https://etherscan.io/address/0x0df05adac0159e215111696339ad4998e5871b3d) |

## Burn Addresses

The STAKE circulating supply is **decreasing due to the** [**STAKE/GNO swap**](stake-gno-swap.md)**. Supply does not include tokens sent to the following addresses** (burn or swap addresses).&#x20;

|                       |                                            |
| --------------------- | ------------------------------------------ |
| Burn Address 1        | 0x0000000000000000000000000000000000000000 |
| Burn Address 2        | 0x0000000000000000000000000000000000000001 |
| Burn Address 3        | 0x0000000000000000000000000000000000000002 |
| Burn Address 4        | 0x000000000000000000000000000000000000dead |
| Eth2 Deposit Contract | 0x00000000219ab540356cBB839Cbe05303d7705Fa |

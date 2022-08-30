# Governance Board Summary of Decisions

The [Bridge Governance Board](./#bridge-governance-board) is responsible for enacting updates related to bridge functionality, contract upgrades, and other parameters impacting bridge operations. The following items have been implemented by the board.

## 2022

## Decrease OmniBridge withdrawal fee for GNO

:ballot\_box: **Justification:** Incentivize users to move operations to the Gnosis Chain

:white\_check\_mark: **Implemented:** January 17**,** 2022&#x20;

## Decrease OmniBridge withdrawal fee for WBTC

:ballot\_box: **Justification:** Reduce fees to 0 to attract participants to protocols on the Gnosis Chain.

:white\_check\_mark: **Implemented:** January 24**,** 2022&#x20;

## Increase gas limit to 4m gas for AMB messages

:ballot\_box: **Justification:** Necessary for Cow token deployment. Blocks can handle this capability with EIP1559 implementation.

​**​**✅ **Implemented:** January 30**,** 2022

## Rotate AMB validator

:ballot\_box: **Justification:**  Maintain active participation by rotating a signer address on the ETH-GC Arbitrary Message Bridge

:white\_check\_mark: **Implemented:** February 21**,** 2022&#x20;

## Update Governing Body

:ballot\_box: **Justification:**  Add additional governors to increase decentralization and remove several inactive validators. A series of related proposals accomplished the following:

* Removed 2 inactive governors, Burner Wallet and Request
* Added 3 new governors, KarpatkeyDAO, Cow Protocol and Gnosis Safe

:white\_check\_mark: **Implemented (in several txs):** March 26, 2022&#x20;

## Add Bridge Validator & Increase Requires Sigs

:ballot\_box: **Justification:**  Add an additional validator to xDai Bridge and AMB OmniBridge. A second proposal increased the number of signatures required for bridge execution.&#x20;

* xDai: 4/6
* AMB OmniBridge 5/8

:white\_check\_mark: **Implemented (in series of txs):** March 26**,** 2022&#x20;

## Decrease Daily Limit Amounts for Bridge Transactions

:ballot\_box: **Justification:**  Increase the bridge security by decreasing the allowable daily limits for the following assets:

* xDAI - 3’000’000 (4%)
* USDC - 2’500’000 (3%)
* USDT - 1’500’000 (4%)
* WETH - 250 (3%)
* WBTC - 2 (2.5%)
* GNO - 5’000 (2%)

:white\_check\_mark: **Implemented (in series of txs):** April 11**,** 2022&#x20;

## Interest Received by Bridge Compounding Redirected to KarpatkeyDAO

:ballot\_box: **Justification:**  As part of the agreement between xDai/Gnosis Chain token merge the interest received on bridged funds should be managed by KarpatkeyDAO.\\

:white\_check\_mark: **Implemented:** April 26**,** 2022&#x20;

## Update Bridge Validator Set

:ballot\_box: **Justification:**  Remove unresponsive validator and add new validators to both the AMB Omnibridge and xDai Tokenbridge.

* Removed 1 inactive validator, Mariano Conti
* Added 2 new validators, Cow Protocol and Gnosis Safe

:white\_check\_mark: **Implemented in batch:** May 01, 2022&#x20;

## Update Bridge Fee Receiver to GnosisDAO

:ballot\_box: **Justification:**  Bridge responsibility is migrating to GnosisDAO, and fees should be sent to a GnosisDAO owned safe.

* Added new fee recipient
* Removed existing recipient

:white\_check\_mark: **Implemented:** May 03, 2022&#x20;

## Update Bridge Fee Receiver to GnosisDAO

:ballot\_box: **Justification:**  Bridge responsibility is migrating to GnosisDAO, and fees should be sent to a GnosisDAO owned safe.

* Added new fee recipient
* Removed existing recipient

:white\_check\_mark: **Implemented in batch:** May 03, 2022&#x20;

## Increase Default Daily Limits of AMB Bridge&#x20;

:ballot\_box: **Justification:**  To support projects looking to move large amount of tokens from Ethereum to Gnosis Chain, increase the limits from 10^9 to 10^18 to enable transfer in a single tx.

:white\_check\_mark: **Implemented:** May 11, 2022&#x20;

## Increase Limits for **xDAI, USDC and USDT**&#x20;

:ballot\_box: **Justification:**  Due to market conditions, stablecoin bridge limits should be temporarily raised to ensure leveraged positions are not liquidated due to inability to bridge.

:white\_check\_mark: **Implemented:** May 12, 2022&#x20;

## **Remove Validator from the AMB Validator Set**&#x20;

:ballot\_box: **Justification:**  This odd-numbered validator run by the xDai team is redundant and should be removed from the set.

:white\_check\_mark: **Implemented:** May 24, 2022&#x20;

## **Decrease Withdrawal Fee on OmniBridge for CommonGround**

:ballot\_box: **Justification:**  The Common Ground token withdrawal fees should be set to 0 when bridging from Gnosis Chain to Ethereum to help promote adoption.

:white\_check\_mark: **Implemented:** May 30, 2022&#x20;

## Swap Governance Account Address

:ballot\_box: **Justification:**  Account for the former xDai team needs to be updated in the Governance Gnosis Safe.

:white\_check\_mark: **Implemented:** June 03, 2022&#x20;

## Disable Deposit Function in StakingAura POSDAO contract

:ballot\_box: **Justification:**  Staking is deprecated in POSDAO. Current validators will continue until the Gnosis Chain <-> Gnosis Beacon Chain merge but no new deposits are allowed.&#x20;

:white\_check\_mark: **Implemented:** June 14, 2022&#x20;

## Remove Former xDai Team Validators from AMB & xDAI Bridges

:ballot\_box: **Justification:**  xDai validators were important at the early stages of the project to ensure operational execution and bridge functionality. Now, with increased community involvement and ecosystem maturity, the next step is to further decentralize processes and remove the former xDai team.

:white\_check\_mark: **Implemented:** June 14, 2022&#x20;

## 2021

## Add Syncnode as Governor / xDai Bridge Oracle

:ballot\_box: **Justification:**  Increase decentralization by extending the governance and the bridge validators set to include Syncnode.

:white\_check\_mark: **Governor Set Implemented:** January 22, 2021 \
:white\_check\_mark: **Oracle Implemented:** January 7, 2021&#x20;

## Upgrade Bridge Contracts

:ballot\_box: **Justification:**  A number of updates were made to the contracts to facilitate user engagement, support costs for xDai transfers, and provide logic for rebasing tokens. The minimum amount per token transaction was reduced to 1 wei (primarily to support LP tokens or other token fractions) and fees were set to 0.1% for xDai to Dai transfers.

:white\_check\_mark: **Implemented:** March **** 15, 2021&#x20;

## **Return user funds**

:ballot\_box: **Justification:**  A user accidentally [sent over 2000 USDC ](https://blockscout.com/xdai/mainnet/tx/0x2837cd89972f2e37a1cb631e60dbb761213010fe526a089c99f48ed483f63956)to the USDC token contract on xDai. After confirming the users identity, the board agreed to call the `claimTokensFromTokenContract` method and return the amount to the user.&#x20;

:white\_check\_mark: **Implemented:** April 15, 2021

## Reduce USDC withdrawal fees to 0 for 3 months&#x20;

:ballot\_box: **Justification:** Current exit fees for USDC transfers on OmniBridge are currently 0.1%. The primary purpose of this temporary 3-month reduction to 0 fees is to attract more protocols utilizing USDC and OmniBridge for their activities.

:white\_check\_mark: **Implemented:** June 15, 2021&#x20;

## Increase finalization time on Ethereum Mainnet

:ballot\_box: **Justification:**  \
Increase the amount of blocks required for confirmation on the Ethereum Mainnet to 20, increaseing bridge operation reliability and security (less chances for re-orgs). This update slightly delays user transfers from 2.5 minutes to \~4 minutes.

:white\_check\_mark: **Implemented:** August 20, 2021&#x20;

## Add 01Node & Peerion Representatives to the Governance Board

:ballot\_box: **Justification:**  Increase decentralization by extending the governance and the bridge validators set.

:white\_check\_mark: **Implemented:** September **** 22, 2021&#x20;

## Add 1Hive Representative to the Governance Board

:ballot\_box: **Justification:**  Increase decentralization by extending the governance and the bridge validators set.

:white\_check\_mark: **Implemented:** October **** 04**,** 2021&#x20;

## Upgrade Bridge Contracts

:ballot\_box: **Justification:** Add new functionality including increased AMB request ability, contracts to send requests, and fix a security vulnerability identified through the Bug Bounty program.

:white\_check\_mark: **Implemented:** October 4**,** 2021&#x20;

## Include Compounding for xDai Bridge

:ballot\_box: **Justification:** Add compounding to support bridge operations. [Details here.](../bridges/converting-xdai-via-bridge/dai-compounding.md)

:white\_check\_mark: **Implemented:** October 6**,** 2021&#x20;

## Update Contracts

:ballot\_box: **Justification:** Last in a series of upgrades to allow reverse bridging and deploy  contracts included in the Chainsecurity audits.

:white\_check\_mark: **Implemented:** October 15**,** 2021&#x20;

## Increase finalization time to 20 blocks

:ballot\_box: **Justification:** To increase security, finalization time on the xDai chain for the xDAI TokenBridge and for the ETH-xDAI Arbitrary Message Bridge increased to 20 blocks from previous 8-12.

:white\_check\_mark: **Implemented:** October 18**,** 2021&#x20;

## Add Tornado cash contracts to Omnibridge forwarding rules manager

:ballot\_box: **Justification:** Add Tornado Cash contracts for proper routing and subsidized exits. This was done in several transactions from Oct 27 to Dec 10 to account for all contract functionality.

:white\_check\_mark: **Implemented:** October 27**,** November 9**,** 2021,  November 15, 2021, December 10, 2021.

## Decrease OmniBridge withdrawal fee for WETH

:ballot\_box: **Justification:** Incentivize users to move operations to the Gnosis Chain

:white\_check\_mark: **Implemented:** December 03**,** 2021

## Adjust Perpetual Finance contract auto-execution functionality

:ballot\_box: **Justification:** Perpetual Finance is no longer subsidizing transaction for users - users will need to deposit/withdraw/ and pay tx fees themselves. The bridge no longer needs to auto-execute transactions for this contract.

:white\_check\_mark: **Implemented:** December 22**,** 2021&#x20;

##

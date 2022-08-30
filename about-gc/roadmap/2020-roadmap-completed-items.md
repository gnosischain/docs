# 2020 Roadmap (Completed Items)

{% hint style="warning" %}
The xDai project roadmap is a high-level strategic plan designed to guide xDai research and development. Target dates and details are reviewed regularly and subject to move, adjust and change as the project evolves. Note that only completed items ( :white\_check\_mark: Status: Complete) are considered achieved project milestones.
{% endhint %}

## :white\_check\_mark: Completed 2020

## Fiat to xDai Onramp

****:dart: **Target:** Q4 2019\
&#x20;:white\_check\_mark:**Status:** [Ramp integration](../../for-users/get-xdai-tokens/buying-xdai-with-fiat/ramp-network.md) completed 2020. Includes support for 40+ countries, additional integrations and US support will continue to be explored

In order to offer options for users, xDai should be available for direct purchase. Prior to a fiat gateway, the primary method for users to get xDai is to get Dai first and relay it to xDai via the xDai Bridge. The process can be complicated and time-consuming due when Ethereum is congested.

The xDai team is working with payment processing companies to enable one or several Fiat to xDai onramps.&#x20;

## **Multi-Collateral Dai <-> xDai Bridge**

:dart: **Target Date:** Q4 2019\
:white\_check\_mark:**Status**: Complete. Summary: [https://forum.poa.network/t/migration-of-the-xdai-tokenbridge-completed/3212](https://forum.poa.network/t/migration-of-the-xdai-tokenbridge-completed/3212)

{% hint style="success" %}
xDai bridge is upgraded to support both Dai and Sai.

Bridge balance migrated from Sai to Dai. Both Dai and Sai can be deposited on the Ethereum side. Sai to Dai converted automatically.

_Update 4/15/2020: With the impending Sai shutdown, Sai transfers are no longer allowed on the bridge._ [_https://metamask.zendesk.com/hc/en-us/articles/360020394612-How-to-connect-a-Trezor-or-Ledger-Hardware-Wallet_](https://metamask.zendesk.com/hc/en-us/articles/360020394612-How-to-connect-a-Trezor-or-Ledger-Hardware-Wallet)__
{% endhint %}

## Chai <-> Dai Bridge Contracts Update

:dart: **Target Date:** Q1 2020\
:white\_check\_mark:**Status**: Completed 03/31/2020

{% hint style="info" %}
This feature has been deprecated. The governing board may revisit at a later time or look to introduce another mechanism for incentivization.\
\
[Proposal and Decision](https://forum.poa.network/t/disable-chai-token-support-to-safe-gas-for-deposit-and-withdrawal-operations/3936)
{% endhint %}

{% hint style="success" %}
Bridge contracts are upgraded and functional. For more on _**`CHAI,`**_ see the [Chai FAQs](../../for-stakers/staking-with-gno-on-the-gnosis-beacon-chain/stake-token/stake-reward-mechanics/xdai-rewards/chai-faqs.md).
{% endhint %}

The new version of the bridge contract supports usage of [the Dai Savings Rate contract](https://community-development.makerdao.com/makerdao-mcd-faqs/faqs/dsr) through [the Chai token](https://chai.money/) to earn the interest for tokens deposited on the bridge balance. Dai locked in the bridge contract is converted to Chai, an interest earning form of Dai. The interest accumulated from the locked Chai during a staking epoch will be used as an additional incentive for stakers **in Phase 2** of the consensus upgrade.&#x20;

## Consensus POSDAO Upgrade: Phase 1

:dart: **Target Date:** Q1-Q2 2020\
:white\_check\_mark:**Status**: Completed 04/01/2020

{% hint style="success" %}
Phase 1 of the POSDAO upgrade was successfully activated April 1, 2020.&#x20;
{% endhint %}

xDai will upgrade to a Proof of Stake model in several phases. In the first phase, the current validators will receive xDai-based STAKE tokens and to protect the chain. These validators will remain in place to assist in the transition to phase 2.

For more information on this transition, see the [staking roadmap](../../for-stakers/staking-with-gno-on-the-gnosis-beacon-chain/stake-token/stake-and-staking/).

## EasyStaking STAKE on Ethereum

:dart: **Target Date**: Q3 2020\
:white\_check\_mark: **Status**: Completed 08/05/2020

[Easy Staking](../../for-stakers/staking-with-gno-on-the-gnosis-beacon-chain/stake-token/easy-staking/) provides an alternative interest-earning application for [STAKE ](../../for-stakers/staking-with-gno-on-the-gnosis-beacon-chain/stake-token/)token holders. Users can deposit STAKE tokens deployed on the Ethereum mainnet and earn a pre-determined interest rate without bridging to xDai and with no minimum STAKE amount requirements. Rewards are split among Liquidity Providers and protocol stakers.

Easy Staking serves to reduce the overall amount of STAKE in active circulation and acts as a mechanism to limit available liquidity and supply. Limited supply in the open market increases security for POSDAO chains such as the xDai stable chain.

## OmniBridge Phase 1

:dart: **Target Date**: Q3 2020\
:white\_check\_mark: **Status:** [Security Audits Completed 11/6/2020 ](../../for-developers/security-audits.md#tokenbridge-audit-by-quantstamp-covers-omnibridge)

Universal mediators will support transfers for virtually any ERC20 token to the xDai chain with no additional contract deployment. This lowers the barrier-to-entry for projects and DApps looking to move tokens to xDai and take advantage of low-fee, high-speed transactions. Users will be able to automatically create equivalent tokens on xDai ready for immediate usage.  Learn more here: [https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension)

## Bridge Governance Expansion

:dart: **Target Date:** Q3 2020\
:white\_check\_mark: **Status:** [Completed for both sides of the bridge 10/23/2020](../faqs/bridges-xdai-bridge-and-omnibridge.md#what-is-the-bridge-governance-board).

Bridge management should be expanded to additional community representatives. These individuals will use a Gnosis Safe to manage bridge operations. A majority must sign to approve operations including:

* Bridge contracts upgrades
* Extending the set of bridge validators
* Updating bridge parameters like number of block confirmations, transactions limits,  bridge fees etc.

## Consensus POSDAO Upgrade: Phase **2**

:dart: **Target Date:** Q2 2021\
:white\_check\_mark:**Status:** Completed Q4 2020.&#x20;

To increase decentralization and enable a permissionless consensus process,  the broader community will have the opportunity to participate as validators and/or delegators in the consensus process.&#x20;

## Change Log

| Update       | Items                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _26.01.2021_ | <p></p><ul><li>Update EasyStaking, POSDAO and Liquidity Pool Analytics to Complete</li></ul>                                                                                                                                                                                                                                                                                                                                                  |
| _04.01.2021_ | <p></p><ul><li>Organize 2020 items to completed, add preliminary 2021 Items</li><li>Adjust target dates for some 2021 items</li><li>Add NFT bridge</li></ul>                                                                                                                                                                                                                                                                                  |
| _23.12.2020_ | <p></p><ul><li>Update POSDAO Phase 2 to completed.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                  |
| _25.11.2020_ | <p></p><ul><li>Update Fiat -> xDai gateway status to completed.</li></ul>                                                                                                                                                                                                                                                                                                                                                                     |
| _18.11.2020_ | <ul><li>Update OmniBridge status to completed</li><li>Update Bridge Governance status to completed</li><li>Add OmniBridge Phase 2</li></ul>                                                                                                                                                                                                                                                                                                   |
| _24.09.2020_ | <ul><li>Switch Fiat integration to Wyre</li><li>Add Bridge Governance Expansion</li><li>Revise public POSDAO targets from Q4 2020 to Q2 2021 to devote resources to <a href="https://ethresear.ch/t/optimistic-bridge-between-mainnet-and-a-pos-chain/7965">Optimistic Bridge development</a>. </li><li>Add distributions dashboard to EasyStaking Liquidity Pool analytics</li><li>Adjust order of items to reflect prioritization</li></ul> |
| _06.08.2020_ | <ul><li>Update EasyStaking status to Completed</li><li>Adjust POSDAO consensus upgrade target to Q4 2020</li><li>Adjust Privacy Preserving transactions to Q3-Q4</li><li>Added LP Analytics to Q3 2020 </li><li>Added Multi-Token Bridge to Q3 2020</li></ul>                                                                                                                                                                                 |
| _28.05.2020_ | <p><em></em></p><ul><li>Added EasyStaking Q3</li><li>Updated Synthetic Assets to 50% complete</li><li>Adjusted target date for L2 scalability to Q1 2021</li><li>Renamed NG to POSDAO Phase 3, adjusted target date to Q2 2021</li></ul>                                                                                                                                                                                                      |

# EasyStaking on Ethereum

## EasyStaking

{% hint style="warning" %}
The following instructions are for easystaking on Ethereum, which uses the STAKE token. When the [STAKE -> GNO swap](../stake-gno-swap.md) is complete, participants will no longer accrue rewards. **It is recommended to exit the protocol and swap STAKE for GNO prior to the May 31 deadline.**
{% endhint %}

:ballot\_box\_with\_check: [https://easy-staking.xdaichain.com/deposits](https://easy-staking.xdaichain.com/deposits)

{% hint style="info" %}
EasyStaking is for staking STAKE on Ethereum. If you want to stake on xDai directly with POSDAO, see the [Staking Protocol and Tutorials](../staking-protocol/) section.

Easy Staking Stats are available here:\
[https://duneanalytics.com/maxaleks/xdai-staking](https://duneanalytics.com/maxaleks/xdai-staking)
{% endhint %}

{% hint style="success" %}
* [Instructions](instructions/) on how to use the EasyStaking application.
* [EasyStaking Parameters](easy-staking-parameters.md) for basic application requirements and incentive details.
* Learn how the xDai Foundation is bootstrapping the launch with the [EasyStaking Initiative](../../../../about-gc/news-and-information/project-updates/easystaking-launch-initiative.md).
* View reward scenarios and other metrics at [stakingrewards.com](https://www.stakingrewards.com/earn/xdai/calculate)&#x20;
* See a [reward comparison with different staking methods](../stake-reward-mechanics/staking-rewards-comparison.md) (EasyStaking, LP Provider, Delegation & Validation)
* View latest stats and analytics for EasyStaking and POSDAO with the :bar\_chart: [Dune Analytics Staking Dashboard](https://www.duneanalytics.com/maxaleks/xdai-staking).
{% endhint %}

## What is Easy Staking?

Easy Staking allows users to place STAKE into a contract and receive STAKE emissions on Ethereum. It provides an accessible staking mechanism for users and increases STAKE utility and DeFi composability. EasyStaking also:

* Incentivizes liquidity providers on decentralized exchanges through unique reward mechanisms
* Creates staking opportunities via hardware wallets and other Ethereum applications
* Provides staking opportunities with no minimum STAKE requirements to participate
* Limits total circulating supply

Total STAKE Emissions are minted at a total of 15% APR. Emissions are sent to stakers as well as Liquidity Pool Providers (see below) and provisioned based on two parameters:

* **Time**: 7.5% APR. The amount of time STAKE has been committed to the protocol. Longer staking times result in a higher APR for the Staker.
* **Total Staked Amount**: 7.5% APR. The total amount in the pool from all Stakers and other contributors. Larger stakes result in a higher APR for all Stakers. More staked amount = higher rewards.

![Sigmoid function for determining time-based APR.](../../../../.gitbook/assets/Sigmoid\_With\_Parameters.png)

Stakers and Liquidity Providers each receive portions of the emission based on how long a Staker decides to keep STAKE in the application and the total amount Staked. Longer staking times benefit the Staker, and shorter staking periods benefit Liquidity Providers.

## Time-Based Emission Example

| Example Staking Time | Staker    | Liquidity Providers   |
| -------------------- | --------- | --------------------- |
| 1 Month              | 5.02% APR | 15 - 5.02 = 9.98% APR |
| 4 Months             | 7.44% APR | 15 - 7.44 = 7.56% APR |
| 9 Months             | 7.70% APR | 15 - 7.70 = 7.30% APR |

{% hint style="info" %}
As well as functioning as a stand-alone application, Easy Staking may be integrated into hardware wallets and other applications.
{% endhint %}

## Liquidity Pool (LP) Participants

{% hint style="warning" %}
LP incentives are distributed on average every 7 days - the exact distribution date is randomized. Incentives are distributed among the **top 100 pools**.&#x20;
{% endhint %}

* Uniswap ETH/STAKE Pool: [https://uniswap.info/pair/0x3B3d4EeFDc603b232907a7f3d0Ed1Eea5C62b5f7](https://uniswap.info/pair/0x3B3d4EeFDc603b232907a7f3d0Ed1Eea5C62b5f7)
* LP STAKE reward distributions dashboard:\
  [https://stake-reward-distribution.xdaichain.com/](https://stake-reward-distribution.xdaichain.com/)

Liquidity pool providers will also receive STAKE incentives from the Easy Staking application. Users who put funds into an ETH/STAKE liquidity pool on Uniswap will be eligible for these additional incentives. **Note only the top 100 LPs receive additional STAKE.**&#x20;

&#x20;Here's an example of how it works for :man\_farmer: Bob:

1. Bob acquires .3 ETH and 30 STAKE by trading on [Uniswap](https://uniswap.exchange/swap), purchasing on [BitMax](https://bitmax.io/), or through some other means. (Model assumes .3 ETH and 30 STAKE have equivalent value)\

2. He goes to Uniswap (v2) and adds both into the [STAKE/ETH liquidity pool](https://uniswap.info/pair/0x3B3d4EeFDc603b232907a7f3d0Ed1Eea5C62b5f7).\

3. After some time, :man\_farmer: Bob checks his address and sees that he has received an additional 51 STAKE directly to his wallet. He has received STAKE rewards (at a very high % relative to his pool contribution) thanks to :woman\_artist: Mary :arrow\_heading\_down: withdrawing money from Easy Staking.

## STAKE Distribution (time-based example)

:woman\_artist: Mary has 10,000 STAKE she places into the Easy Staking application on the Ethereum Mainnet. She submits a deposit through the Easy Staking UI. After 1 year, she decides to realize her STAKE gains and submits a withdrawal request. Assume APR is 10%. Since she deposited 10000 STAKE and staked for 1 year, Mary receives 11000 STAKE (her initial amount + 10% APR).  The remaining 500 STAKE (5% APR) earned as part of the total 15% APR are sent to the LP distribution contract.

Distribution to LP participants occurs through a script which collects addresses and pool amounts. It is called once a week (within 5-9 day time slots at random intervals) and distributes funds based on pool participation percentages.

For simplicity, let's say only :man\_farmer: Bob and :man\_cook: Roger were participating in the Uniswap LP. Bob has .3 ETH/30 STAKE and Roger has .1 ETH/10 STAKE in the pool when the distribution script is executed.  At this point, :man\_farmer: Bob receives 375 STAKE (75% of the STAKE in the LP distribution contract) and :man\_cook: Roger 125 STAKE (25%) based on :woman\_artist: Mary's withdrawal scenario above.

In this example, this reward APR%  for Bob and Roger is very high, much more than they would have received for other staking methods, as they capture value from STAKE placed in the Easy Staking contract. Distribution percentages will vary based on how much ETH and STAKE exist in liquidity pools and how much STAKE is placed in the Easy Staking contract.&#x20;

## How to Participate

{% hint style="info" %}
The [instructions page](instructions/) covers the basics.
{% endhint %}

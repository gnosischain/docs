# Emission Rates

STAKE Emissions are minted at a total of 15% APR. Emissions are split between Stakers and Liquidity Providers (LP). Two factors determine the % accrued for each group.

* **Time-based**: 7.5% total APR, split between Stakers and LPs. The amount of time an individual deposit has been staked in Easy Staking. A longer staking time for a deposit results in a higher APR for the Staker. Rewards for Stakers increase rapidly during the first several months and level out over time as they approach the 7.5% max based on a [sigmoid function](https://www.desmos.com/calculator/2xtimbnzqw).\

* **Supply-based**: 7.5% total APR, split between Stakers and LPs. The total amount of STAKE in the pool from all Stakers. Larger amounts result in a higher APR for Stakers. Rewards increase in relation to the total amount staked vs the total supply (or by a factor between 0% and 100% of the total supply (`totalSupplyFactor`) if STAKE supply is a lot more than all STAKE holders currently have).

## Rewards Calculator

In addition to the calculator for stakers on the EasyStaking site, [StakingRewards.com](https://www.stakingrewards.com/) offers an example calculator for Stakers and LPs!&#x20;

To start, go to [https://www.stakingrewards.com/earn/xdai/calculate](https://www.stakingrewards.com/earn/xdai/calculate)&#x20;

From here you can select the Easy Staking or Liquidity Provider option, then adjust staking time, total amount staked and other parameters to see your anticipated rewards!

![](../../../../.gitbook/assets/staking-rewards.jpg)

## Examples

If a scheduled (timed) withdrawal with 0% fee occurs at the time-based point, the following rewards apply. If an instant withdrawal is processed, a fee is assessed on the total amount (deposit + emissions) and sent to the Liquidity Providers contract address prior to withdrawal.

| Staker Deposit Amount | Time-based (tb) | <p>Staker<br>tb <br>APR</p> | <p>Supply-<br>based (sb)</p>                                    | <p>Staker<br>sb <br>APR</p> | Reward Staker Receives                                                             | Reward LPs Receive                                                                      |
| --------------------- | --------------- | --------------------------- | --------------------------------------------------------------- | --------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| 1000 STAKE            | 28 days         | 4.53%                       | 2.134M out of 8.538M staked                                     | 1.875%                      | <p>4.91 STAKE <br></p><p><code>1000 * (4.53 + 1.875) / 100 * 28 / 365</code></p>   | <p>6.59 STAKE<br></p><p><code>1000 * (15-(4.53 + 1.875)) / 100 * 28 / 365</code></p>    |
| 5000 STAKE            | 48 days         | 5.99%                       | 2.134M out of 4.269M staked (totalSupplyFactor of 50% employed) | 3.75%                       | <p>64.04 STAKE</p><p></p><p><code>5000 * (5.99 + 3.75) / 100 * 48 / 365</code></p> | <p>34.58 STAKE</p><p></p><p><code>5000 * (15-(5.99 + 3.75)) / 100 * 48 / 365</code></p> |

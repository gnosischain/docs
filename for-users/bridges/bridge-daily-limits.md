# Bridge Daily Limits

Daily limits on token exits (bridging tokens from Gnosis Chain to Ethereum) have been established for several tokens on the Gnosis chain. The following tokens are impacted on the [xDai - Dai bridge](https://bridge.xdaichain.com/) (DAI) and the [Omnibridge](https://omni.xdaichain.com/bridge) (other tokens).

| Token | Daily Max  |
| ----- | ---------- |
| DAI   | 10,000,000 |
| USDC  | 10,000,000 |
| USDT  | 5,000,000  |
| WETH  | 250        |
| WBTC  | 2          |
| GNO   | 5000       |

Daily Max defines the maximum number of tokens that can be moved from Gnosis Chain to Ethereum in a 24 hour period, increasing bridge security and protecting against potential mass-liquidation events in the event any protocol on the GC is hacked and attackers want to quickly move stolen funds.

Once the daily limit is reached, users must wait until the following day to bridge additional amounts. Limits reset each day at 12:00am UTC.

The most recent limits were set and executed by a majority of the bridge governance board members [12 May, 2022. ](../governance/governance-board-summary-of-decisions.md#increase-limits-for-xdai-usdc-and-usdt)

Limits may be updated in the future based on fluctuations in assets locked in the bridge, and can be updated by a majority of bridge governors as required. To update limits for each token, transactions are signed and executed by governors on the Gnosis Chain side and then on the Ethereum side of the bridge.&#x20;

* Bridge Governor's Gnosis Safe on Gnosis Chain: [0x7a48Dac683DA91e4faa5aB13D91AB5fd170875bd](https://gnosis-safe.io/app/gno#/safes/0x7a48dac683da91e4faa5ab13d91ab5fd170875bd/transactions)
  * Invoked methods: `setMaxPerTx`, `setDailyLimit`
* Bridge Governor's Gnosis Safe on Ethereum Mainnet: [0x42F38ec5A75acCEc50054671233dfAC9C0E7A3F6](https://gnosis-safe.io/app/eth:0x42F38ec5A75acCEc50054671233dfAC9C0E7A3F6/transactions/history)
  * Invoked methods: `setExecutionMaxPerTx`, `setExecutionDailyLimit`


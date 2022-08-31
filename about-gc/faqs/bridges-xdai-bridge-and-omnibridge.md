# Bridges: xDai Bridge & OmniBridge

{% hint style="info" %}
The TokenBridge project is responsible for the xDai Bridge, OmniBridge and many other bridges in development for cross-chain interaction. For additional details, see the bridge documentation at [docs.tokenbridge.net](https://docs.tokenbridge.net/)
{% endhint %}

## Why are there Multiple Bridges?

Different bridges exist to support different operations. Two primary bridges exist on the Gnosis Chain. Additional bridges and/or extensions may be deployed in the future.

* **xDai Bridge**: Convert **Dai to xDai** and **xDai to Dai**
* **OmniBridge**: Convert **any other ERC20 tokens** on Mainnet to equivalent ERC677 tokens on the xDai chain. OmniBridge also has bridge modes to bridge tokens between xDai and Binance Smart Chain (BSC) and BSC and Ethereum.

An NFT Bridge is currently in active development.

The [Optimistic Omnibridge](https://ethresear.ch/t/optimistic-bridge-between-mainnet-and-a-pos-chain/7965) is also in R\&D as an option to provide a bridge for trustless transfers from GC to Ethereum.

## xDai Bridge FAQs

### Why is the xDai bridge important?

The bridge is a key element of GC, allowing for fast interoperability between xDai and Ethereum. The bridge connects the networks and allows tokens to exist on both sides. To mint xDai, Dai is locked in the bridge contract and the equivalent amount of xDai is created on the xDai chain. In order to return this xDai to Dai, xDai is burned and Dai is unlocked.

### My transaction is still pending, or was not completed. What should I do?

Please check the [Troubleshooting Section](../../for-users/bridges/converting-xdai-via-bridge/troubleshooting.md) for common issues and resolutions.

### What are the transfer limits when using the xDai bridge?

The current limits are below. Note that these can be changed by a majority vote from the Governance Board.

|                                         |                       |                |
| --------------------------------------- | --------------------- | -------------- |
| Max Single Deposit                      | 9,999,999 Dai         | 9,999,999 xDai |
| Minimum Transfer                        | 0.005 Dai             | 10 xDai        |
| Transaction (Gas) Fees                  | variable, paid in Eth | paid in xDai   |
| Transfer Fees (in addition to gas fees) | 0%                    | 0%             |

### What is the Bridge Governance Board?

In response to increased usage and value locked in the xDai bridge, a proposal was introduced to extend security and decision making powers to a wider group of participants (governors).

The proposal was accepted, and governance by means of a multi-signature Gnosis Safe was put into place initially on the Ethereum side on 2 October, 2020. Once Gnosis Safe was deployed to xDai, updated governance was enacted on the xDai chain on 23 October, 2020.

* [Current xDai Bridge Governance Board Members](../../for-validators/for-bridge-validators/)
* Gnosis Safe contract on Ethereum: [https://gnosis-safe.io/app/#/safes/0x42F38ec5A75acCEc50054671233dfAC9C0E7A3F6/settings](https://gnosis-safe.io/app/#/safes/0x42F38ec5A75acCEc50054671233dfAC9C0E7A3F6/settings)
* Gnosis Safe contract on xDai: [https://xdai.gnosis-safe.io/app/#/safes/0x7a48Dac683DA91e4faa5aB13D91AB5fd170875bd/settings](https://xdai.gnosis-safe.io/app/#/safes/0x7a48Dac683DA91e4faa5aB13D91AB5fd170875bd/settings)

{% hint style="info" %}
For more on this transition, see the original forum proposal: [https://forum.poa.network/t/increase-number-of-participants-in-the-xdai-bridge-management-multsigs/3773](https://forum.poa.network/t/increase-number-of-participants-in-the-xdai-bridge-management-multsigs/3773)
{% endhint %}

### How are the xDai bridge validators managed?

The bridge governance board votes on management, and smart contracts deployed on both sides of the bridge (Ethereum and Gnosis Chain) are updated to reflect changes. [Learn More](../../for-validators/for-bridge-validators/).

### I completed a Dai to xDai transfer and see the transaction to lock Dai, but do not see the transaction that mints xDai. How does it work?

The process requires several steps on the xDai chain.

1. Oracles send confirmations of the transaction to the bridge contract.&#x20;
2. After receiving the required number of confirmations, the bridge contract sends a request to the Block Reward contract to schedule emission (minting) of new xDai (the same denomination as requested in the bridge transaction).
3. The Block Reward contract is invoked by the xDai network validator during the last step of block verification, and account balances are updated in the Block Reward contract.&#x20;

{% hint style="info" %}
Example transaction executing a transfer: [https://blockscout.com/xdai/mainnet/tx/0x799abac45b6c2ab18728b3baa04d112f8af8fba4d34d8078cf93856c71e73b91/internal-transactions](https://blockscout.com/xdai/mainnet/tx/0x799abac45b6c2ab18728b3baa04d112f8af8fba4d34d8078cf93856c71e73b91/internal-transactions)

🔎 Transactions can be investigated in further detail using [Tenderly](https://tenderly.co/).

💁♂ When troubleshooting, check the Coin Balance History in Blockscout for the account in question to find information about balance changes and blocks where these occurred.
{% endhint %}

### When claiming a DAI transaction on Ethereum, does the user originating the transaction also need to pay for the claim?

No, anyone can pay the fees to process the claim transaction and receive DAI, but the DAI will always be sent to the account set as the receiver in the initial originating request. This functionality opens the door for projects or other entities to pay for gas fees/subsidize the claims on Ethereum.

#### Claim Amnesty

A claim amnesty was initiated by the xDai team on May 21, 2021 to assist users whose DAI had gone unclaimed on the mainnet. Over 160K in DAI was returned to 461 Ethereum addresses. The xDai team paid the fees for these transfers totaling 3.58 ETH - the equivalent of $8,985 USD. The average costs was $19.50 per claim transaction. Amnesty was also processed for [OmniBridge users](bridges-xdai-bridge-and-omnibridge.md#claim-amnesty-1). The amnesty was provided as a one-time service to the community with no immediate plans for future amnesty.

Address processing the amnesty claims: [https://etherscan.io/address/0xbf74fdd93597f8e4fafbe7fa777e5d14195d7905](https://etherscan.io/address/0xbf74fdd93597f8e4fafbe7fa777e5d14195d7905)

### I didn't claim my Dai on Ethereum yet (completed 1st transaction on Gnosis Chain but not the claim transaction). Is there a time limit to claim my Dai?

No. The amount will remain locked in the contract until you decide to claim it. If gas prices are high, you may want to wait to execute the claim transaction when prices are more in your favor. For more on dealing with high gas fees for claims, [see this troubleshooting question.](../../for-users/bridges/converting-xdai-via-bridge/troubleshooting.md#gas-fees-for-an-exit-claim-are-very-high-how-can-i-reduce-them)

If you have an unclaimed amount, you will see a message once you connect your web3 wallet to the application.

![](../../.gitbook/assets/claim1.png)

Click on the History button to see your transactions, then click the Claim button in the history section to claim the transaction. You will need Eth to complete your claim.

![](../../.gitbook/assets/claim2.png)

### I decided I don't want to bridge my xDai to Ethereum, but already processed the first transaction. Can I revert?

No, this is not possible. When the first transaction is complete, the requested amount of xDai is burned on the xDai chain. If you want to return the amount back to the xDai chain, you must finalize the transfer (claim) on Ethereum and then send back to the xDai chain via the bridge to mint xDai once again.

### My transaction was successful, so why do I see "Failed" status for some bridge validators in the ALM application?

Once a quorum of confirmations is reached, the transaction is executed and the remaining confirmations are not required. This saves resources, and creates an easy visual record to see which validators confirmed for any given tx.

Successful transactions are recorded with Status "Success", and additional validator confirmations, which are not needed, are either marked as 'Failed' or 'Not required' depending on the processing order.

## OmniBridge FAQs

## OmniBridge Basics

### What is the OmniBridge URL?

[https://omni.gnosischain.com/](https://omni.gnosischain.com/)

### I want to learn more about OmniBridge internal functionality and/or developer features

Please see the OmniBridge documentation at [https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension) for additional details.

### What tokens have been bridged using OmniBridge?

You can find current lists on BlockScout. This includes tokens bridged from Ethereum and tokens bridged from Binance Smart Chain.

The suffix **from Ethereum** or **from BSC** is added to the token name so users know which chain the token was bridged from.

Bridged from Ethereum: [https://blockscout.com/xdai/mainnet/bridged-tokens/eth](https://blockscout.com/xdai/mainnet/bridged-tokens/eth)\
\
Bridged from Binance Smart Chain: [https://blockscout.com/xdai/mainnet/bridged-tokens/bsc](https://blockscout.com/xdai/mainnet/bridged-tokens/bsc)

### How do I monitor transactions?

Use the AMB Live Monitoring application located at [https://alm-xdai.herokuapp.com/](https://alm-xdai.herokuapp.com/). You can enter a transaction originating from either side of the bridge. More information on various [ALM transition states is available here](https://docs.tokenbridge.net/about-tokenbridge/components/amb-live-monitoring-application/alm-transition-states).

### I don't see the token I bridged in MetaMask - how can I add it?

The easiest way is to connect MetaMask to xDai and click on the "MetaMask" icon next to the token in the tokens list. This will add the token address to your MetaMask account.

![](<../../.gitbook/assets/MM-1 (1).png>)

If preferred, you can also add manually. [Here are some instructions](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension/ui-to-transfer-tokens/transfer-erc20#add-the-new-token-to-metamask).

### What is the minimum number of a certain token that can be transferred using OmniBridge?

This can vary by token. The default setting when a token is first bridged is 1, but this can be changed by bridge governance. To check the minimum for a particular token, query the `minPerTx` method of the omnibridge mediator contract.

1. Go to [https://blockscout.com/xdai/mainnet/address/0xf6A78083ca3e2a662D6dd1703c939c8aCE2e268d/read-proxy](https://blockscout.com/xdai/mainnet/address/0xf6A78083ca3e2a662D6dd1703c939c8aCE2e268d/read-proxy)
2. Enter the bridged contract address into the `minPerTx` field. Convert from wei using [http://eth-converter.com/](http://eth-converter.com/)

![](../../.gitbook/assets/query1.png)

{% hint style="info" %}
For more details about other OmniBridge parameters, see the[ OmniBridge docs](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension#omnibridge-technical-information-and-extension-parameters).
{% endhint %}

### Can I use Omnibridge without the UI?

Yes you can. [Instructions](https://docs.tokenbridge.net/eth-xdai-amb-bridge/multi-token-extension/how-to-transfer-tokens).

## OmniBridge Validators

### Does the OmniBridge use the same validators / governors as the xDai bridge?

No, OmniBridge is an extension (similar to a DApp) unrelated to chain consensus and it uses a separate set of validators. [Learn more](../../for-validators/for-bridge-validators/).

### Do validators replace transactions that are taking a long time to mine?

Yes, attempts are made to replace transactions with a higher gas price after 20 minutes. This occurs if it receives a price provided by the gas price oracle, and is repeated every 20 minutes until the transaction is successful.

## Troubleshooting Issues

### MetaMask is showing very high fees to claim a transaction on Ethereum (tokens bridged from Gnosis Chain to Ethereum). Is this estimate accurate?

Generally, the MetaMask gas limit estimates are high for OmniBridge tokens. In the following example, the gas limit was 1,036,275 but the gas spent for the execution was 208,805, **5 times lower than estimated**.

**Example:**\
[https://etherscan.io/tx/0x35c33d1d95794c46e70dd846811d82a4c202c1380a2df65f447f26e9dd98f778](https://etherscan.io/tx/0x35c33d1d95794c46e70dd846811d82a4c202c1380a2df65f447f26e9dd98f778)

Each token has unique parameters, and it is not possible to provide an accurate estimate before the tx is sent to the bridge oracles. Here are a few examples to provide an idea of the gas costs when transferring tokens from xDai to Ethereum\*.

| Token | Min Gas to Execute | Max Gas to Execute |
| ----- | ------------------ | ------------------ |
| USDC  | 209,312            | 239,396            |
| STAKE | 206,499            | 236,559            |
| WETH  | 203761             | 233,821            |

{% hint style="info" %}
_\*Notes:_

* Max Gas may be higher for a given tx, data is taken from a small sample size.
* Some bridged tokens may have a much higher cost depending on the contract internals. For example, plDai max was 494,794.
* We are working to provide more accurate estimates on a per-token basis, starting with higher volume bridged tokens.
{% endhint %}

When confirming a transfer, you will see a note with information about a claim transfer. This is a semi-accurate estimate of cost (it is a hardcoded value).

You always have the option to process the first tx on GC, then wait until gas prices are lower on Ethereum to execute the 2nd claim transaction.

![](<../../.gitbook/assets/confirm-transfer (1).png>)

### If the cost to claim less than the MetaMask estimate, do I still need the full amount of estimated ETH to start the claim process?

Yes, you will need that much in your wallet to initiate the claim transaction. However, only the amount used for gas fees will actually be deducted from your balance.

With the example in the question above, the MetaMask estimate tx fee was 0.109 ETH/$200 worth of ETH at the time. The user needed to have that amount to start the tx, but the final cost was only 0**.**0218 ETH/$40. It is also useful to [check the current gas price](https://www.ethgasstation.info/) and possibly adjust your gas price (amount you are willing to pay per unit of gas) but **DO NOT adjust the gas limit (the max amount of gas spent for the claim)**.

### I completed the first transaction but decided I don't want to complete the 2nd (claim). Can I revert?

Unfortunately not, once you have started the transfer process it is non-reversible. The only way to complete is to claim the token on Ethereum. If too expensive, you can wait until gas fees come down. There is not a time limit to claim the transaction.

#### Claim Amnesty

A claim amnesty was initiated by the xDai team on May 22, 2021 to assist users whose tokens had gone unclaimed on the mainnet. Over 200K worth of tokens were returned to 570 Ethereum addresses. The xDai team paid the fees for these transfers totaling 6.06 ETH - the equivalent of $15,200 USD. The average costs was $26.66 per claim transaction. Amnesty was also processed for [xDai Bridge ](bridges-xdai-bridge-and-omnibridge.md#claim-amnesty)users. The amnesty was provided as a one-time service to the community with no immediate plans for future amnesty.

Address that processed the claims: [https://etherscan.io/address/0xbf74fdd93597f8e4fafbe7fa777e5d14195d7905](https://etherscan.io/address/0xbf74fdd93597f8e4fafbe7fa777e5d14195d7905)

### Can I claim transactions manually?

Yes, it is possible to use BlockScout and Etherscan to interact with the contracts and submit manually, or if you are familiar with the contract interaction through a Web3 provider, you can importing the contract's ABI to your application. [This post details how](https://docs.tokenbridge.net/eth-xdai-amb-bridge/about-the-eth-xdai-amb/submit-confirmations-manually).

### I am seeing a warning while bridging. What does it mean?

To improve the user experience, several warnings are provided related to specific bridge operations. Common Warnings:

**Binance Pegged Asset Warning**:  Transferring assets such as WXDAI or USDC from Ethereum directly to Binance can result in assets on BSC with no liquidity. Before bridging, these assets should be exchanged to BSC compatible assets using Component. [Learn More](../../for-users/bridges/omnibridge/binance-smart-chain-omnibridge/dai-token-on-xdai-bsc.md)

![](<../../.gitbook/assets/warning-1 (1).png>)

**Gas Price Warning**:  Displays if the gas price is high on Ethereum (relative to the recent median price). You can still bridge and claim with the current gas price, bridge later, or complete the first bridge action and come back to claim when gas prices are lower.

![](../../.gitbook/assets/warning-2.png)

**Inflationary Token Warning**: Inflationary tokens do not accumulate gains for users while these funds are locked in the bridge. Gains remain in the contract on exit.  These tokens can be bridged, but users must check a box to proceed with the understanding they will not receive gains. [More information and inflationary token examples](../../for-users/bridges/omnibridge/exceptions.md#inflationary-eth-2-0-staking-tokens).

![](../../.gitbook/assets/warning-3.png)

**Rebasing Token Warning**: Rebasing tokes cannot be bridged, and a warning message alerts users to this fact. Transfer of these types of tokens to xDai is disallowed due to bridging mechanics. [More information and examples](../../for-users/bridges/omnibridge/exceptions.md#rebasing-tokens).

![](../../.gitbook/assets/warning-4.png)

### Is a token I want to bridge traded on HoneySwap?  I am confused if it was bridged from Ethereum or BSC.

There can be confusion when tokens are bridged to xDai from both Ethereum and Binance Smart Chain. To check where a token was bridged from, and if there is liquidity for trading:

1\. Go to [https://info.honeyswap.org/pairs](https://info.honeyswap.org/pairs) to find a pair you may want to swap. For example, WETH-LINK: [https://info.honeyswap.org/pair/0x529410569eef63b2d73612f0f844a5133265af68](https://info.honeyswap.org/pair/0x529410569eef63b2d73612f0f844a5133265af68) \
In this example, Click on the LINK token.

![](../../.gitbook/assets/ink-token.png)

2\.  This will take you here: [https://info.honeyswap.org/token/0xe2e73a1c69ecf83f464efce6a5be353a37ca09b2](https://info.honeyswap.org/token/0xe2e73a1c69ecf83f464efce6a5be353a37ca09b2). Click on the token address or use the address starting with 0x and paste into BlockScout.

![](../../.gitbook/assets/link2.png)

3\. In BlockScout, click on the TokenProxy token name (ChainLink Token on xDai) to go to the token page. Example token page: [https://blockscout.com/poa/xdai/tokens/0xE2e73A1c69ecF83F464EFCE6A5be353a37cA09b2/token-transfers](https://blockscout.com/poa/xdai/tokens/0xE2e73A1c69ecF83F464EFCE6A5be353a37cA09b2/token-transfers)&#x20;

![](../../.gitbook/assets/ink3.png)

4\. The Token Name will reflects the chain the token was bridged from (from Ethereum). Tags also tell you where the token was bridged from. “ETH” means that the token was bridged from the Ethereum Mainnet. “BSC” means that the token was bridged from Binance Smart Chain.&#x20;

![](../../.gitbook/assets/chainlink-pic1.png)

### How can I convert USDC from Binance Smart Chain to USDC on xDai, or DAI from BSC to xDai?

Use [https://xdai.component.finance/](https://xdai.component.finance/) to swap between USDC bridged from Ethereum or Binance Smart Chain. You can also use to swap between Dai bridged from Binance Smart Chain and wxDai. [More instructions are here.](../../for-users/bridges/omnibridge/binance-smart-chain-omnibridge/dai-token-on-xdai-bsc.md)

### I'm having issues related to Bridging & HoneySwap 🐝

Honeyswap is a popular application running on xDai and utilizing bridge functionality. They have a forum at [https://forum.1hive.org/](https://forum.1hive.org/) with tons of info, a [Discord ](https://discord.com/invite/NTDBRNz)and [an FAQ](https://about.1hive.org/faq/) that covers basics about bridging, xDai and more. Please bring any related questions to them.

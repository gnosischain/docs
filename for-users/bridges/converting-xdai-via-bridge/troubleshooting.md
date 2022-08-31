---
description: Resolving bridge issues
---

# Troubleshoot Bridge Txs, UI, xDai.io, xmoon.exchange, MetaMask

Bridge transactions can take some time (hours in extreme cases) to complete depending on Ethereum mainnet congestion. Try these actions first if your transaction has been **pending for 10 minutes or more** (and you don't want to wait any more time). Actions differ depending on if you are transferring from xDai to Dai or [Dai to xDai](troubleshooting.md#dai-to-xdai-transaction-is-taking-a-long-time).

If you are using OmniBridge for other ERC20 tokens (not xDai <-> Dai) please see the [OmniBridge page](../omnibridge/). **This guide only addresses issues with xDai to Dai transfers.**

{% hint style="info" %}
**Things to know**

* A bridge exit (moving from xDai to Dai) requires **2 transactions**, **one to initiate the transfer** on xDai, and a **2nd to claim DAI on Ethereum**.
* To process the **2nd transaction**, you will need to **switch to Ethereum Mainnet in Metamask** and **you will need Ether to pay gas fees.**
* The **2nd transaction may take quite a long time**, it is being processed on Ethereum. You can set a higher gas price if you want to speed it up. [**Instructions**](troubleshooting.md#dai-to-xdai-transaction-is-taking-a-long-time)**.**
* If you closed the UI before starting the 2nd transaction, you can come back and to complete later. [**Instructions**](troubleshooting.md#i-used-the-xdai-bridge-ui)**.**
* Additional troubleshooting items below.
{% endhint %}

## Bridge UI is Offline or in Maintenance Mode

We are doing some periodic maintenance and optimization on the Bridge and are now putting the UI into maintenance mode during these times to avoid additional confusion and/or delayed transactions for users. If you started a transaction but it did not complete because of maintenance mode, be assured that funds are safe and will be available once maintenance is complete. If you have questions or concerns during maintenance, please contact us in [Discord channel ](https://discord.gg/mPJ9zkq)for up-to-date information.

## I Only See Bridging in 1 Direction

The bridge is dynamic and supports bi-directional bridging**. It will shift automatically when you update your web3wallet (MetaMask) to the correct chain**. When you are on Ethereum Mainnet, you will see the Eth-Mainnet to xDai chain side, and when you are on xDai, you will see the xDai to Eth Mainnet side. You can adjust which side through the Bridge toggle in menu, however to initiate a transfer you will need your wallet set to the correct chain.

![](../../../.gitbook/assets/toggle.gif)

## I Transferred xDai to Dai but it's Not Working

A new bridge decentralization feature means **withdrawals now require 2 steps**. You must

1. initiate the bridge transaction on xDai
2. Claim your Dai on Ethereum.&#x20;

There are currently different bridging UIs, and depending on the UI you may need to take different steps to complete the process.

* \*\*\*\*[**xDai bridg**e](troubleshooting.md#i-used-the-xdai-bridge-ui) at [https://bridge.xdaichain.com/](https://bridge.xdaichain.com/) (or [http://dai-bridge.poa.network/](http://dai-bridge.poa.network/) - this is another URL for the same app)
* [**Burner Wallet**](troubleshooting.md#i-used-burner-wallet-at-xdai-io) at [xDai.io](https://xdai.io)
* \*\*\*\*[**xMoon exchange**](troubleshooting.md#i-used-xmoon-exchange) at [https://xmoon.exchange/](https://xmoon.exchange/)

## I Used the xDai Bridge UI

When using the xDai bridge, we recommend Chrome and MetaMask. It is also useful to disable ad blockers, as there are popups which guide you through the process. [A successful transfer process is documented here](moving-xdai-to-dai.md).

If you submitted a tx on xDai, but not complete the claim process, return to the Bridge Ui and connect your MetaMask (MM) wallet with the account you used previously.

1\) Switch MetaMask to the ETH Mainnet. If you have unclaimed txs you should see the following popup. Click on **History**.

![](../../../.gitbook/assets/xmodal1.png)

2\) If you are in the Bridge UI, you can also click on **History to view.**

![](../../../.gitbook/assets/history-1.png)

1. **Filter by Unreceived Transactions** and click the **Claim** button to begin the process. MetaMask will ask you to confirm the transaction and pay the gas fees to complete the process.

![](../../../.gitbook/assets/history2.png)

![](../../../.gitbook/assets/history3.png)

{% hint style="info" %}
You may want to [manually set gas prices for a cheaper exit](troubleshooting.md#gas-fees-for-a-claim-are-very-high-how-can-i-reduce-them).
{% endhint %}

## I Used **Burner Wallet** at xDai.io

If you initiated a transfer from Burner Wallet, it likely is stuck on the Waiting for Bridge message.

![](../../../.gitbook/assets/b1.jpg)

### I'm connected to the Burner Wallet with MetaMask

You can retrieve the pending transaction using the MetaMask interface. [Learn more here.](find-a-transaction-hash.md#find-transaction-hash-in-metamask)

1. Go to the Bridge UI at [https://bridge.xdaichain.com/](https://bridge.xdaichain.com/)
2. Switch your MetaMask wallet to the ETH Mainnet
3. Click on **History.** You will see any unclaimed transactions_. (You can also filter unclaimed transactions)_&#x20;
4. Press the **Claim button** to process**.** _(will not appear until 6+ minutes after the transaction)_
5. **Confirm** transaction in MetaMask and wait for tx validation.

{% hint style="warning" %}
You may want to [manually set gas prices for a cheaper exit](troubleshooting.md#gas-fees-for-a-claim-are-very-high-how-can-i-reduce-them).
{% endhint %}

### I'm using a standalone Burner Wallet

In this case, you'll want to export your private key into MetaMask to finish the conversion.

1\) Click the Advanced Button.

![](../../../.gitbook/assets/a1.jpg)

2\) Copy Private Key.

![](../../../.gitbook/assets/a2.jpg)

3\) Open MetaMask and import the account.

![](../../../.gitbook/assets/a3.jpg)

4\) Paste in the private key and click Import.

![](../../../.gitbook/assets/a4.jpg)

5\) Go to the Bridge UI at [https://bridge.xdaichain.com/](https://bridge.xdaichain.com/)

1. Switch your MetaMask wallet to the ETH Mainnet
2. Click on **History.** You will see any unclaimed transactions_. (You can also filter unclaimed transactions)_&#x20;
3. Press the **Claim button** to process**.** _(will not appear until 6+ minutes after the transaction)_
4. **Confirm** transaction in MetaMask and wait for tx validation.

{% hint style="warning" %}
You may want to [manually set gas prices for a cheaper exit](troubleshooting.md#gas-fees-for-a-claim-are-very-high-how-can-i-reduce-them).
{% endhint %}

{% hint style="info" %}
You will need some ETH in your wallet to pay gas fees and finalize the transaction. You can send from another account.
{% endhint %}

6\) You will see a Success message when the transaction is complete.

7\) Add DAI as a custom token in MetaMask to view your DAI balance in the wallet.

![](<../../../.gitbook/assets/a10 (2) (2) (2) (2) (2) (2) (2) (2) (2) (1).jpg>)

![](<../../../.gitbook/assets/a11 (2) (2) (2) (3) (3) (3) (2) (1).jpg>)

![](../../../.gitbook/assets/a12.jpg)

## I Used **xmoon.exchange**

### I'm connected to the xmoon.exchange with MetaMask (or another 3rd party wallet through wallet connect)

You can retrieve the pending transaction using the MetaMask interface. [Learn more here.](find-a-transaction-hash.md#find-transaction-hash-in-metamask)

Once you have copied the transaction on xDai

1. Go to the Bridge UI at [https://bridge.xdaichain.com/](https://bridge.xdaichain.com/)
   1. Switch your MetaMask wallet to the ETH Mainnet
   2. Click on **History.** You will see any unclaimed transactions_. (You can also filter unclaimed transactions)_&#x20;
   3. Press the **Claim button** to process**.** _(will not appear until 6+ minutes after the transaction)_
   4. **Confirm** transaction in MetaMask and wait for tx validation.

{% hint style="warning" %}
You may want to [manually set gas prices for a cheaper exit](troubleshooting.md#gas-fees-for-a-claim-are-very-high-how-can-i-reduce-them).
{% endhint %}

The claim will process and you can view your Dai on Ethereum with the same wallet you used to initialize the transaction on xMoon.exchange._._

## Gas fees For an Exit Claim are Very High! How Can I Reduce Them?

You can check current gas prices at [https://ethgas.watch/](https://ethgas.watch/). If they are high at the moment, you may want to wait until later to process your transaction. [https://ethereumprice.org/gas/](https://ethereumprice.org/gas/) can help you plan for the best time of day to make the claim transaction.

If you want to go ahead with the claim, try setting MetaMask to SLOW. This may take longer to process but can save you on tx fees. You can also click on Advanced to see additional metrics and choose an exact gas price for your transaction. [More information available here](https://metamask.zendesk.com/hc/en-us/articles/360015488771-How-to-Adjust-Gas-Price-and-Gas-Limit-).

## Dai to xDai Transaction is Taking a Long Time

8 block confirmations are required to ensure a transaction is final and xDai can be minted to your account. If Ethereum is congested, it may take many more blocks for your transaction to be queued. If your transaction is stuck in pending for a long time, you can opt try to speed it up by:

1. Selecting the pending transaction in MetaMask.
2. Clicking Speed Up.
3. Paying the additional gas to try and get it through more quickly.&#x20;

Otherwise, it will likely be in a pending state until the congestion breaks up. If it remains in a pending state on MetaMask for a long time, see [Resetting MetaMask ](troubleshooting.md#transaction-not-showing-on-blockscout-or-etherscan-resetting-metamask)below.

![](../../../.gitbook/assets/speedup.jpg)

## Transaction Not Showing on BlockScout or Etherscan - Resetting MetaMask.

If you initiated a transaction but don't see a pending transaction the Block Explorer (in either direction, if originating from xDai check [BlockScout](https://blockscout.com/xdai/mainnet), if Ethereum check [Etherscan](https://etherscan.io/)) try resetting your MetaMask account to clear your transaction history.

This can be useful to clear up:

* A pending transaction which refuses to clear.
* A transaction fails to show up on Etherscan but is still pending.

{% hint style="warning" %}
Imported accounts will not repopulate win your wallet with this method, so be sure you have access to a private key or seed phrase to restore these in a reset account.
{% endhint %}

{% embed url="https://metamask.zendesk.com/hc/en-us/articles/360015488891-Resetting-an-Account" %}

This [troubleshooting guide from 1Hive](https://forum.1hive.org/t/troubleshooting-problems-on-metamask/215) is also helpful for instructions on resetting and dealing with other MetaMask issues.

## I'm using a Ledger to Claim tokens on an xDai to Dai Bridge Transfer

To use a Ledger you need to allow contract data in order to interact with smart contracts. We assume that you have installed the [Ethereum app](https://support.ledger.com/hc/en-us/articles/115005200009-Set-up-and-use-MyEtherWallet).

1. [Update the firmware](https://support.ledgerwallet.com/hc/en-us/articles/360002731113) to the latest version.
2. Connect and unlock your Ledger device.
3. Open the **Ethereum** application.
4. Press the right button to navigate to **Settings**. Press both buttons to validate.
5. In the **Contract data** settings, press both buttons to allow contract data in transactions.  The device displays **Allowed**.
6. Retry your transaction.

For more help with Ledger, please see their [support docs](https://support.ledger.com/hc/en-us).

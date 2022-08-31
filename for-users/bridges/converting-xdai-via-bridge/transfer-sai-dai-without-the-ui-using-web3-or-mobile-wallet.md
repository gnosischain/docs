# Transfer Dai without a UI (using a web3 wallet and BlockScout / Etherscan)

It is possible to move Dai and xDai using a wallet rather than through the UI. This method is supported by all wallets that support ERC20 transfers (e.g. [NiftyWallet ](https://chrome.google.com/webstore/detail/nifty-wallet/jbdaocneiiinmjbjlgalhcelgbejmnid?hl=en), [MyEtherWallet.com](http://myetherwallet.com/), [TrustWallet](https://trustwallet.com/), [MetaMask](https://metamask.io/)). Here we use NiftyWallet.

Token address for reference:

* Dai: [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f)

TokenBridge addresses for reference (where you send the asset to transfer)

* Mainnet TokenBridge (Dai -> xDai): `0x4aa42145Aa6Ebf72e164C9bBC74fbD3788045016`
* xDai TokenBridge (xDai -> Dai): `0x7301CFA0e1756B71869E93d4e4Dca5c7d0eb0AA6`

## Transfer Dai from the Ethereum Mainnet to the xDai chain

1\) Connect to the Ethereum Mainnet and locate DAI in your webwallet.

![](../../../.gitbook/assets/sd1.png)

2\) Click Send

![](../../../.gitbook/assets/sd2.png)

3\) Enter in the following:

1. TokenBridge Address as the recipient: `0x4aa42145Aa6Ebf72e164C9bBC74fbD3788045016`
2. Amount to Send
3. Press Next

![](../../../.gitbook/assets/sd3.png)

4\) Submit the transaction

![](../../../.gitbook/assets/sd4.png)

4\) Wait for the relay confirmation from the bridge validators. This may take several minutes.

5\) Set your wallet to the xDai chain and check your balance.

![](../../../.gitbook/assets/sd5.png)

![](../../../.gitbook/assets/sdbalance2.png)

## Transfer xDai to DAI from the xDai chain to the Ethereum Mainnet

{% hint style="info" %}
The following demonstrates interaction with contract methods using BlockScout and Etherscan
{% endhint %}

1\) Send xDai coins to the Token Bridge address `0x7301CFA0e1756B71869E93d4e4Dca5c7d0eb0AA6` on the xDai Сhain using any wallet software.

2\) Wait for the transaction confirmation on the xDai chain (5 seconds).

3\) Copy the transaction hash of the confirmation and connect to the Ethereum mainnet.

4\) Visit the helper contract: [https://blockscout.com/xdai/mainnet/address/0x2D51EAa266eafcb59bB36dD3c7E99C515e58113A/read-contract](https://blockscout.com/xdai/mainnet/address/0x2D51EAa266eafcb59bB36dD3c7E99C515e58113A/read-contract)

5\) In the `getMessageHash` method field add the following information from your originating transaction and press the Query button. The method will return a hashed message.

* DAI recipient (typically the transaction sender but may differ if the ‘relayTokens’ functionality is used)
* Value (in **Wei** - do not include fees, only amount sent (Wei converter at [http://eth-converter.com/](http://eth-converter.com/))
* Originating transaction hash

6\) Copy the message hash and paste into the `getMessage` method. If you receive 0x0 it means either the bridge oracles did not send a confirmation for the withdrawal yet or the data entered in the step 3 is incorrect. Double check the info and if it is correct you will eventually receive the message.

7\) Once you receive the message, use the message hash again this time with the `getSignatures` method. It will return a blob with packed signatures provided by the validator. The method could fail if not enough signatures are collected.

![](../../../.gitbook/assets/blockscout1.jpg)

8\) Go to Etherscan and connect a web3 wallet: [https://etherscan.io/address/0x4aa42145aa6ebf72e164c9bbc74fbd3788045016#writeProxyContract](https://etherscan.io/address/0x4aa42145aa6ebf72e164c9bbc74fbd3788045016#writeProxyContract)

9\) Enter the message (from `getMessage` method above) and the signatures blob to the `executeSignatures` method, press the **Write** button and complete the transaction with a Web3 wallet. If the method reverts, the withdrawal was likely already executed. You can check all input for the recipient here: [https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0x](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0x)..., where the recipient's address follows after “a=“.

![](../../../.gitbook/assets/etherscan1.jpg)

Once you have written to the contract method, a View your **transaction** button will appear. Click to view the pending transaction.

![](../../../.gitbook/assets/etherscan3.jpg)

![A completed transaction](../../../.gitbook/assets/Etherscan2.jpg)

---
description: Swap and add liquidity on xDai
---

# SushiSwap

SushiSwap is a multi-chain DEX (decentralized exchange) with AMM (automated market-making) capabilities. It is deployed on several chains, and includes support for xDai. To incentivize usage, an [additional $2M in liquidity will be provided for select trading pairs](https://forum.poa.network/t/proposal-to-add-stake-incentives-matched-to-the-sushiswap-deployment-on-xdai/5821).

Detailed instructions follow. If you are familiar with trading on xDai and want to get started right away, go to [https://app.sushi.com](https://app.sushi.com/swap) and select xDai from the dropdown network list.

![](<../../.gitbook/assets/sushi-1 (1).png>)

{% hint style="info" %}
This tutorial uses MetaMask with xDai enabled (Custom RPC).  You will likely need this setup to transfer assets, and can [add xDai to MetaMask a number of ways](../../for-users/wallets/metamask/metamask-setup.md).
{% endhint %}

## 1) Bridge Assets to xDai

To start trading on xDai, move your assets (from Ethereum, BSC, Fantom, Polygon) using a bridge.  You can move a single asset and then convert to multiple assets on xDai using SushiSwap or other DEXs, or move multiple assets to xDai for use.\
\
There are several bridges available for moving assets. Fees vary based on the origination chain.

1. [xDai Bridge](https://bridge.xdaichain.com/). This bridge is used to convert Dai on Ethereum to xDai on the xDai chain. See the [Moving Dai to xDai tutorial](../../for-users/bridges/converting-xdai-via-bridge/moving-dai-to-xdai.md) for more information.
2. [OmniBridge](https://omni.xdaichain.com/bridge). For transferring any [ERC20 tokens on Ethereum](../../for-users/bridges/omnibridge/#resources) or [BSC](../../for-users/bridges/omnibridge/binance-smart-chain-omnibridge/bsc-omnibridge-example.md).&#x20;
3. [Connext Network Bridge](https://bridge.connext.network/). State channel bridge for stable asset transfer between xDai, Polygon, BSC and Fantom.

## 2) Swap Assets on Sushi

1\) Go to [app.sushi.com/swap](https://app.sushi.com/swap)

2\) Connect to xDai in the dropdown chain menu. If connected through MetaMask, a notification will ask if you want to switch chains (or add xDai chain if not in your MetaMask).&#x20;

![](../../.gitbook/assets/switch1.png)

![](../../.gitbook/assets/switch-2.png)

3\) Select the token you want to exchange and the token you want to receive. Exchange amount will auto-populate for the trade. Clicking on an asset brings up the Select a token menu for available assets.

![](../../.gitbook/assets/swap1.png)

![](../../.gitbook/assets/swap2.png)

4\) Swapping requires 2 confirmations with your connected wallet.

1. Press **Approve** to begin. You will sign a transaction in MetaMask to proceed.&#x20;
2. Once Approve is confirmed, press **Swap** to complete the transaction. For both transactions, it is possible to set Gas Price to 1 Gwei (unless network is congested - check slow, average and fast gas prices by hovering over the [xDai Gas Tracker on BlockScout](https://blockscout.com/xdai/mainnet)).

![](<../../.gitbook/assets/approve-1 (1).png>)

![Transaction 2 to Confirm the Swap](<../../.gitbook/assets/approve-2 (1).png>)

5\) Check your transaction(s) in BlockScout to verify. [https://blockscout.com/poa/xdai/tx/0xdb3f16bf528266f9525fc9923906b96a006e7a8bfe4dd152739b181567fcb087](https://blockscout.com/poa/xdai/tx/0xdb3f16bf528266f9525fc9923906b96a006e7a8bfe4dd152739b181567fcb087)

![](../../.gitbook/assets/blockscout-1.png)

## 3) Add Liquidity for LP Tokens

Once you have the required assets you can provide liquidity for a trading pair. You will need 50% of each asset to fund a pair. For example if you provide $100 worth of xDai you will also need to provide $100 worth of STAKE at current prices, or the corresponding 50/50 amount for any other pair you chose.

1\) Go to the Liquidity tab and select the assets you will provide.&#x20;

![](../../.gitbook/assets/liquidity-1.png)

2\) Enter the amount of the first asset. The second asset will auto-populate based on the amount provided. Click **Confirm Adding Liquidity** to proceed.

![](../../.gitbook/assets/liquidity-2.png)

3\) **Confirm Supply**. You will see the amount of LP tokens you will receive for providing liquidity. Note that you adjust gas price for this transaction as well.

![](../../.gitbook/assets/confirm-supply.png)

![](../../.gitbook/assets/confirm-supply2.png)

4\) Check your transaction in BlockScout to verify. \
[https://blockscout.com/poa/xdai/tx/0xcf6d9dcc4544dd263a424856cb4d7791c260d3e306b5aa0479d457645b5d5178](https://blockscout.com/poa/xdai/tx/0xcf6d9dcc4544dd263a424856cb4d7791c260d3e306b5aa0479d457645b5d5178)

![xDai was converted automatically to wxDai when adding liquidity to the pool](../../.gitbook/assets/view-bs-details.png)

4\) You can add additional liquidity or withdraw all or some LP tokens from pools you have funded. With your xDai account connected, go to the liquidity tab and press **View your Liquidity Positions**.&#x20;

![](../../.gitbook/assets/view-liquidity-1.png)

Click Manage to find buttons to **Add** or **Remove** liquidity, and follow the MetaMask prompts to confirm these transactions as you normally would.

![](../../.gitbook/assets/view-liquidity-2.png)

## 4) Add LP Tokens to MetaMask

It's easy to add custom tokens to MetaMask with BlockScout.&#x20;

1\) Find your LP transaction in [BlockScout](https://blockscout.com/poa/xdai) and click on the SLP token.

![](../../.gitbook/assets/add-1.png)

2\) On the token page, click on the **MetaMask icon** next to the token address.

![](../../.gitbook/assets/add-2.png)

3\) **Add Token** in MetaMask. The token will appear in your list of assets.

![Add Token to MM](../../.gitbook/assets/add-3.png)

![](../../.gitbook/assets/app-4.png)

## 5) LP Tokens and Incentives

Providing liquidity to some pairs will provide additional incentives for SushiSwap on xDai users. See the [Analytics Dashboard](https://analytics-xdai.sushi.com/) for more information on fees, volume and other metrics.&#x20;

Currently incentivized pairs are:

USDC-WXDAI\
WETH-WBTC\
STAKE-WXDAI\
WETH-WXDAI\
LINK-WXDAI\
USDT-WXDAI\
USDT-USDC

Please go to [app.sushi.com/yield](http://app.sushi.com/yield) for more information. Make sure you switch your network to xDai to see farms and APYs.

## 6) Lend and Borrow with Kashi

Anyone can create markets for lending, borrowing, and collateralizing assets on Kashi. Kashi users can leverage [Chainlink price feeds on xDai](../../for-developers/developer-resources/chainlink-price-feeds.md) to get accurate pricing info.&#x20;

{% hint style="info" %}
Learn more about Kashi in the [Sushiswap docs](https://docs.sushi.com/products/kashi-lending).
{% endhint %}

1\) Select either **Lend** from the main menu. You will be directed to [https://app.sushi.com/lend](https://app.sushi.com/lend)

![](../../.gitbook/assets/lend.png)

2\) Once in the Kashi interface:

1. Use the submenu to switch between the lend, borrow, and create functionality.&#x20;
2. From the lend tab, select an existing pool to add collateral.

![Example uses lending pools on Ethereum as xDai pools are just starting](../../.gitbook/assets/menu2.png)

3\) Click the button to sign and approve Kashi. This is a free transaction that gives Kashi full access to funds in (and approved to) BentoBox.

![](../../.gitbook/assets/approve1.png)

4\) Enter the amount you want to lend and approve the asset for transfer. Here we approve Dai.

![](../../.gitbook/assets/approve-2.png)

{% hint style="warning" %}
Note that the default is to provide unlimited amounts for transfer. This allows you to skip this step (and not pay for additional transactions of this type) in the future for this asset, but can introduce security risks. If you prefer to approve only for the amount you are lending, go to **Edit Permission** and select a custom amount for approval, then click **Save**.
{% endhint %}

![](../../.gitbook/assets/edit1.png)

![](../../.gitbook/assets/edit-2.png)

5\) Confirm the transaction. This transaction can be expensive on Ethereum (note the gas fees in this example) but not on xDai!  Once you confirm your funds will be included in the protocol.&#x20;

![](../../.gitbook/assets/approve-3.png)

{% hint style="info" %}
We will provide more info on lending and borrowing once the protocol is live with some funded pools on xDai.
{% endhint %}


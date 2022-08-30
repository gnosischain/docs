---
description: >-
  Converting Binance-Peg Dai Token to xDai / xDai to Binance-Peg Dai Token on
  xDai
---

# Binance-Peg Dai Token on xDai

The [Binance-Peg Dai Token](https://bscscan.com/token/0x1af3f329e8be154074d8769d1ffa4ee058b1dbc3) can be bridged to xDai using the beta BSC-xDai Omnibridge. **However, this process DOES NOT mint native xDai**. Instead, the [Dai Token from BSC](https://blockscout.com/xdai/mainnet/tokens/0xFc8B2690F66B46fEC8B3ceeb95fF4Ac35a0054BC/token-transfers) is bridged across networks.&#x20;

![](../../../../.gitbook/assets/binance-bridge-warning.png)

Using xDai tools, it only takes a few steps to convert Binance-Peg Dai to xDai. The process can also be completed in the reverse direction where xDai is converted to Binance-Peg Dai. Once converted from xDai, Binance-Peg Dai can be bridged back to BSC.

This option gives users the ability to convert Dai/xDai when mainnet bridging fees are expensive. A similar process should also be considered for Binance-Peg USDC tokens.

**Token Addresses:**

**Dai**

* [Binance-Peg Dai Token on Binance](https://bscscan.com/token/0x1af3f329e8be154074d8769d1ffa4ee058b1dbc3)
* [Binance-Peg Dai Token on xDai ](https://blockscout.com/xdai/mainnet/tokens/0xFc8B2690F66B46fEC8B3ceeb95fF4Ac35a0054BC/token-transfers)(Named Dai Token from BSC)

**USDC**

* [Binance-Peg USDC Token on Binance](https://bscscan.com/token/0x8ac76a51cc950d9822d68b83fe1ad97b32cd580d)
* [Binance-Peg USDC Token on xDai](https://blockscout.com/xdai/mainnet/tokens/0xD10Cc63531a514BBa7789682E487Add1f15A51E2/token-transfers) (Named USDC Coin from BSC)

**Tools Used:**

* [Wrapeth](https://wrapeth.com/): Convert xDai to wrapped xDai / unwrap wrapped xDai)
* [Component Finance](https://xdai.component.finance/): Swap stable tokens on xDai
* [BSC Bridge](https://bsc-to-xdai-omnibridge.web.app/): Bridge (in Beta) between xDai and Binance Smart Chain

## xDai -> BSC: Swap xDai to Binance-Peg DAI Example

### 1) Convert xDai to wxDai using the WrapEth Tool.

1. Go to [https://wrapeth.com/](https://wrapeth.com/)
2. set MetaMask to the xDai Chain Network
3. Enter the amount of xDai to wrap
4. Press Submit.
5.  Once the tx is complete, and wxDai is deposited, you can add wxDai ([0xe91D153E0b41518A2Ce8Dd3D7944Fa863463a97d](https://blockscout.com/xdai/mainnet/address/0xe91D153E0b41518A2Ce8Dd3D7944Fa863463a97d/transactions))

    to Custom Tokens in MetaMask.

![](../../../../.gitbook/assets/wrapeth1.png)

![](../../../../.gitbook/assets/add-token.png)

### 2) Swap wxDai for Binance-Peg Dai on xDai using Component.

1. Go to [https://xdai.component.finance/](https://xdai.component.finance/)
2. Connect your Web3 Wallet (MetaMask) to the application and confirm you are connected to the xDai network.
3. Press the Swap tab and select the **WXDAI/DAI \[BSC]** pair.
4. Press Swap. You will need to approve the first transaction with amount to swap or you can select unlimited.
5. Complete this first approve transaction in Metamask.
6. Press Swap again and confirm the second transaction to swap.
7. Once complete, add Binance-Peg Dai on xDai  to your MetaMask custom tokens. The address is [0xFc8B2690F66B46fEC8B3ceeb95fF4Ac35a0054BC](https://blockscout.com/xdai/mainnet/tokens/0xFc8B2690F66B46fEC8B3ceeb95fF4Ac35a0054BC/token-transfers) and in BlockScout it is called Dai Token on xDai.

{% hint style="info" %}
The same process can be used to swap USDC to USDC (BSC)
{% endhint %}

![Swap Tab with WXDAI and DAI \[BSC\] selected](../../../../.gitbook/assets/component.png)

![Unlock for swapping, you can allow unlimited approval or a smaller amount](../../../../.gitbook/assets/continue.png)

![TX1 for approval](../../../../.gitbook/assets/tx1.png)

![Tx 2 to complete the swap (2nd time pressing Swap button)](../../../../.gitbook/assets/tx2.png)

### 3) Move to BSC (if desired) with the BSC Bridge

You can [follow this tutorial](bsc-omnibridge-example.md) to bridge with the Omnibridge. Note you will need some BNB on the Binance Smart Chain to complete the process (to pay the claiming fee). If you have BNB on BEP2 you will need to swap it to BSC.

## BSC -> xDai: Swap Binance-Peg Dai to xDai

You will follow the same process in reverse to convert Binance-Peg Dai from BSC to xDai.

### 1) Bridge Dai from BSC to xDai.

You can [follow this tutorial](bsc-omnibridge-example.md) to bridge with the [Omnibridge](https://omni.xdaichain.com/bridge).

### 2) Swap Dai (BSC) token for wxDai using Component.

1. Go to [https://xdai.component.finance/](https://xdai.component.finance/)
2. Connect your Web3 Wallet (MetaMask) to the application and select the xDai network.
3. Press the Swap tab and select the Dai \[BSC]/ wxDai pair. Follow the instructions in section 2 above to approve 2 transactions and swap.

### 3) Unwrap wxDai into xDai with Wrapeth.

1. Go to [https://wrapeth.com/](https://wrapeth.com/)
2. Set MetaMask to the xDai Chain Network.
3. Select the Unwrap wxDai tab and enter the amount of wxDai to wrap.
4. Press Submit.

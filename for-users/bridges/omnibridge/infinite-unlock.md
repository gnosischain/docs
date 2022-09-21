---
description: Option to approve all token transfers
---

# Infinite Unlock

{% hint style="info" %}
**New Documentation here**
: [https://docs.gnosischain.com/](https://docs.gnosischain.com/)

The information in this page may be outdated.
{% endhint %}

You must give approval to the bridge contracts to access and send ERC-20 tokens. This is similar to Uniswap or another DEX that asks for approval to spend your tokens.&#x20;

You can give this permission on a per transaction basis, or you can unlock an unlimited amount to transfer with the infinite unlock option. Infinite unlock saves on transaction fees, but does introduce security risk if the contract is compromised. A 3rd party may have the ability to access all funds rather than a finite approved amount.

## Set Infinite Unlock

1\) Go to [ ](https://omni.xdaichain.com/)and select **Settings**.

![](../../../.gitbook/assets/settings-1.png)

2\) Toggle **Infinite Unlock** and Click **Save**. When you process your next unlock, the transaction will allow all transfers of that token without needing to unlock again.

![](../../../.gitbook/assets/infinite-1.png)

## MetaMask Unlock/Approvals&#x20;

You will notice when approving an unlock you are presented with options for the unlock in MetaMask. On the first screen you will see a message confirming you allow the contract to interact with and withdraw the selected token (in this case the xBRICK token). _Note the prior URL here, the correct url is_ [_https://omni.gnosischain.com/_](https://omni.gnosischain.com/)_._

![](<../../../.gitbook/assets/xBRICK-1 (1).png>)

Click **Edit Permission** to see details. From this screen you can set a **Custom Spend Limit** if you like. Notice the difference when Infinite Unlock is selected, giving permission to withdraw an unlimited amount.

![Without Infinite Unlock Set](../../../.gitbook/assets/MM2.png)

![With Infinite Unlock Set](../../../.gitbook/assets/mm3.png)

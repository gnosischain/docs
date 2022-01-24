# Voluntary Exit

If you decide to stop validating and disable your node, you can initiate a voluntary exit. This will freeze your balance at its current value (rewards and/or penalties will no longer accrue).&#x20;

If you perform a voluntary exit, you **will not be able to withdraw your balance** until the merge is complete and withdrawals are activated.

Voluntary exit procedures vary depending on your client.

{% hint style="warning" %}
Exits are non-reversible; once you have exited you cannot restart your validator.&#x20;
{% endhint %}

### Prysm

Login to your node and use the following command to request a voluntary exit. Replace \<PUBKEY\_1> with each public key you want to exit.

```bash
docker run --rm -it -v "$(pwd)/config:/tmp/config" -v "$(pwd)/wallet:/home/.eth2validators/prysm-wallet-v2" --network host ghcr.io/gnosischain/gbc-prysm-validator:v2.0.5-gbc accounts voluntary-exit --accept-terms-of-use --wallet-password-file /tmp/config/wallet_password.txt --beacon-rpc-provider localhost:4000 --public-keys "<PUBKEY_1>,<PUBKEY_2>,...,<PUBKEY_N>"
```

* For more info, see the [Prysm Voluntary Exit docs](https://docs.prylabs.network/docs/wallet/exiting-a-validator/)

### Lighthouse

Native support for voluntary exit is in process. If you need to request a voluntary exit prior to native support, please [contact us in discord](https://t.co/yrSN2dS9Z2) in the beacon-chain channel.

* For more info, see the [Lighthouse Voluntary Exit docs](https://lighthouse-book.sigmaprime.io/voluntary-exit.html)


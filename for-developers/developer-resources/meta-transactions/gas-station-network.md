---
description: Ethless transactions
---

# Gas Station Network

Gas Station Network supports the Gnosis Chain. Users without xDai can proceed immediately with transactions, helping facilitate onboarding. Transactions are subsidized by projects or Dapps through a relayer which accepts requests and pays gas fees on behalf of the user. Since tx costs are low this is not a large or variable expenditure for projects looking to support their users.

* See the [GSN docs](https://docs.opengsn.org/#the-problem) for more information on using/deploying relayers and [adding GSN to your application](https://docs.opengsn.org/javascript-client/getting-started.html#adding-gsn-support-to-existing-app).

### GSNv2 contracts on the GC

Please see the [GSN docs for address specifics and recommended configs](https://docs.opengsn.org/networks/xdai/xdai.html).

* **RelayHub:** Trustlessly connects clients, relay servers, and paymasters.\
  \-> Current [GSN relay servers on the Gnosis Chain](https://relays.opengsn.org/#xdai).
* **Forwarder**: Verify signature / nonce
* **VersionRegistry**: Manage versioning
* **Accept-Everything Paymaster**: Agrees to refund relay server for txs

\

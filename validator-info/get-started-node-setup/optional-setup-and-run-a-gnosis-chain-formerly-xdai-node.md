# Optional: Setup and run a Gnosis Chain (formerly xDai) Node

{% hint style="info" %}
This process is optional and suggested for experienced node runners only.
{% endhint %}

While not mandatory (public RPC endpoint connection is possible), we encourage users to also run a Gnosis Chain L1 node to increase decentralization. You can run the GC client on the same machine where you run the Gnosis Beacon Chain client or choose a different setup.

Select either OpenEthereum or Nethermind as your client of choice. Follow these instructions to get started:

* [Nethermind](../../clients/gnosis-chain-node-openethereum-and-nethermind/nethermind-node-setup.md)
* [OpenEthereum](../../clients/gnosis-chain-node-openethereum-and-nethermind/openethereum-node-setup.md)

Once your node is setup, take note of the RPC endpoint -  you will need it later in the setup. The default is typically `http://x.x.x.x:8545` where `x.x.x.x` is your instance ip.&#x20;

**Additional client RPC endpoint info:**

* [Nethermind RPC](https://docs.nethermind.io/nethermind/ethereum-client/json-rpc) (JSON RPC needs to be explicitly switched on in the Nethermind `config` file)&#x20;
* [OpenEthereum RPC](https://openethereum.github.io/JSONRPC) (HTTP: Listens on port `8545`)

### 3rd Party Public RPC Endpoints 

**Ankr Gnosis Public RPC:** [https://rpc.ankr.com/gnosis](https://rpc.ankr.com/gnosis)

Features: 
* Automatic geo-routing across North America, Europe, Asia for fast requests
* High Rate Limits


### 3rd Party Service Providers

Third party node providers are also an option for setting up and running a Gnosis (xDai) Chain Node.

* **QuickNode** [https://blog.quiknode.io/xdai-network-is-live-on-quiknode/](https://blog.quicknode.com/xdai-network-is-live-on-quiknode/)****
* **Ankr** [https://www.ankr.com/](https://www.ankr.com/protocol/public/gnosis/)****
* **GetBlock.io** [https://getblock.io/nodes/stake](https://getblock.io/nodes/stake)****
* **AnyBlock Analytics** [https://www.anyblockanalytics.com/json-rpc](https://www.anyblockanalytics.com/json-rpc/)****
* **Pocket** [https://www.portal.pokt.network](https://www.portal.pokt.network/#1).&#x20;

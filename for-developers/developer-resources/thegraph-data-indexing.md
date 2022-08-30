# TheGraph Data Indexing

[TheGraph](https://thegraph.com/), a decentralized protocol for indexing and querying chain data, supports the Gnosis chain. Data defined through subgraphs is easy to query and explore. Subgraphs can be created locally, or use a free hosted explorer for indexing and data display.&#x20;

## Setting up a hosted project with TheGraph & xDai

{% hint style="info" %}
See [https://thegraph.com/docs/quick-start](https://thegraph.com/docs/quick-start#hosted-service) for more details, local installation and more. The docs include an example for learning how subgraphs work and  [this video provides a good introduction.](https://thegraph.com/hackathons/2019/12)
{% endhint %}

The article below also covers the initializing a graph using a smart contract address on xDai.

{% embed url="https://medium.com/multiply-impact/impact-insights-b793289085b2" %}

## Steps:

1\) Go to Graph Explorer ([https://thegraph.com/explorer/](https://thegraph.com/explorer/)) and setup an account. You will need a GitHub account for authentication.&#x20;

2\) Go to your dashboard and click **Add Subgraph**. Define the subgraph Name, Account, and Subtitle and update the image and other info (you can update later) if desired.\


![Basic info is required to create a subgraph. You can modify later if needed.](../../.gitbook/assets/xdai-graph.png)

3\) Install Graph CLI on your machine (using either npm or yarn)

```
$ npm install -g @graphprotocol/graph-cli
$ yarn global add @graphprotocol/graph-cli

```

4\) The following command creates a subgraph that indexes all events of an existing contract. It attempts to fetch the contract ABI from BlockScout and falls back to requesting a local file path. If any of the optional arguments are missing, it takes you through an interactive form.\
\
_\*Note: The interactive form does not currently include Gnosis Chain in the dropdown of networks, so using the following flags is useful for a GC (xDai) deployment._

```
graph init \
  --from-contract <CONTRACT_ADDRESS> \
  [--network xdai ] \
  [--abi <FILE>] \
  <GITHUB_USER>/<SUBGRAPH_NAME> [<DIRECTORY>]
```

\--from-contract `<CONTRACT_ADDRESS>` is the address of your existing contract.

\--abi `<FILE>` is a local path to a contract ABI file (optional, If [verified in BlockScout](https://docs.blockscout.com/for-users/smart-contract-interaction/verifying-a-smart-contract), the graph will grab the ABI, otherwise you will need manually add the ABI. _You can save the abi from BlockScout or by running `truffle compile` or `solc` on a public project._ [_More info available here_](https://thegraph.com/docs/define-a-subgraph#the-subgraph-manifest)_.)_

The `<GITHUB_USER>` is your github user or organization name, `<SUBGRAPH_NAME>` is the name for your subgraph, and `<DIRECTORY>` is the optional name of the directory where `graph init` will put the example subgraph manifest.&#x20;

* _Chose the subgraph name created in step 2 as lowercase-hypenated_&#x20;

{% hint style="info" %}
More details are here: [https://thegraph.com/docs/en/developer/create-subgraph-hosted/](https://thegraph.com/docs/en/developer/create-subgraph-hosted/)
{% endhint %}

5\)  Authenticate with the hosted service

```
graph auth https://api.thegraph.com/deploy/ <your-access-token>
```

6\) cd to the directory you created and start defining the subgraph. Information on creating a subgraph is available in the Graph Docs.

{% embed url="https://thegraph.com/docs/define-a-subgraph" %}

7\) When you are ready, deploy your subgraph. You can always test and redeploy as needed.&#x20;

```
yarn deploy
```

{% hint style="success" %}
Your subgraph will be deployed, and you can try sample queries. If you are ready to make it public, select the subgraph and turn off the Hide slider.
{% endhint %}

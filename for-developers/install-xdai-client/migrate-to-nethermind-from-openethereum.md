# Migrate to Nethermind from OpenEthereum

Nethermind (NE) is the primary supported client for Gnosis Chain and node runners should switch to this client from OpenEthereum (OE).&#x20;

You can either:

1. Create a new, separate VM instance for your node and once it is synced stop your OE instance.
2. Run both OE and NE simultaneously on the same instance until Nethermind is synced.&#x20;

Instructions for both methods are below.

{% hint style="info" %}
Additional Notes:

* Nethermind uses [fast sync mode](https://docs.nethermind.io/nethermind/ethereum-client/sync-modes) by default. Syncing can take up to 24 hours depending on your setup.
* [Hybrid pruning](https://docs.nethermind.io/nethermind/ethereum-client/configuration/pruning) (memory + full) to save disc space is enabled by default and is the recommended setting.
* Erigon is not yet ready for GC but availability is expected following the Gnosis Chain <-> Gnosis Beacon Chain merge.
* If you are running a validator node on Gnosis Chain you will need to follow a [different set of instructions available here](broken-reference).
{% endhint %}

{% hint style="warning" %}
OpenEthereum on Ethereum:

* If your are running OE on Ethereum mainnet it is time to switch clients! Here are[ basic details on primary implementations](https://ethereum.org/en/developers/docs/nodes-and-clients/#execution-clientshttps://ethereum.org/en/developers/docs/nodes-and-clients/#execution-clients) along with links to setup and sync a new node. \
  \
  We recommend Nethermind, Erigon or Besu (rather than Geth) to help increase execution layer client diversity on Ethereum. [Current client stats.](https://ethernodes.org/)
{% endhint %}

## 1. Clean VM&#x20;

1. Check the [recommended configs](nethermind.md#configuration).
2. Install Docker Engine and Docker Compose following the instructions.
   1. &#x20;[https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)
   2. [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)
3.  Clone the repo.

    ```
    $ git clone https://github.com/xdaichain/non-validator-ne-node-dockerized
    $ cd non-validator-ne-node-dockerized
    ```
4.  Start your node.

    ```
    $ docker-compose up -d
    ```

After docker containers are created, the node will sync with the chain (may take a while).

To restart, use use `docker-compose stop` and `docker-compose start` from the `non-validator-ne-node-dockerized` directory.

Once your Nethermind node is fully synced, [stop your OpenEthereum node](migrate-to-nethermind-from-openethereum.md#stop-openethereum-node).

## 2. Simultaneous VM

1. Go to your VM where the OE node is running.
2. Create a separate folder for your your NE node.
3. If you haven't already,install Docker Engine and Docker Compose following the instructions.
   1. &#x20;[https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)
   2. [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)
4.  Clone the repo.

    ```
    $ git clone https://github.com/xdaichain/non-validator-ne-node-dockerized
    $ cd non-validator-ne-node-dockerized
    ```
5.  Change ports in `docker-compose.yml` on [lines 23-24](https://github.com/xdaichain/non-validator-ne-node-dockerized/blob/71bf7050af8728d0c40fff01ddff3e5e4e13675c/docker-compose.yml#L23-L24). This is required since 30303 is in use by OE.

    ```
    - "30304:30303"
    - "30304:30303/udp"
    ```
6.  Start your node.

    ```
    $ docker-compose up -d
    ```

Once your Nethermind node is fully synced, [stop your OpenEthereum node](migrate-to-nethermind-from-openethereum.md#stop-openethereum-node).

## Stop your OpenEthereum Node

Instructions vary based on your setup:

* If you run OpenEthereum in a terminal,  `CTRL+C` will cleanly exit. Make sure to wait a couple of seconds.
* To stop OpenEthereum started as system service, use `systemctl` (Linux) or `launchctl` (macOS):

```
sudo launchctl stop openethereum
```

* Another way is to issue a _hang-up_ (HUP) call for the OpenEthereum client, i.e.:

```
killall -HUP openethereum
```

* If using docker, cd to your directory and `docker-compose stop`

Once OE is stopped, you can remove the [data folder](https://github.com/xdaichain/validator-node-dockerized/blob/1cd379ff9b5e541120f29485bee96d093288bda5/docker-compose.yml#L36) to reclaim disc space.

{% hint style="info" %}
More information is available on the [OpenEthereum wiki.](https://openethereum.github.io/FAQ.html#basic-operations-configuration-and-synchronization)
{% endhint %}

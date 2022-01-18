# Get Started

## Chain Currently in Beta Deployment

{% hint style="success" %}
If you are interested in running a node in the future, please **** [**fill out this form**](https://airtable.com/shrrzJsRLa767gpcQ) and we will contact you to start the setup.
{% endhint %}

{% hint style="warning" %}
Instructions are in process. If you are not currently working with the team to run a validator, fill out the form above and we will contact you with more information.
{% endhint %}

{% hint style="info" %}
**Hardware Solutions.**

If preferred, you can use pre-configured hardware to easily run a node with minimal setup.

* **DappNode** supports the Gnosis Beacon Chain! To use services for validation, please see the [guide and instructions here.](https://forum.dappnode.io/t/how-to-setup-a-gnosis-beacon-chain-gbc-validator-on-dappnode/1351)
* [Avado](https://ava.do) offers an out-of-the-box validator solution.

Otherwise, proceed to the steps below to setup, run, and deposit to your validators.
{% endhint %}

## Setup Summary

Before you begin the setup, please check the [Validator Requirements and Responsibilities](../validator-requirements-and-responsibilities.md) and [Technical Requirements](../technical-requirements.md) for your node.

When you are ready, you will perform the following steps to get things up and running.

{% hint style="warning" %}
Optional:  [Setup and run a Gnosis Chain (GC) Node](./#1-setup-and-run-a-gnosis-chain-formerly-xdai-node): This step is for experienced node runners only. To gebin, it is not needed but will be encouraged for the merge. Instructions below include a default option to connect to the public RPC.
{% endhint %}

1. [Generate Validator Keystores and Deposit Data](./#2-generate-validator-account-s-and-deposit-data): On an offline machine, generate up to 128 separate validator keys per node.
2. [Choose your Gnosis Beacon Chain (GBC) Client](./#3-choose-your-beacon-chain-client-and-import-validator-keys): Choose to run either Prysm or Lighthouse. Add keystores and env variables.
3. [Start up your GBC Node](./#4-run-the-beacon-chain-node-with-the-attached-validator-process): Run in the docker container.
4. [Deposit to your Validator(s)](../validator-deposits/): Use the Deposit UI to convert GNO to mGNO (metaGNO for staking) and deposit to your validator.
5. [View on Explorer](../validator-deposits/#view-your-validator): Wait \~1.5-2 hours for your validator(s) to go live and view at [https://beacon.gnosischain.com](https://beacon.gnosischain.com).

### **Requirements:**

* Recent [Docker](https://www.docker.com) version (Docker v20.10+)
* Terminal access on your node and cli familiarity
* [MetaMask](https://metamask.io) (or equivalent) connected to the Gnosis Chain with 1 GNO per validator and a small amount of xDai for transaction costs.

## Step 1) Generate Validator Account(s) and Deposit Data

{% hint style="warning" %}
The following processes use [Docker](https://www.docker.com) to generate keystores and spin up clients. Please check that you are running a recent version. For key generation, binaries are also available.&#x20;
{% endhint %}

{% hint style="info" %}
We highly recommend generating keystores on a safe, completely offline device. To do so, you will need to connect online to pull the docker image (step 1), then disconnect to proceed with key generation (step 2), then finally save your deposit\_data.json file (step 3) to a usb key or other transfer method that does not require online connection.&#x20;

Securely backup your mnemonic, keystores, and password and keep in a safe place.
{% endhint %}

1.  Pull the docker image for the data generator.

    ```
    docker pull ghcr.io/gnosischain/validator-data-generator:latest
    ```
2. If this is your first time running the process and there is no an existing mnemonic to generate keystores and deposit data, replace the variables below with your info then run the command.\
   __
   1. `NUM` The number of signing keys (validators) to generate.
   2. `START_NUM` Index for the first validator key. If this is the first time generating keys with this mnemonic, use 0. If keys were previously generated with this mnemonic, use the subsequent index number (eg, if 4 keys have been generated before (keys #0, #1, #2, #3, then enter 4 here).
   3. `WITHDRAWAL_ADDRESS`  Use this parameter to provide a regular Gnosis Chain `0x` address for mGNO withdrawal. This parameter can also be omitted to generate withdrawal credentials with the mnemonic-derived withdrawal public key in the [EIP-2334 format](https://eips.ethereum.org/EIPS/eip-2334#eth2-specific-parameters) (Eth2 address format). Withdrawals will not be available until after the merge.
   4. `/path/to/` should be replaced with a valid and existing path where you want to create the validator\_keys folder. Or, to create the validator\_keys folder in your current working directory, use `$(PWD)/validator_keys:/app/validator_keys`
   5. More details about command line arguments can be found[ here.](https://github.com/gnosischain/validator-data-generator/)

```
docker run -it --rm -v /path/to/validator_keys:/app/validator_keys \
  ghcr.io/gnosischain/validator-data-generator:latest new-mnemonic \
  --num_validators=NUM --mnemonic_language=english --chain=gnosis \
  --folder=/app/validator_keys --eth1_withdrawal_address=WITHDRAWAL_ADDRESS
```

3\. If you have run the process before, you can prompt the mnemonic during execution:&#x20;

```
docker run -it --rm -v /path/to/validator_keys:/app/validator_keys \
  ghcr.io/gnosischain/validator-data-generator:latest existing-mnemonic \
  --validator_start_index=START_NUM --num_validators=NUM --chain=gnosis \
  --folder=/app/validator_keys --eth1_withdrawal_address=WITHDRAWAL_ADDRESS
```

4\.  Choose a secure password and confirm. You will see a mnemonic seed phrase. Write down and store your pwd and mnemonic safely offline.

![](../../.gitbook/assets/mnemonic.png)

Following execution, the path you defined for `/path/to/validator_keys` will contain the keystores and `deposit_data*.json` file.&#x20;

{% hint style="warning" %}
Note: The output will be "Success! Your keys can be found at: /app/validator\_keys/validator\_keys". However, **the validator\_keys folder will be located wherever you set `path/to/`**
{% endhint %}

{% hint style="info" %}
_`Want to learn more about Ethereum 2.0 keys and key generation?`_ 💡[Learn more](./#chain-currently-in-beta-deployment)
{% endhint %}

## Step 2) Choose Your Beacon Chain Client & Import Validator Keys

{% hint style="info" %}
To begin, determine which client you want to run, [Lighthouse ](https://lighthouse.sigmaprime.io)or [Prysm](https://prysmaticlabs.com). Instructions differ for the 2 clients.

Make sure your machine conforms to the [Technical Requirements](../technical-requirements.md#beacon-chain-node-requirements) for running a node, including opening the following pair of ports:

* **12000 UDP, 13000 TCP**
{% endhint %}

### Prysm

The Prysm client has been modified slightly. The underlying go-ethereum library used for eth1 block hash calculation is adapted to account for a different block structure. No other changes are made to the client, however, **the original Prysm binary will not work as expected for the Gnosis Chain - use the binary below**.

1. Go to a root directory where the node configuration and data will be stored. E.g. `cd /opt`.
2.  Clone the repo that includes the required configs.

    ```
    git clone https://github.com/gnosischain/prysm-launch.git gbc
    ```
3. Switch to the cloned directory: `cd gbc`.
4. Copy validators’ keystore files generated in _Step 1_ to the `keys/validator_keys` directory. **Keystores should only be used on a single node.**\
   ****_Note: Depending on your setup, you may need to_ [_change file ownership parameters_](https://linuxize.com/post/chmod-command-in-linux/) _to copy keys._
5. Write the keystore password from Step 1 to the `keys/keystore_password.txt` file.
6. Generate a wallet password and place it in the `./keys/wallet_password.txt`. Create a strong password (1 uppercase, 1 number, 1 special character, at least 8 characters long) using any password generation method and save it as `wallet_password.txt`. This password will be used by Prysm to access the validator's private keys following the import. [More info](https://docs.prylabs.network/docs/wallet/nondeterministic/#usage)
7. Create an `.env` file from the example at `.env.example`. Fill in the valid external `PUBLIC_IP` __ address of your node. Other values can remain unchanged. If you are experienced and want to run your own GC node, [see these instructions to connect to it](connect-to-a-gc-node.md).&#x20;
   1. Use the `curl ifconfig.me ; echo ''` command to get the IP of your node.
8.  Run the following command to import all added keystore files:

    ```
    docker-compose up validator-import; docker-compose down
    ```

### Lighthouse

The Lighthouse client has been modified to account for consensus parameters specific to the Gnosis Chain. **The original Lighthouse binary will not work; use the configured client below.**

1. Go to a root directory where the node configuration and data will be stored. E.g. `cd /opt`.
2.  Clone the repo that includes the required configs.

    ```
    git clone https://github.com/gnosischain/lighthouse-launch.git gbc
    ```
3. Switch to the cloned directory: `cd gbc`.
4. Copy validators’ keystore files generated on _the Step 1_ to the `keys/validator_keys` directory. **Keystores should only be used on a single node.**\
   ****_Note: You may need to_ [_change file ownership parameters_](https://linuxize.com/post/chmod-command-in-linux/) _to copy._
5. Write the keystore password to the `keys/keystore_password.txt` file.
6. Create an `.env` file from the example at `.env.example`. Fill in the valid external `PUBLIC_IP` __ address of your node. Other values can remain unchanged. If you are experienced and want to run your own GC node, [see these instructions to connect to it](connect-to-a-gc-node.md).&#x20;
   1. Use the `curl ifconfig.me ; echo ''` command to get the IP of your node.
7.  Run the following command to import all added keystore files:

    ```
    docker-compose up validator-import; docker-compose down
    ```

## Step 3) Run the Beacon Chain node with the attached Validator Process&#x20;

On the same machine as _Step 2_ run the following commands (works for both Lighthouse and Prysm):

```
docker-compose up -d node
docker-compose up -d validator
```

Observe the logs by `docker-compose logs -f node` to check that the node started successfully.

A similar command can be used to look at the validator process logs: `docker-compose logs -f validator`. But since deposits have not been made to the validators yet, there should not be much activity.

## Step 4) Make a Deposit

Making deposits is a 2 part process. See the [Validator Deposits section](../validator-deposits/) for details.

##

# T3rn_executor_node
Setting up T3RN Executor node on VPS

Welcome to t3rn, a Modular Interoperability Layer designed for fast, secure, and cost-efficient cross-chain swapping. t3rn is uniquely positioned to bridge the gaps in blockchain interoperability, offering superior swapping for users and yield for infra providers by becoming t3rn Executors.

Docs : [t3rn docs](https://docs.t3rn.io/intro) | X : [t3rn](https://x.com/t3rn_io)

---

💡 **Get started with the perfect VPS for your needs!** 🚀


----------------------------------------------------------------------------------------------------------------------------------------
### Getting Started with t3rn:
#### Participate as an Executor:
Join the network as an Executor to process transactions and engage in the ecosystem by bidding on orders and executing transactions.

#### Explore t3rn's Bridge UI:
Explore cross-chain swaps with our intuitive Bridge UI. Now live on testnets, it enables fast, secure, and cost-efficient cross-chain transactions.

Faucet : https://faucet.brn.t3rn.io/

Bridge : https://bridge.t1rn.io 

----------------------------------------------------------------------------------------------------------------------------------------

# Join Crypto Console Community

Join TG : [Crypto Console Telegram](https://t.me/Crypto_airdropHM) | 

----------------------------------------------------------------------------------------------------------------------------------------

### Update and upgrade system packages
```
sudo apt update
sudo apt upgrade
```
### Install fonts
```
sudo apt-get install figlet
figlet -f /usr/share/figlet/starwars.flf

```
### Download t3rn binaries
```
LATEST_VERSION=$(curl -s https://api.github.com/repos/t3rn/executor-release/releases/latest | grep 'tag_name' | cut -d\" -f4)
EXECUTOR_URL="https://github.com/t3rn/executor-release/releases/download/${LATEST_VERSION}/executor-linux-${LATEST_VERSION}.tar.gz"
curl -L -o executor-linux-${LATEST_VERSION}.tar.gz $EXECUTOR_URL

```
### Extract 
```
tar -xzvf executor-linux-${LATEST_VERSION}.tar.gz
rm -rf executor-linux-${LATEST_VERSION}.tar.gz
cd executor/executor/bin

```

### Open screen 
```
screen -S t3rn
```
### Set your preferred Node Environment.
```
export NODE_ENV=testnet
```
### Set your log settings
```
export LOG_LEVEL=debug
export LOG_PRETTY=false
export EXECUTOR_PROCESS_ORDERS=true
export EXECUTOR_PROCESS_CLAIMS=true
export EXECUTOR_MAX_L3_GAS_PRICE=50
export EXECUTOR_PROCESS_PENDING_ORDERS_FROM_API=false
```
### PRIVATE KEYS
Set the PRIVATE_KEY_LOCAL variable of your Executor, Replace with your privatekey
```
export PRIVATE_KEY_LOCAL=<replace your privatekey>
```
### Set Networks
```
export ENABLED_NETWORKS='arbitrum-sepolia,base-sepolia,optimism-sepolia,l1rn'
```
### Start Node
```
./executor
```

Take a screenshot of running node and post it on discord to get a role.

Discord : https://discord.gg/tW9Zqacw

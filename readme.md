# Fabric's network example with CA

This Hyperledger Fabric network consists of the following components:

- 2 peer nodes.
- 1 Raft orderer node.
- All nodes have their own CA.

## Instalation instructions

```sh
# Before begin we must set some environment variables in network folder
cd ./network
export PATH=${PWD}/../bin:${PWD}:$PATH
export FABRIC_CFG_PATH=${PWD}/../config

# Next, we need to execute the following scripts to start the network
. ./start.sh && clearExistingNetworks
. ./start.sh && startCAs
. ./start.sh && registerNodes
. ./start.sh && startNetwork
```

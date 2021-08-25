# Zbank Setup Manual

![blockchain](https://www.cyberbahnit.com/wp-content/uploads/2017/11/blockchain.jpg)



There are a few steps to setup Zbank's Blockchain
# Step 1
Create Nodes

Create accounts for two nodes using geth.
./geth --datadir node1 account new
./geth --datadir node2 account new

Step 2
Copy Node info

Node 1
Public address of the key:   0x263E6Ed688b78713f6996E2137468dF65873fd7e
Path of the secret key file: node1\keystore\UTC--2021-08-25T19-06-26.690460200Z--263e6ed688b78713f6996e2137468df65873fd7e

Node 2
Public address of the key:   0x151f397A6320369Ee2e91c103edE9CD0b9c7ED0b
Path of the secret key file: node2\keystore\UTC--2021-08-25T19-07-10.086164000Z--151f397a6320369ee2e91c103ede9cd0b9c7ed0b
Step 
Record important iformation about the network and geneiss block

Chain ID: 555
Name: arak1
Metamask acct1: 0xd5e9ddeF40A999C25E3B84134e94b2960461BAaE

## Creating the Genesis Block


- run ./puppeth
- Seal using node addresses  (pick one)
- Pre fund address should be your wallet that you intened to fund
- After created-- > Export and save to default directory
--See Screnshot folder

## Initializing Nodes

Using geth, initialize each node with the new network.json.
./geth --datadir node1 init arak2.json
./geth --datadir node2 init arak2.json


## Activate Nodes(This is a POA so they must be unlocked)
Activate node 1 as miner and ledger
Node1

./geth --datadir node1 --unlock "0x263E6Ed688b78713f6996E2137468dF65873fd7e" --mine --rpc --allow-insecure-unlock

Node 2

./geth --datadir node2 --unlock "0x151f397A6320369Ee2e91c103edE9CD0b9c7ED0b" --mine --port 30304 --bootnodes "enode://7d9515d22cd614dd9af0b0301558b7c54572bb5780b53d20096f6e747b7e380a9bcdef5d3e9f75c463f6f1f41255e538ff3fbaa920647dc33306e444ad678b93@127.0.0.1:30303"  --ipcdisable --allow-insecure-unlock

## Transacting
See Screenshot folder for transactions. 


# Networking requirements
Date: 19/10/2022
Today seminar: Hardhat vs RemixIDE and mint NFT
Next seminar: DEX: Uniswap v2 v3

---------------------------------
No centralized server 
- Key:  Broadcast block and tx to all nodes
- Rebutness: Some nodes go off, new node join


## Type of network architecture
- Client - server
- Peer to Peer
  + Not only node join also have middle node to relay connection
- Overlay network
  + Physical network then transform 
  + Virtual topology
  + Pros: Support weak node
  + Cons: Need vera large bandwidth
- Structured overlay network:
  + Example: CHORD
    * Assign a graph node identifier to each node 
    * Well defined peer routing rules
    * O(logN) routing and O(logN) connection per node
    * Pros: 
      * Reduce number of msg
    * Cons:
      * Increase time send msg
      * Vulnerable: Fake msg, ...
- Unstruct overlay network
  + Example: d-regular graph
    * No node grapnh indentifer
    * Connedct to any random

## Gossip and flloding
Ref: Libp2p (Golang)
- Mimic the sperad of an epidemnic
- Once a node is infected it infects its peer
- Info spread exponentially and reaches nodes in O(logN) time

## Bitcoin network
- TCP with peer
- most 8 outbonds TCP
- Accept up to 117 connection
- Maintain a large list of nodes (IP, port) on bitcoin network
- Establishes connection to a subst of the stored nodes

## Peer  discorvery
- Block is broadcast to network using gossip-flooding
- Standard block relay protocol to gossip blocks
- Relay after block validattion
- INv(Blockhash) inventory msg contain blockhash
Chi phu hop voi bitcoin boi vi bitcoin chain ko co state cu the
Khac voi ethereum, mang co 1 state cu the
- Vi the ethereum phai sync state sau do moi sync header cua block moi nhat ve
- Sau buoc tren ether node co the bat dau validate 
- Viec craw lai block truoc do co the lam bat ky luc nao

## Capacity and propagtion delay
Chup hinh trong dien thoai
### Effect of delay
- Wasted hashpower
- Forking



## Solution to improve P2P network topology
- random IP
  - Not related to geographic distianses
- Need a geometric random network
  - IP addr do not reveal
- ...... (ko note kip)

- *Perigee algorhthm*
Add score for realy ntwork
  - Picture: Perfomance of perigee and other (chup hinh trong dien thoai)
- Efficient networking (skip)
- Trusted networks
  - FRN (Fast relay network): Hub and spoke model, trusted server, server are fast

Strange keyword: Deanonymized
# Buoi4 
Anh Hy
Sharding

---------------------------------------------------------------

Remix IDE & Hardhat

Full replication
Consensus : Tính dong thuan
## Strawman approach -> maintain multichain
Multi consensus architecture: Node to shard allocation (N2S):
    After a random time, node will be moved to another node
- Problem: 
  + Security for each shard 
  + After node move to new shard must get all info of this shard 

## Beaconchain
Only save what affect chain, not the user do --> Problem this shard know what that shard did by look ing beaconchain

## State commitment

### Multiconsensus
- Asumption: Each shard has honest majority
- A state commitment is correct is signed by majority in a shard
- OR: a state commitment is correct if a tx including one is finalized in the shard ledger

----------------------------------------------------------------

Homework: Seminar about a problem
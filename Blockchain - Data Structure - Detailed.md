# Blockchain - Data Structure - Detailed
___
### Hash Function
![[Pasted image 20220618033138.png]]

**Why is Blockchain Ledger safe from tampering?**
- Even if one of the **hash pointers** don't match, entire blockchain is invalid
- To fake a transaction, we have to **fake the entire structure**

**Hash Pointer**
![[Pasted image 20220618033149.png]]

**How to create Hash Pointer?**
Use a [[Cryptographic Hash Function]]
Properties required in Hash Function:
- We don't want the person to **guess the previous hash**
	- `y = h(x) guess x`
- We don't want the person to **use another output to deduce the input**
	- we know `x1 and y1 such that y1 = h(x1)`
	- we know that `h(x1) = h(x2)`
	- therefore we know `x2` so we know the hash of the **previous block**
	- by applying this over and over, we know the hash of the genesis block
	- it is now possible to fake the entire blockchain and introduce new transactions

___
### Verify
Verify that `Block B` is a part of the blockchain

- We need to traverse the chain from the head, until we find h(B) in one of the block headers
	- Liner `O(N)` time

- Better way? - [[Merkle Trees]]
	- ![[Pasted image 20220618034142.png|300]]

___

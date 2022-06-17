#export
# Bitcoin Practical Implementation
We know about [[Bitcoin Building Blocks]] now it is time to see how it all functions
___
### Topics
- bitcoin network - **p2p**
	- bitcoin nodes
- bitcoin identity/address - **wallets**
- bitcoin transaction (UXTO)
	- Blocks
	- Transaction types
- bitcoin scripting language - **locking/unlocking**
- bitcoin scalability

___
### Network
- Bitcoin is a **public permissioned** blockchain
- unstructured p2p network
	- all nodes equal
	- overlay network TCP - `port 8333`
	- Communication strategy - **Flooding**

___
### Nodes
- Relay transactions - **flooding**
- Verify transactions - [[Bitcoin Mining]] - [[Proof-of-Work]]
- Add confirmed blocks into blockchain

___
### Addresses
use **base58** encoding
- avoid ambiguity `O` vs `0`

1. Pay-to-pubkey-hash **(P2PKH)**
	- `160 bit` value
	- encoding starts with `1`
2. Pay-to-script-hash **(P2SH)**
	- encoding starts with `3`
	- allows more complex transactions - **multisig**, **smart contracts**, **transaction puzzles**
3. **Bech32**
	- starts with `bc1`
	- more storage efficient, lower transaction fee, better scalability

___
### Balance
- `balance = Σ Unspent Transaction Output (UXTO)`

___
### Transactions
All transactions are **Unspent Transaction Outputs (UXTO)**


In a Blockchain, a trusted third party is responsible for verifying the account balances of the unspent transaction outputs (UTXOs), which avoids double spending.
<span style="color: white; background-color: red ; padding-left: 5px; padding-right: 5px; border: 1px solid red;">
WRONG 
</span>


![[Pasted image 20220618044606.png|600]]

- **structure**
	- `input` - needs to be completely consumed
		- Inputs to a Bitcoin transaction may consist of zero or more **UTXOs**
	- `output`
	- `digital signature` of owner

- **types**
	- **common** - 1 input, 1 output, 1 "change output"
	  ![[Pasted image 20220618044122.png|300]]
	  
	- **aggregating** - multiple inputs, 1 output - `10 $1 to 1 $10` - *wallets*
	  ![[Pasted image 20220618044258.png|300]]

	- **distributing** - 1 input, multiple outputs - `1 $10 to 10 $1` - *payroll*
	  ![[Pasted image 20220618044445.png|300]]

	- **coinbase** - 0 inputs, 1 output - *create a coin*
		- miner's reward

___
### Script
- not turing complete - no loops
	- avoid DoS, logic bombs
- **vs Ethereum** (turing complete)
	- DoS solved by "gas fee" - script stops when gas fee expended
- **types**
	- locking - `ScriptPubKey`
		- place condition on consuming the output in future
			- valid digital signature of owner
			- multisig, puzzle etc.
	- unlocking - `ScriptSig`

___
### Blocks
- `~2000` transactions grouped into a block (merkle tree) for optimization
- **merkle root** stored in block header
- once confirmed using puzzle, block is added
	- `nonce` is the solution to the puzzle
	- solving the hash puzzle - [[Bitcoin Mining]]

___
[[Bitcoin Mining]]
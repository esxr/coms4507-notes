#export
# Bitcoin Mining
___
### Approaches
- [[Proof-of-Work]]
- [[Proof-of-Stake]]

___
### Mining Puzzle
- Probabilistic puzzle - no other strategy
	- Find the right `nonce (32-bit value)` (brute force) to win
- Difficulty adjusted every **2016** blocks (~14 days)
- Average solve time: `~10 days`

___
### Quantitative Analysis
![[Pasted image 20220618051608.png]]



___
### Mining Reward
- Transaction Fees
	- `total output - total input`
	- higher fee = faster transaction
- Block Reward
	- reward for each verified transaction block

___
### Practical Implementation
**[[ASIC Resistant PoW Algorithm]]**
- Use a lot of memory (expensive to implement)
- Aim is to give CPU and GPU mining a chance, going back to the original goal of “one-cpu-one-vote”

**Hash Rate**


**Block Reward**


___
### [[Bitcoin Mining Pool]]
- Mining by yourself
	- you might get $150,000 every 50 years on average, or $300,000 every few thousand years
- Joining a mining pool “smooths out” your revenue stream
	- Without affecting your average return
- ![[Pasted image 20220618053304.png|500]]

___


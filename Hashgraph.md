[[Hashgraph.pdf]]

![[Pasted image 20220618062132.png]]

___
- [ ] **Explain flaw in current implementation**

- [ ] **Explain aim of new technology**
Hedera is designed for fast, fair, and secure applications to take advantage of the efficiency of hashgraph on a decentralized, public network you can trust.

- [ ] **Key features of new technology**

- [ ] **Explain concept behind new technology**
 - Hashgraph uses DAG (directed acyclic graph) structure and BFT model, and assume the network is completely asynchronous.

**EVENT**
![[Pasted image 20220618062307.png|400]]

![[Pasted image 20220618062330.png|500]]

- What it gossips about is gossip itself, which contains not only the transactions, but also the route about how transactions are transferred

**consensus**
- asynchronous Byzantine Fault Tolerant (aBFT)

**virtual voting**
![[Hashgraph 2022-06-18 06.24.52.excalidraw]]

**why it works in asynchronous network?**
Because even the messages can be unbounded latency or dropped, the gossip histories keep unchanged. Sooner or later other nodes will receive it, and it doesn’t require a time limit.

- [ ] **Explain implementation of new technology**

- [ ] **List all solutions based on new technology**

- [ ] **Advantages of new technology**
![[Pasted image 20220618062211.png|300]]

Hashgraph is a math-proved BFT model, which ensures its safety and feasibility. No needs for voting messages and reception, nearly all the transferring messages are valuable transactions, low time complexity. fair and robust transaction orders and timestamps, no special nodes, and resist DDoS.

- [ ] **Limitations/Disadvantages of new technology**
- The ledger structure isn’t as obvious and easy-understanding as Bitcoin, and it needs to trace back the hashgraph to find the information and transaction orders. (mirror nodes)

![[Hashgraph 2022-06-18 06.28.31.excalidraw]]


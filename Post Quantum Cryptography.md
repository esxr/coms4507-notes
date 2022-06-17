[[Post Quantum Cryptography.pdf]]

___
### Usage of public key cryptography
- wherever there is information encryption

___
### Current Algorithms
![[Post Quantum Cryptography 2022-06-17 20.04.23.excalidraw]]

___
### Problems With Current Algorithms
- Quantum Computing solves problems exponentially faster
- Many algorithms which **depend on the time required** to solve computational puzzles will be rendered useless

___
### Threats
- Shor's Algorithm
	- Solves *Integer Factorization* and *Discrete Log Problem* **exponentially** faster
	- Will break **RSA** and **ECC**

- Grover's Algorithm
	- Quantum threat is much less severe for **symmetric algorithms**
	- Problems
		- quantum - costly hardware
		- quantum - slower clock cycles
		- Grover's algorithm cannot be parallelized

___
### Why we should act now
- Quantum computers will defeat current algorithms
- store-now, decrypt later attacks

___
### What is the new technology based on
- ~~Factorization~~
- ~~Discrete log~~
- Lattice
	- *Shortest Vector Problem (SVP)* - Find a shortest non-zero lattice vector
	- *Learning with Errors (LWE)* - Find solution where there is noise
- Code
	- Given corrupted codeword, find original message (Random Goppa decoding)

**Why are they quantum resistant?**
We don't know otherwise
Derived from a regular [[Hash Function]]

A **cryptographic hash function** is a mathematical function that, simply put, takes any input and maps it to a fixed-size string.

![[cryptographic hash functions 2022-06-17 00.12.28.excalidraw]]

However, there are four special properties of these functions that make them invaluable to the Bitcoin network.

___
### Requirements
1. **Deterministic —** for any input into the cryptographic hash function, the resulting output will always be the same.
2. **Fast** — Computing the output of the hash function, given any input, is a relatively fast process (doesn’t need heavy computation)
3. **(Almost) Unique —** no two inputs result in the same output ([[Collision Resistance]])
4. **Irreversible —** Given an output of a hash function, the original input is unable to be obtained ([[Hiding (Cryptography)]])

Properties:
- [[Collision Resistance]]
- [[Hiding (Cryptography)]]
- [[Puzzle Friendliness]]




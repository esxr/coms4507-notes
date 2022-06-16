# Public Key Cryptography
___
### For Noobs
![[Pasted image 20220617011528.png]]


### Method

![[Pasted image 20220616213125.png]]

- Everyone has **your** public key
- Only you have your private key
- If someone needs to send data, they use **your public key to encrypt**
- You then use your private key to decrypt

___
### Problems
- Data tampering
	- Solution: [[Digital Signature]]
- impersonation
	- Charlie creates his own public key and private key, 
	- Charlie claims he is Alice and send his public key to Bob. 
	- Bob will be able to communicate with Charlie, but Bob will think that he is sending his data to Alice.
	- [[Public Key Certificate]]

___
### Algorithms
- [[RSA (Rivest-Shamir-Adelman) Algorithm]] 
	- Create a **mathematically linked** pair of keys
- **What is the main difference between secret-key and public key cryptography?**
[[secret-key cryptography#Method]]
[[public-key cryptography#Method]]

- **What is a digital signature, i.e. what does it provide?** 
	- Digital Signatures prevent forgery of signatures so that Charlie cannot forge Bob's signature while sending messages to Alice
		[[Digital Signature]]
		[[Digital Signature Detailed (Scheme)]]

- **What is a public-key certificate and what is it for?** 
	- Even if Digital Signatures can be used, "Real Charlie" pretends to be "Digital Bob".
	- Alice thinks that no one else can forge the "Digital Bob" in the digital world.
	- But "Digital Bob" is Charlie in the first place 
	- Public Key Certificates prevent that as they are a form of ID issued by a verified authority (CA) so only the real Bob can be the digital Bob
	- Public key certificates link the "Real Bob" to the "Virtual Bob"
	[[Public Key Certificate#Solution to the Problem]]

- **Difference between "digital signature" and "digital certificate"?**
	- Digital Signatures prevent forgery in the digital world
	- Digital Certificates link the real world to the digital world so that a real person can't fake a digital identity

- **What is a “hash collision”?** 
	- [[Cryptographic Hash Function]]
	- [[Collision Resistance]]

- **What can the RSA algorithm be used for?**
	[[RSA (Rivest-Shamir-Adelman) Algorithm]]
	- data encryption of e-mail 
	- other digital transactions over the Internet
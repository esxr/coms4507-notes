# Digital Signature Detailed
___
- required properties of solution
	- only **YOU can make** your signature
		- **ANYONE can verify** that it is valid
	- one signature => one document

![[Pasted image 20220616215514.png]]

![[Pasted image 20220616220535.png]]

![[Digital Signature Detailed 2022-06-16 22.06.13.excalidraw]]

___
### How to Forge Signatures
- What you have
	- **public key** of signer
	- **msg** object
	- **sign(sk, msg)**
	- output of the verify function
		- `verify(pk, msg, sign(sk, msg)) == true`

![[Digital Signature Detailed 2022-06-16 22.22.11.excalidraw]]

- Send `msg = {m1, m2, m3, ..., n}` documents to be signed
	- Get the output of the **verify** function `output = {o1, o2, o3, ... on}`
	- try to deduce the **sign** function based on the given **inputs** and **outputs**
		- [estimate a function based on INPUTS and OUTPUTS](https://math.stackexchange.com/questions/94766/how-to-determine-function-based-on-input-and-output)
	- once you have the **sign** function, you can use it to forge signatures

___
### How to prevent forgery
- If the **sign** function is a [[One-way Hash Function]]
	- **OUTPUT** is not dependent on **INPUT**
	- consequently, **INPUT** cannot be deduced from **OUTPUT**

![[Pasted image 20220616223507.png]]

- If you know `(x1, y1), (x2, y2) ... (xn, yn)
	- you try to deduce `ya` given `xa` you cannot

___
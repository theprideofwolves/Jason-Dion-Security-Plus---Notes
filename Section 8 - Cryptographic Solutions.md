#### Symmetric vs Asymmetric Encryption
Symmetric Algorithm
- Private key - same key
- No non-repudiation, coz a lot of people have the same key.
Asymmetric Algorithm
- 2 separate keys
- slower
- Diffie-Hellman, RSA, Elliptic curve cryptography
Hybrid implementation
- Use asymmetric to share symmetric key.
- Use the shared symmetric key for the rest of the communication.
Apart from the above classification, algorithms can also be categorized as the following:
- Stream cipher
	- Keystream generator is used
	- Bit by bit encryption
	- Uses mathematical XOR function to create cipher text
	- For audio and streaming purposes
- Block cipher
	- Breaks input into fixed length blocks
	- Uses padding to fill out length.
#### Symmetric Algorithms
DES and 3DES
- **DES** 
	- input broken into 64 blocks
	- transposition and substitution
- 3DES
	- 3 separate symmetric keys
	- Increases strength of DES
	- 112 bit length
IDEA
- International Data Encryption Algorithm
- 64 bit blocks
- Used in PGP tools
AES(most commonly used and an industry standard)
- 128 bit, 192 bit, 256 bit blocks
Blowfish
- Block cipher
- 64 bit blocks
Twofish
- 128 bit block
- 128, 192, 256 bit keys
Rivest Ciphers(RC4, RC5, RC6)
- RC4
	- Symmetric stream cipher
	- Variable key size (40 - 2048 bits)
	- Used in SSL and WEP
- RC5
	- Symmetric block cipher
	- Key size upto 2048 bits
- RC6
	- Symmetric block cipher
	- Replacement for DES
	- but got replaced by AES, lol the irony.
#### Asymmetric Algorithms
No shared key needed.
Known as public key cryptography.
Provides
- Confidentiality
- Integrity
- Authentication
- Non-repudiation
To achieve this, a message digest is created using hashing.
Digital Signature
- hash digest of a message is encrypted with sender's private key to let the recipient know the document was created and sent by the person claiming to have sent it.
Diffie-Hellman
- Used for key exchanges over unsecure network
- VPN or IPSEC
RSA
- Mathematically factors large prime numbers
ECC
- In mobile devices
- ECC 256 bit key is as secure as RSA 2048 bit key
- ECDH (Elliptic curve diffie hellman)
	- ECC version of the popular diffie-hellman key exchange protocol
- ECDHE(ECDH Ephemeral)
	- Uses different keys for each portion of key key establishment process in DH key exchange
- ECDSA(EC Digital signature algorithm)
	- US government uses for digital signatures
	- Public key encryption algorithm
- Needs less resources to compute.
#### Hashing
Provides integrity
One - way
Same length digest
MD5
- 128 bit hash value
- unique to the file
- Limited number of hashes
- prone to collision
SHA
- SHA 1
	- 160 bit digest
- SHA 2
	- Longer digests
	- SHA 224, SHA 256, SHA 384, SHA 512
- SHA 3
	- 224 bits to 512 bits digest
	- 120 rounds of computation
RIPEMD - RACE Integrity Primitive Evaluation Message Digest
- 160, 256, 320 bit versions
- RIPEMD 160 is commonly used and open source
HMAC - Hash based message authentication code
- Checks integrity of message
- Underlying hash functions:
	- HMAC MD5
	- HMAC SHA1
	- HMAC SHA256
Digital signature algorithms
- DSA
- RSA
- ECC w DSA or SHA
DSS
- 160 bit
#### Increasing hash security
Attacks on hashes:
- Pass the hash attack
	- using hash to break into a system instead of a password
	- Don't have to brute force
- Birthday attack
	- Utilizes collision
Improve security by:
- Key stretching
	- increasing the time needed to crack it
	- WPA , WPA2
- Salting
	- Add random data into a one way hash 
	- Even if 2 passwords are same, collision wont happened because of salting
- Rainbow tables
	- Precomputed tables for reversing hash functions
	- This is ineffective if salting is used.
 - Nonce
	 - Number used once
	 - Unique number added to password based authentication process
Limit number of failed login attempts.
#### Public Key Infrastructure
Encrypt using receivers public key
Decrypt using receivers private key
PKI and public key cryptography are related but not the same.
PKI
- System that creates asymmetrical key pairs
- Key management
PKC
- the encryption and decryption process
- part of PKI
CA - Certificate Authority
- Issues digital certificates
- Trust is maintained bw all certificate authorities around the world
Key escrow
- Keys are stored in a third party location called escrow.
PKI is a framework for managing digital keys and certificates that facilitate secure data transfer, authentication, and encrypted communications over networks.
PKI uses PKC.
Data exchange on the internet relies on PKI.
#### Digital certificates
- Binds public key with a user's identity.
- Commonly use X.509 protocol standard for digital certificates inside PKI.
- Contain owner or user's info
Types:
- Wildcard certificates
	- allows all subdomains to use same public key certificate and displays it as valid.
	- if revoked, all subdomains are gone. sad!
SAN FIELD - Subject Alternate Name field
Certificate that specifies what additional domains and IP addresses are going to be supported
- Single sided certs
	- Only requires the server to be validated.
- Dual sided certs
	- Requires both server and user to be validated
- Self signed certs
	- Signed by the entity themselves.
	- Prior trust is needed
- Third party certs
	- issued and signed by a trusted CA
	- preferred choice
- Root of trust
	- Each cert is validated using the concept of a root of trust or chain of trust
- Certificate authority
	- trusted 3rd party
- Registration authority - RA
	- Gets info from user and forwards that certificate req up to the CA to create digital certificate.
- Certificate Signing Request
	- block of encoded text
	- contains info about the entity requesting the certificate
- Certificate revocation list
	- list of certificates that are revoked.
	- this is checked first
- OCSP 
	- Allows to determine revocation status of cert using serial number
	- Quicker than CVL
- OCSP Stapling
	- Allows certificate holder to get OCSP record from server at regular intervals
	- Adds it to TLS, speeds up the authenticating process.
- Public key Pinning
	- allows https website to resist impersonation attacks from users who have fraudulent certificates
- Key escrow
	- occurs when a secure copy of a user's private key is being held.
	- needs alot of security
- Key recovery agent
	- Spl sw that allows the restoration of a lost of corrupted key to be performed
#### Exploring digital certificates
#### Blockchain
- Shared, immutable ledger 
- records transactions, tracks assets, builds trust
	![[Pasted image 20251222112044.png]]
Public ledger
- record keeping system
- Identities of participants are anonymous
Smart contracts
- self executing contracts
- Conditions or agreements are directly written into lines of code.
- cant be altered once deployed.
- less risk of fraud
Permissioned blockchain
- used for biz transactions
- using in supply chain - fully traceable and transparent.
#### Encryption tools
TPM - Trusted platform module
- Dedicated microcontroller device
- Secures hardware
- uses integrated cryptographic keys
- Bitlocker etc.

HSM - Hardware Security Module
- Physical device
- Safeguards and manages digital keys that are needed in critical situations
- tamper - resistant
Key management system - KMS
- Integrated approach
- generates, distributes and manages keys for apps and devices 
Secure enclave
- co processor integrated into main processor
- designed for data protection
- shielded location
- Face if, toucher id.
#### Obfuscation
Steganography
- concealing a message within a message
- no suspicion of having a hidden message
- using along with encryption
Tokenization
- substitute sensitive data with non-sensitive data
- common in pcidss
Data masking 
- Data remains recognizable but doesn't include sensitive information
#### Cryptographic attacks
Techniques or strategies that attackers use to exploit vulns in cryptographic systems to compromise CIA of data.
Attacks:
- Downgrade attacks
	- Forces system to use outdated protocols
	- Most systems use backward compatibility, attacker takes advantage of this
	- POODLE attack in ssl 3.0
	- No support for older versions can help
-  Collision attack
	- 2 inputs same output
	- Attacker tries to get same hash using other input to match the Original's file hash value
	- MD5 is susceptible to collision
	- trust and reliability is undermined
- Birthday attack
	- Probability that 2 distinct inputs, when processed through a hashing function will produce the same output or a collision.
Quantum computing
Quantum bits, qbits are used to access enormous computing power.
Quantum communication
- sends multiple combinations of ones and zeros simultaneously.
Qubit
- bit composed of electrons or photos
Quantum computing is good at math. So a risk to cryptography.

Post quantum cryptography
- new cryptographic algorithm
- CRYSTALS-Dilithium, FALCON, SPHINCS+ are some of the post quantum cryptography algorithms.
- 
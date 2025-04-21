


## What is Cryptography?

Cryptography is a technique of securing information and communications through the use of codes so that only those persons for whom the information is intended can understand and process it. Thus preventing unauthorized access to information. The prefix “crypt” means “hidden” and the suffix “graphy” means “writing”. In Cryptography, the techniques that are used to protect information are obtained from mathematical concepts and a set of rule-based calculations known as algorithms to convert messages in ways that make it hard to decode them. These algorithms are used for cryptographic key generation, digital signing, and verification to protect data privacy, web browsing on the internet and to protect confidential transactions such as credit card and debit card transactions.


![[Pasted image 20250130175755.png]]



## Features Of Cryptography

- Confidentiality: Information can only be accessed by the person for whom it is intended and no other person except him can access it.

- Integrity: Information cannot be modified in storage or transition between sender and intended receiver without any addition to information being detected.

- Non-repudiation: The creator/sender of information cannot deny his intention to send information at a later stage.
- 
- Authentication: The identities of the sender and receiver are confirmed. As well destination/origin of the information is confirmed.

- Interoperability: Cryptography allows for secure communication between different systems and platforms.

- Adaptability: Cryptography continuously evolves to stay ahead of security threats and technological advancements.



## Types Of Cryptography


### 1. Symmetric Key Cryptography

It is an encryption system where the sender and receiver of a message use a single common key to encrypt and decrypt messages. [Symmetric Key cryptography](https://www.geeksforgeeks.org/what-is-a-symmetric-encryption/) is faster and simpler but the problem is that the sender and receiver have to somehow exchange keys securely. The most popular symmetric key cryptography systems are [Data Encryption Systems (DES)](https://www.geeksforgeeks.org/data-encryption-standard-des-set-1/) and [Advanced Encryption Systems (AES)](https://www.geeksforgeeks.org/advanced-encryption-standard-aes/) .

![Symmetric Key Cryptography](https://media.geeksforgeeks.org/wp-content/uploads/20240409123909/Private-Key-Encryption-(1)-768.png)

Symmetric Key Cryptography

### 2. Hash Functions

There is no usage of any key in this algorithm. A hash value with a fixed length is calculated as per the plain text which makes it impossible for the contents of plain text to be recovered. Many operating systems use hash functions to encrypt passwords.

### 3. Asymmetric Key Cryptography

In [Asymmetric Key Cryptography,](https://www.geeksforgeeks.org/asymmetric-key-cryptography/) a pair of keys is used to encrypt and decrypt information. A sender’s public key is used for encryption and a receiver’s private key is used for decryption. Public keys and Private keys are different. Even if the public key is known by everyone the intended receiver can only decode it because he alone knows his private key. The most popular asymmetric key cryptography algorithm is the RSA algorithm.

![Asymmetric Key Cryptography](https://media.geeksforgeeks.org/wp-content/uploads/20240409125853/Asymmetric-.webp)

Asymmetric Key Cryptography


## Applications of Cryptography

- Computer passwords: Cryptography is widely utilized in computer security, particularly when creating and maintaining passwords. When a user logs in, their password is hashed and compared to the hash that was previously stored. Passwords are hashed and encrypted before being stored. In this technique, the passwords are encrypted so that even if a hacker gains access to the password database, they cannot read the passwords.

- Digital Currencies: To protect transactions and prevent fraud, digital currencies like Bitcoin also use cryptography. Complex algorithms and cryptographic keys are used to safeguard transactions.

- Secure web browsing: Online browsing security is provided by the use of cryptography, which shields users from eavesdropping and man-in-the-middle assaults. Public key cryptography is used by the [Secure Sockets Layer (SSL)](https://www.geeksforgeeks.org/secure-socket-layer-ssl/) and [Transport Layer Security (TLS)](https://www.geeksforgeeks.org/transport-layer-security-tls/) protocols to encrypt data sent between the web server and the client, establishing a secure channel for communication.

- Electronic Signatures: Electronic signatures serve as the digital equivalent of a handwritten signature and are used to sign documents. Digital signatures are created using cryptography and can be validated using public key cryptography. In many nations, electronic signatures are enforceable by law, and their use is expanding quickly.

- Authentication: Cryptography is used for authentication in many different situations, such as when accessing a bank account, logging into a computer, or using a secure network. Cryptographic methods are employed by authentication protocols to confirm the user’s identity and confirm that they have the required access rights to the resource.

- Cryptocurrencies: Cryptography is heavily used by cryptocurrencies like Bitcoin and Ethereum to protect transactions, thwart fraud, and maintain the network’s integrity. Complex algorithms and cryptographic keys are used to safeguard transactions, making it nearly hard to tamper with or forge the transactions.

- End-to-end Internet Encryption: End-to-end encryption is used to protect two-way communications like video conversations, instant messages, and email. Even if the message is encrypted, it assures that only the intended receivers can read the message.  End-to-end encryption is widely used in communication apps like Whats App and Signal, and it provides a high level of security and privacy for us.



## Types of Cryptography Algorithm

- Advanced Encryption Standard (AES): [AES (Advanced Encryption Standard)](https://www.geeksforgeeks.org/advanced-encryption-standard-aes/) is a popular encryption algorithm which uses the same key for encryption and decryption It is a symmetric block cipher algorithm with block size of 128 bits, 192 bits or 256 bits. AES algorithm is widely regarded as the replacement of DES (Data encryption standard) algorithm.

- Data Encryption Standard (DES): [DES (Data encryption standard)](https://www.geeksforgeeks.org/data-encryption-standard-des-set-1/) is an older encryption algorithm that is used to convert 64-bit plain text data into 48-bit encrypted ciphertext. It uses symmetric keys (which means same key for encryption and decryption). It is kind of old by today’s standard but can be used as a basic building block for learning newer encryption algorithms.

- RSA: [RSA](https://www.geeksforgeeks.org/rsa-algorithm-cryptography/) is an basic asymmetric cryptographic algorithm which uses two different keys for encryption. The RSA algorithm works on a block cipher concept that converts plain text into cipher text and vice versa.

- Secure Hash Algorithm (SHA): [SHA](https://www.geeksforgeeks.org/sha-1-hash-in-java/) is used to generate unique fixed-length digital fingerprints of input data known as hashes. SHA variations such as SHA-2 and SHA-3 are commonly used to ensure data integrity and authenticity. The tiniest change in input data drastically modifies the hash output, indicating a loss of integrity. Hashing is the process of storing key value pairs with the help of a hash function into a hash table.


## Frequently Asked Questions on Cryptography – FAQs

### What is the purpose of Cryptography?

> The purpose of cryptography is to secure and protect sensitive information by encoding it in a way that only authorized parties can understand.

### What are Digital Signatures?

> Digital signatures are cryptographic techniques used to provide authentication, integrity, and non-repudiation for digital documents or messages.

### Can quantum computers break existing Cryptographic Systems?

> Quantum computers have the potential to break existing cryptographic systems due to their ability to solve certain mathematical problems much faster than traditional computers.

### How is Cryptography used in e-commerce transactions?

> Cryptography is used in e-commerce transactions to encrypt sensitive data, such as credit card information, during transmission to ensure its confidentiality and integrity.


-----

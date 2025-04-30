# Understanding Cryptographic Hashes

- A cryptographic hash is a function that converts data into a fixed-length string of text, often referred to as a message digest or digital fingerprint.
- This digital fingerprint is unique to the data it represents, similar to how a human fingerprint uniquely identifies an individual.
- It is important to note that a cryptographic hash is not the same as encryption; it is a one-way function and cannot be reversed to recreate the original data.
- Hashes can be used to verify the integrity of documents by ensuring that the downloaded file matches the original file from a website.
- In addition to integrity verification, hashes are also used in creating digital signatures, which provide authentication, non-repudiation, and integrity for messages.

## Creating and Understanding SHA-256 Hashes

- The SHA-256 hashing algorithm is a widely used cryptographic hash function that generates a 256-bit hash value represented as 64 hexadecimal characters.
- When creating a hash, even a minor change in the input text significantly alters the resulting hash, demonstrating the sensitivity of hashing functions.
- For example, changing a period to an exclamation mark in the input string results in a completely different hash output.
- It is crucial that different inputs produce different hashes to avoid collisions, where two distinct inputs generate the same hash value.
- While collisions are rare with robust hashing algorithms, some older algorithms, like MD5, have demonstrated vulnerabilities to collision attacks, which is why they are not recommended for secure applications.

## The Collision Problem in Hashing

- A collision occurs when two different inputs produce the same hash output, undermining the integrity of the hashing process.
- The MD5 hashing algorithm, identified as having collision issues since 1996, serves as a cautionary example of the importance of selecting secure hashing algorithms.
- Demonstrating this, two nearly identical strings can yield the same MD5 hash, highlighting the critical need for stronger alternatives.
- In practical applications, hashing is used frequently for file verification and password storage, emphasizing the necessity of reliable hashing algorithms to maintain security.

## Practical Uses of Hashing

- Hashing is commonly employed to verify downloaded files, ensuring that they match the original files posted on websites, especially for important files like Linux distributions.
- Each file is associated with a specific hash, allowing users to run a hashing algorithm on their downloaded file and compare it to the posted hash for validation.
- Another significant application of hashing is in password storage; instead of storing passwords in plain text, hashes are stored to enhance security.
- Passwords are hashed along with a unique random value known as a salt, which prevents attackers from easily reverse-engineering the original passwords, even if they gain access to the hashed data.

## Salting Passwords for Enhanced Security

- Salting involves adding random data to passwords before hashing, which ensures that even identical passwords yield different hash outputs due to the unique salt values.
- This technique significantly complicates brute-force attacks, as attackers cannot rely on pre-computed hash tables, known as rainbow tables, to crack passwords.
- By using salts, the time required for an attacker to brute-force a password can increase dramatically, making it a more secure method for password management.
- For example, the password "dragon" would produce different hashes when different salts are applied, demonstrating the effectiveness of this method in protecting user credentials.

## Digital Signatures and Their Importance

- Digital signatures are cryptographic equivalents of handwritten signatures, providing validation that a message has not been altered during transmission.
- They ensure the integrity of the message and authenticate the sender, offering proof that the message was indeed sent by the claimed sender.
- The process of creating a digital signature involves hashing the original message and encrypting that hash with the sender's private key.
- Upon receiving a message, the recipient can verify the digital signature by decrypting it with the sender's public key, ensuring the message's authenticity and integrity.
- If the decrypted hash matches the hash generated from the received message, it confirms that the message remains unchanged and is indeed from the claimed sender.

## The Process of Sending a Digital Signature

- When Alice wants to send a signed message to Bob, she first hashes the message and then encrypts the hash to create the digital signature.
- The original message is sent in plain text alongside the digital signature, which can be verified by the recipient.
- Bob, upon receiving the message, will use his email client to verify the digital signature, which involves decrypting the signature using Alice's public key.
- The email client compares the decrypted hash with the hash of the received message to confirm whether they match, thus validating the integrity and authenticity of the message.
- This process illustrates the seamless integration of cryptographic techniques in everyday communication tools, ensuring secure and reliable exchanges of information.


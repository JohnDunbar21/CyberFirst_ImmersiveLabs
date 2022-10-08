# Hashing

## Quick Summary
Hashing is a mathematical function that converts any form of data into a unique string of characters and numbers. Appearing in almost all information security applications, they are extremely useful for checking data integrity.

### What is Hashing?

Hashing is the process of converting a given piece of data into another value, known as a hash, for the purposes of checking data integrity. Any piece of data can be hashed, and the generated hash will always be the same length, no matter the data's size or type.

A hash is designed to act as a one-way function; data put into a hashing algorithm produces a unique string, but a hash cannot be deciphered to the input data it represents without knowing the original data.

Hashing is everywhere. For example, when creating an account for a prominent website, the provider may run your password through a hashing algorithm and save the hash of your password. However, even if an attacker were to access this hash, they would not be able to log in as you. Access is only granted when the hash for the input password matches that stored in the database.

### Why is Hashing Important?

Hashing operates in one direction only, making it extremely difficult to deduce the original data from the resultant hash. The intention of hashing is not to preserve the contents of the data, but to create a unique identifier for every single piece of data. This is so that when someone sends a file to another user, the recipient can generate a hash of the file to ensure it hasn't been modified or tampered with prior to reaching them. Similarly, when a file is published on the internet, the author may choose to publish the hash value for that file so that others can download the file, generate a hash and verify that it's the same as the original.

### Common Types of Hashing

Hashing is also used in data encryption. Passwords can be stored in the form of their hashes so that even if a database is breached, plaintext passwords are not accessible. **MD5**, **SHA-1**, and **SHA-2** are popular cryptographic hashes:

* **MD5** was invented by Ronald Rivest and is 128 bits in length, normally shown in their 32 digit hexadecimal value equivalent. MD5 checksums are built to be non-reversible, meaning they can't be used to identify the original inputted data.
* **SHA-1** is often used to verify that a file has been unaltered. This is done by producing a checksum before the file has been transmitted, and then again once it reaches its destination. It has a 160 bit message digest (hash value) size and was the first version of this algorithm.
* **SHA-2** was pubished in 2001, several years after SHA-1. SHA-256 is used in some of the most popular authentication and encryption protocols, including SSL, TLS, IPsec, SSH, and PGP. Cryptocurrencies such as Bitcoin use SHA-256 for verifying transactions.

### How Does Hashing Work?

Websites using hashing typically flow like this:

1. A user creates an account
2. Their password is hashed and stored on the database
3. When the user attempts to log in, the hash of their entered password is compared to the hash stored in the database
4. If the hashes match, the user can access the account
5. If the hashes do not match, a generic error message is sent back such as "Invalid credentials" so hackers can't trace the error to the username or password specifically

### Hashing in Encryption

Thanks to computer technology and the internet, we can now practice public key cryptography. This is where one public key is used to encrypt and the other private key is used to decrypt, making it a two-way function practice.

The most common forms of encryption are:

* **Asymmetric Key Encryption** - This is the public key where one key encryots and another decrypts. The encryption only goes one way.
* **Symmetric Key Encryption** - This is the private key used for an encryption algorithm where the key we use to encrypt the data is the same used to decrypt the data.
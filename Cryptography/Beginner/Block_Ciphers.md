# Block Ciphers

## Quick Summary
Particularly good for encrypting large amounts of data without compromising security, block ciphers are often used in symmetric-key encryption as an underlying algorithm.

### What Are Block Ciphers?

A block cipher is a type of encryption method often used in symmetric-key encryption algorithms. They have been widely used since 1976 and are still used today as an underlying algorithm.

Block ciphers have different modes of operation for things like improved security, efficiency, and error checking, yet they all do the same thing: encrypt data.

### How Do Block Ciphers Work? (Encryption)

#### The Basics

Block ciphers are relatively straightforward and work as two separate processes, one that encrypts and one that decrypts. At the base level, the encryption side of the algorithm takes a plaintext message and runs it through the block cipher encryption with the key to generate ciphertext, known as a block. This key is the same used throughout the block cipher encryption process.

#### Bits

Taking a step up from the absolute basics, block ciphers work in specified bit lengths. If your plaintext message is over a certain bit length, it will split the message into separate parts, known as plaintext bits. These plaintext bits are run through the block cipher algorithm to spit out ciphertext bits. The length of the bits is determined by the type of block cipher algorithm, not the original plaintext message. For example, if a plaintext message equalled 174 bits and your block cipher worked in 64-bit blocks, the result would be three blocks of ciphertext.

#### Padding

If the plaintext message requires multiple ciphertext blocks, but is not big enough to fill those additional blocks, padding is inseerted so that all ciphertext blocks are the same length. Working with the above example of 174 bits of plaintext, we would have two 64-bit cipher blocks and one 46-bit cipher blocks which will be padded to 64-bits prior to being run through the block cipher (this can be at the beginning or end of the plaintext message).

It's important to note that padding should not be added to the same sections each time (i.e. at the end of each plaintext block), or the security of the block cipher could be reduced as it becomes predictable.

#### Initialisation Vectors

Block ciphers can use initialisation verctors (IV) to prevent any two blocks from being exactly the same. If using an IV, the value is required to be random or pseudorandom in order to achieve a high level of security. Ensuring the IV is unique and unpredictable prevents the attacker from gaining access to the key and being able to decrypt the already encrypted information. The way IVs are used depends entirely on the cipher and method of operation. One way is to use the previous block as the initialisation vector for the next block's ciphertext.

Take your plaintext, split it into three blocks using the 174-bit example again, and parse it through the initialisation vector before using the block cipher encryption and chosen key. The ciphertext output is then the IV for the second block. So on your second block, you would take the second plaintext block and pass it through the initialisation vector (which is your first block of ciphertext) before parsing it through the block cipher algorithm and key. Rinse and repeat for the rest of the blocks.

### How Do Block Ciphers Work? (Decryption)

The decryption process for block ciphers is effectively the opposite of the encryption. The block ciphertext is put through the key and decryption algorithm to produce the original block of plaintext. The initialisation vector is still used before the plaintext is generated, towards the end of each block process rather than the beginning. The same key that was used to encrypt is also used to decrypt.

### Cryptocurrency Schemes That Use Block Ciphers

There are a number of encryption standards and cryptographic algorithms that use block ciphers as their basis:

* Triple Digital Encryption Standard (3DES)
* Advanced Encryption Standard (AES)
* TwoFish
* Serpent
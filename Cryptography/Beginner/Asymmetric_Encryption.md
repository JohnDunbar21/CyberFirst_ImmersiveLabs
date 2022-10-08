# Asymmetric Encryption

## Quick Summary
Asymmetric encryption is where a pair of keys - one public and one private - are used for both encryption and decryption. First presented in 1976 at Stanford University, asymmetric encryption was created to solve the problem of key distribution.

### What is Asymmetric Encryption?

Asymmetric encryption is a process in which a pair of keys are used to encrypt and decrypt a message to protect it from unautherised access or use. Sometimes referred to as public-key encryption, it was created and presented at Stanford University in 1976 as a result of problems concerning key distribution and sharing, thus putting security of encrypted data under threat.

### How Does It Work?

In asymmetric encryption, each user has two keys - a public key and a private key. A public key can be used by anyone to encrypt a message so that it can only be deciphered by the intended recipient with a private key. A private key - also known as a secret key - then decrypts the message, not sharing it with anyone else.

To understand asymmetric encryption further, here is a simple example:

You are working at a spy agency. You have an undercover agent who needs to send their reports to HQ securely. Using asymmetric encryption, you can create a public key for the agent to encrypt their reports. Every key is mathematically linked to **only one** private key. The private key that is linked to the agent's public key can then be used at HQ to decrypt the message, providing a secure one-way communication method.

Typically, asymmetric encryption is used to authenticate data using digital signatures. The Digital Signature Algorithm (DSA) is a type of public-key encryption algorithm and is used to generate an electronic signature.

A digital signature validates the authenticity of a message and therefore provides evidence for the identity, origin, and status of a message. This means a recipient can verify that a message has come from a particular sender. By using a digital signature, we can achieve non-repudiation: this is assurance that the sender of information is provided with proof of delivery and the recipient is provided with proof of the sender's identity, so neither can later deny having processed the information.

Asymmetric encryption is focussed on protecting the confidentiality of a message, yet encryption does not necessarily protect the integrity of a message. Because of this, digital signatures use encryption combined with **hashing** to validate the integrity of a message.

Asymmetric encryption can be applied in systems that numerous users may need to simultaneously encrypt and decrypt messages. An example of this would be an encrypted email, with a public key being used to encrypt the message and a private key used to decrypt it. The issue previously found with key distribution is eliminated and security is increased as there is no exchanging of keys and private keys remain secret.

Bitcoin and other cryptocurrencies also use this encryption algorithm. Users have public keys that everyone can see and the private keys are kept secret. This algorithm ensures that only the owner of a Bitcoin wallet can withdraw or transfer money from it to spend the funds.
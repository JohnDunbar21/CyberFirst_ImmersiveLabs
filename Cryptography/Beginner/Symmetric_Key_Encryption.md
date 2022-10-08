# Symmetric Key Encryption

## Quick Summary
Symmetric-key encryption uses the same key for both encryption and decryption. Based on how messages were passed between armies in ancient times, this method of encryption is still widely used today.

### What Is Symmetric-Key Cryptography?
Symmetric-key encryption, is where the same key is used to both encrypt and decrypt a message or data. Sometimes referred to as ‘secret’ or ‘private-key’ cryptography, the strength of symmetric-key encryption lies in the strength of the key generated and its management. Block and stream ciphers are two main encryption types used with symmetric-key cryptography. AES, DES and Triple DES are some of the more commonly used symmetric-key algorithms.

### How Does Symmetric-Key Cryptography Work?
Symmetric-key encryption takes a key then uses that key to encrypt the data or information the user wishes to protect.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/4nOmEACCCli56i9rfQKtxwjbIt2NYWnknkA9Mve24qs.png">

The user operates the same key to decrypt the data.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/uKnk1UtBZA4eB3FbfAefOCvvQLgdPPhDx-uDbjMqMVM.png">

But if that key was shared or no longer private, anyone with that key would be able to decrypt the data encrypted with it.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/FwCp8JEmJ-1OeidaW7sNGOOpwCepj4E4dF3rHMOlHZI.png">

Normally when using symmetric-key encryption, a new key would be generated for each new entity that data needs to be shared with. Unfortunately if one of these keys falls into unauthorised hands, it's possible for the data to be decrypted, read and re-encrypted with a new key by the unauthorised person. Giving keys an expiry or a life cycle can help combat the presence of older keys and reduce unauthorised entities from being able to decrypt and read the data.

Despite the potential risks, symmetric-key encryption has its benefits. It's more efficient to process and generate keys than its counterpart, asymmetric-key encryption, and is therefore more popular when large amounts of data need to be encrypted. An added bonus is that keys tend to be smaller yet offer a significant level of protection when managed properly. It's also possible to use symmetric-key encryption with other encryption methods. For example, you could encrypt large amounts of data with symmetric-key encryption, then encrypt the key with asymmetric-key encryption.

### Symmetric Key Management
The management of keys is important in symmetric-key encryption, so knowing how to manage these keys is crucial. Luckily the National Institute of Standards and Technology (NIST) has a three-part standard series, NIST 800-57 Recommendations for Key Management, that you can follow.

Large companies such as Amazon have their own key management systems (KMS) and guidelines, often based on the guidance of standards.
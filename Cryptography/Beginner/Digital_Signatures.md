# Digital Sigantures

## Quick Summary
A digital signature is a technique used to validate the authenticity and integrity of a message, software, or digital document. By verifying the identity of the signer using a digital signature, security issues connected to the transmission of public keys can be minimised.

### What Are Digital Signatures?
Digital signatures are in essence electronic fingerprints. Like handwritten signatures or fingerprints, they are unique to each signer or entity. In the form of a coded message, the signature associates a signer with a document, and can therefore provide evidence of origin, identity, and status of electronic documents, transactions, or digital messages. Digital signatures use a standard format, called Public Key Infrastructure (PKI), to provide the highest levels of security and universal acceptance. PKI requires the provider to use a mathematical algorithm to generate two long numbers, called keys. One key is public and one key is private.

### How Do They Work?
When a signer electronically signs a document, the signature is created using the signer’s private key, which is always kept securely by the signer. The mathematical algorithm creates data matching the signed document called a hash and encrypts that data. The resulting encrypted data is the digital signature. The hash generated is unique to the document, and changing any part of the document will completely change the hash.

Once sent, the recipient of the document generates their own hash of the document and decrypts the signer's digital signature using the signer’s public key (which can be available and verified in a key repository) to retrieve the original hash. The recipient then compares their own hash and the signer’s hash; if they match, the document has not been modified and the sender is authenticated. If they do not match, it indicates that the document has been changed after signing, and the digital signature is invalid. Additionally, if we use a known, verified public key of the expected sender (one that is in a key repository) digital signatures can also verify that the sender is who they claim to be.

The process behind a digital signature is therefore as follows:

1. The signer creates a hash of the data they wish to send
2. The signer encrypts this hash using their private key; this is the digital signature
3. The signer sends the original data along with the digital signature

Then the recipient has a similar set of steps:

1. The recipient receives the original data and the digital signature
2. The recipient generates a hash of the original data
3. The recipient decrypts the digital signature using the signer's public key to retrieve the hash the signer originally generated
4. The recipient compares the original hash to the one they have generated. If the hashes are the same, the document has not been modified and the sender is authenticated

#### Example
Jane signs an agreement to sell a timeshare using her private key. The buyer receives the document and a copy of Jane’s public key. If the public key cannot decrypt the signature, it means the signature isn’t Jane’s, or the document has been changed since it was signed. The signature is therefore considered invalid.

### What Are They Used For?
Using digital signatures with Public Key Infrastructure (PKI) improves integrity. PKI uses a public and private key pair for digital identity authentication by validating that a key belongs to a sender. The public key repositories verify the identity of someone before allowing them to upload their public key. A recipient can then retrieve the public key of the expected sender from the repository and use the digital signature to confirm both the integrity of the document and its origin. This then helps prevent forgery or changes to the document after signing and increases the transparency of online interactions to ensure trust between customers, business partners, and vendors.

As paperless, online interactions are used more widely, digital signatures can help you secure and safeguard the integrity of your data. By using these signatures, the following assurances can be provided:

* **Authenticity**: The proclaimed signer is confirmed as the real signer
* **Integrity**: The content has not been tampered with or altered since it was signed
* **Non-repudiation**: Proves the origin of the signed document to all parties (repudiation refers to the act of a signer denying any association with the signed content)

Digital signatures are commonly used for financial transactions, contract management software, email service providers, and in other cases where it is important to detect forgery or tampering.
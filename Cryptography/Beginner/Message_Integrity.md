# Message Integrity

## Quick Summary
Message integrity describes the concept that a message has not been tampered with or altered in transit from the intended party. While encryption protects the confidentiality of a message, it does not necessarily protect the message's integrity.

### Message Integrity And Cryptography
Message integrity is the assurance that the message transported has not been altered or tampered with. A message has integrity when the payload sent is the same as the payload received. Sending a message confidentially, even through encryption, does not guarantee data integrity, as this could be compromised during the transmission of a message.

There are occasions where messages may not strictly need confidentiality but must have integrity. For example, Alice may write a will to distribute her estate upon her death, but the will does not need to be encrypted because anyone can examine the will after she has died. However, the integrity of the will needs to be preserved so that the contents of the will are unchanged.

When sensitive data is exchanged, the intended recipient must have the assurance that the message has come intact from the intended sender and has not been modified (inadvertently or otherwise). There are two different types of message integrity threats:

**Passive Threats**: These data errors are likely to occur due to noise in a communication channel, or the data may get corrupted while the file is stored on a disk.

**Active Threats**: These threats happen when an attacker manipulates the message with malicious intent.

Security mechanisms, such as hash functions, are used to tackle the active modification threats.

### How Does It Work?
One way to preserve the integrity of a document is through the use of a fingerprint. For example, if Alice needs to ensure the content of her document is not changed, she can put her fingerprint at the bottom of the document, as no one can forge her fingerprint. We can therefore compare Alice’s fingerprint on the document with Alice’s fingerprint on file.

The electronic equivalent of the document and fingerprint pair is the message and digest pair. A message is passed through an algorithm called a cryptographic hash function to preserve integrity. This is the most common approach to ensure message integrity, as the hash function creates a compressed value of the message that can be used as a fingerprint.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/wAqJfpcPnxE8MYU4CVSaAgXPpSQeZvp5DvVSRM_ZNEk.png">

The two pairs (document/fingerprint and message/message digest) are similar but with some differences. The document and fingerprint are physically linked. The message and message digest can be unlinked separately, and most importantly, the message digest needs to be safe from change.

The message digest is created at the sender site and is sent with the message to the receiver. To check the integrity of a message or document, the receiver creates the hash function again and compares the new message digest with the one received. If both are the same, the receiver is sure that the original message has not been changed.

This process is depicted in the following illustration:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/_Gdh6kt4eH1CfpwjoDbXTednjaejujVJ0M8KzYNKuDg.png">

Message integrity is important because recipients need to be sure that the message digest they receive has not been tampered with or changed while in transit. The use of a cryptographic hash function therefore allows recipients to cross-reference the original digest and the received message to check that they are identical. If the digest is different, we can assume that it has been intercepted during transit and changed, thus invalidating its integrity.
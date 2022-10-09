# Collection: Ensure Integrity

## Quick Summary
After acquiring the data, you need to verify its integrity to prove that the data is trustworthy and has not been tampered with. In this lab, we'll look at what integrity verification is, how it's performed, why it's important for evidence, and the tools we can use to verify integrity.

### Integrity verification
What is integrity verification?
Ensuring the integrity of evidence during collection is a critical part of a forensic investigation. This process, which involves checking whether the evidence is the same as that found at the crime scene, can be applied to any form of forensic investigation. Integrity verification isn't exclusively related to a digital investigation, which is why all forms of evidence have to be stored securely with the chain of custody appropriately filled. 

### How is integrity verified?
To verify the integrity of a digital file, you can use cryptographic hashing algorithms to calculate the hash of the file, also known as a message digest. A hash is a unique string of characters and numbers generated for a file. You should calculate the hash of a file as soon as you've acquired the evidence. You can verify if the evidence is the same by creating another hash of the file at a later time and comparing it to the original one. If the hashes match, you can ensure the evidence has not been changed or tampered with. Hashing is an effective method of checking if the evidence is the same because even if the slightest change has been made, the hash is likely to be completely different. 

Some cryptographic hash functions are more secure than others. For example, Message-Digest 5 (MD5) is not considered to be secure due to weaknesses in the algorithm. SHA-256 (part of the secure hashing algorithm family) is a more up-to-date and secure hashing algorithm. However, both of the hashes are used in forensics. According to the National Institute of Standards and Technology (NIST), some standards and basic requirements are involved when it comes to cryptographic hashing algorithms: 

* The hash can be calculated quickly.
* The hash must be collision-resistant. This means that it would take an unreasonable amount of time and computations to have two different files with the same hash.
* The original message cannot be recovered or reconstructed based on the hash.
* Any change to the original file should also change the hash value. A one-byte change to the original file should cause around half of the hash bytes to change, on average.

### The importance of integrity verification
Verifying file integrity is critical to an investigation because if the evidence is not verified or the verification fails, it's considered inadmissible in court. Admission of evidence in a court case could be a deciding factor for the jury or the judge. Maintaining a high level of physical security, a chain of custody, and using hashing techniques are crucial to preserving the integrity of evidence.

### Tools for integrity verification
On Linux systems, there are inbuilt digest computation commands that can be used in the terminal, such as md5sum and sha256sum. PowerShell on Windows systems offers the get-filehash command, which can be parsed with a specific hashing algorithm but defaults to sha256.

HashCalc is also a popular tool supported on Windows machines. This can compute multiple digests of a file using a variety of hash algorithms.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/xiG6XpKfb02gq0LeztPlOHBFM-rE11UW35cfFzC4Wz0.png">
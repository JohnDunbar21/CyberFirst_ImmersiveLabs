# Anti-Forensics Techniques

## Quick Summary
Interpreting and analyzing evidence can be challenging if an attacker has decided to tamper with any of the forensics artifacts.

### Anti-forensics techniques
Analyzing evidence can be challenging, as attackers will sometimes use methods to tamper with artifacts to confuse or mislead a digital forensics investigator. These methods are known as **anti-forensics**. Attackers can be smart when it comes to covering their trail, so to be a good investigator, you need to be smarter. 

### Manipulating timestamps
Timestamps are an important artifact in forensics investigations. They help with creating timelines and provide context to events. Every time you create or modify a file, the time of that action will be recorded in the metadata of the file. 

Attackers can change this timestamp to match other files in the same folder, so it doesn’t look out of place; hiding in plain sight. This is known as **timestomping**.

### Hiding data
Skilled attackers may be able to conceal information in different media files. This technique is called **steganography**. There are different types of steganography for each type of media file. Concealing information in images is considered to be the more traditional approach to steganography, but in more recent years, video and audio steganography have also become quite popular. 

Finding these files can be challenging, but there are tools available that make this process easier, such as Binwalk and Steghide.

### Encryption
Encrypting files contributes to the security of systems, but, unfortunately, this technique is also used by threat actors. Encryption is a classic method of preventing forensic analysts and their tools from viewing or analyzing malicious files. 

Typically, to decrypt and read an encrypted file, you need the secret key or password. Criminals will often encrypt files or even entire disks containing valuable investigation data. This is often seen in the form of ransomware, where attackers use custom tools to infect systems and encrypt data, demanding a ransom from organizations in exchange for the key. 

It's possible to acquire encrypted data during the forensics process but decrypting it without a key is a very difficult task; even impossible if the encryption method is strong. 

### Spoofing
Attackers will often disguise themselves as a legitimate device or a user to trick tools and investigators. Using this method, they can modify various artifacts and protocols. 

IP spoofing is one of the most popular methods of spoofing, where attackers will modify network packets to alter their source IP, pretending that the data comes from another place. Spoofed emails (known as phishing emails) are also another variant where attackers may appear to come from a valid source, asking for sensitive information. 

To identify spoofed emails, you can check if the sender's name matches the email address. You can also check the email header and analyze it using tools like the Google Toolbox – Messageheader and Azure's Message Header Analyzer for more details about the email.

### File-wiping
File-wiping refers to the process of identifying the remnants of a deleted file in unallocated disk space and overwriting them with random data, making them unrecoverable. There are many software applications available that facilitate this, such as Eraser or WipeFile. If one of these is found on a device during an investigation, it may indicate that potentially incriminating files have been wiped. Despite being capable of anti-forensics, these tools are often perfectly legitimate as they can be used to prevent cybercriminals from recovering your personal data if you decide to sell your device.

It's important to note that wiper malware does exist and is a very serious threat, so make sure you select a trusted wiper software should you decide to install one. Wiper malware can be disguised as ransomware, so when you think your data has just been encrypted, it may actually have been wiped. 

In 2017, a series of attacks were carried out using a variant of the Petya ransomware. Petya was modified to wipe files rather than encrypt them, which meant that they couldn’t be recovered, even if the ransom was paid.
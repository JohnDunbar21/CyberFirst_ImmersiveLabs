# WPA Wordlist Crack

## Quick Summary
If an attacker captures the four-way handshake when a device connects to a Wi-Fi network (using eavesdropping equipment, for example), they can try to guess password attempts to calculate elements of the four-way handshake, and therefore identify the original password used.

### What's on this page?
In this lab
Brute forcing with Aircrack-ng
IEEE-802.11i

### In this lab
In this lab you will have access to a network capture from a WPA2-personal protected network. Your tasks are to crack the capture using tools on the machine and identify the passphrase. The word-list to use is rockyou.txt located in /usr/share/wordlists/rockyou.txt

### Brute forcing with Aircrack-ng
Aircrack-ng is a tool suite used to assess network security. Used by penetration testers, it can capture wireless traffic, fake access points and crack WPA/WEP networks that use pre-shared keys. 

Brute forcing is time intensive, and it uses lots of processing power. Creating a word-list is similar in this respect. 

It is important that the word-list contains the correct password, or Aircrack-ng will not be able to determine the key.

Running a dictionary attack against a capture file with Aircrack-ng is quite straightforward: simply specify the word-list and the .cap file you wish to crack, and Aircrack-ng will iterate through the list and identify the correct passphrase.

aircrack-ng -w <WORDLIST FILE> <CAPTURE FILE>

### IEEE-802.11i
The IEEE is a standard for wireless networks that provides a level of improved encryption. 802.11i utilised TKIP (Temporal Key Integrity Protocol) and AES (Advanced Encryption Standard) as its new encryption key protocols.

A four-way handshake is a type of authentication protocol used for wireless local area networks (WLANS). The main purpose of the four-way handshake is to send messages between an access point and a client on the network securely.
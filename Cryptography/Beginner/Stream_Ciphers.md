# Stream Ciphers

## Quick Summary
A stream cipher is one of two popular methods of encrypting data within symmetric encryption algorithms. Created in 1987, stream ciphers encrypt one bit of data at a time to bulk secure your data.

### What Are Stream Ciphers?
Stream ciphers break a plaintext message down into single bits, which are then converted individually into ciphertext using key bits. They encrypt plaintext messages by applying an encryption algorithm with a pseudorandom cipher digit stream (keystream) using an exclusive-or (XOR) operation. This means each bit of the message is encrypted one by one with the corresponding keystream digit to give a digit of the ciphertext stream. Also known as a bulk cipher, this is a method of symmetric encryption that allows you to bulk secure your data one bit at a time, rather than waiting for a data block to form.

### How Do They Work?
Imagine you are encrypting a book. You have the option to encrypt the content one page at a time (block cipher, which is discussed in the next lab in the series) or one letter at a time (stream cipher).

Instead of encrypting a message with a key, stream ciphers input a key into a pseudorandom bit generator to generate a keystream. A keystream is a sequence of pseudorandom digits that extend to the length of the plaintext in order to uniquely encrypt each character based on the corresponding digit in the keystream. Using the keystream and plaintext together, we then use XOR to actually perform the encryption by flipping bits of plaintext to get to the ciphertext. This process is used in the encryption and decryption of data in a given stream cipher algorithm.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/n4vclQh6ooDNc8lq3eYC6FcNzda6oo-igjfLkjOfFIE.png">

Here is an example of a stream cipher. Imagine we have a secret message that is 10 bits in size. We will use a key to generate a pseudorandom keystream that is the same length as what we want to encrypt. In this case, it will also be 10 bits:

```
Data:          0010110111
Keystream:     1001100001
```

This keystream is completely random and is always as long as the actual data that needs to be encrypted. To encrypt the data, the algorithm then uses an XOR operator, which works by taking two bits and comparing them:

```
00 -> 0
11 -> 0
01 -> 1
10 -> 1
```

If two bits are both 0 the outcome will be 0. If the two bits are both 1 the XOR operator will also output 0. Only when one of the bits is a 1 and one of them is a 0 (in any order) will the XOR operator output be 1. The XOR operator therefore checks for exclusivity. The stream cipher performs this XOR operation on the first bit, then the second, then the third, and so on through the entire message. It will XOR the bits of the message with the bits of the keystream, which will form our ciphertext:

```
Data:           0010110111
Keystream:      1001100001
XOR     
Ciphertext:     1011010110
```

We can then send this ciphertext to the recipient.

As stream ciphers are a method of symmetric encryption, the same key is used to both encrypt and decrypt data. To decrypt this message, you'd simply switch around the encryption process. XOR the ciphertext with the keystream to get the original message:

```
Keystream:      1001100001
Ciphertext:     1011010110
XOR     
Data:           0010110111
```

### Different Types Of Stream Ciphers
There are two types of stream ciphers that differentiate how keystreams are generated:

1. **Synchronous stream ciphers (a.k.a key autokey, or KAK)** — These types of ciphers generate keystreams independently of any previous plaintext or ciphertext. This means that the stream is generated pseudorandomly outside of the context of what's being encrypted.

2. **Self-synchronizing stream ciphers (a.k.a asynchronous stream ciphers, ciphertext autokey or CTAK)** — These ciphers, on the other hand, rely on previous ciphertext bits to generate keystreams.

### Where Are Stream Ciphers Used?
Stream ciphers are frequently utilised for their speed and flexibility of usage in equipment and in applications where data comes in quantities of unknowable length, like in a secure wireless connection. Wireless technologies use stream ciphers as one of their security systems for secure communication, as they more naturally fit a streaming model than transmitting data in larger, fixed-size chunks (block ciphers). Examples include the A5/1 stream cipher being used in GSM (Global System for Mobile Communications) phones and the RC4 stream cipher that's been used in the security system for wireless local area networks. Bluetooth connections and 4G connections similarly use this type of encryption for the same reasons.

Stream algorithms are faster and more efficient than block ciphers because they encrypt just one bit of data at a time into individual symbols rather than entire blocks. This means they’re better suited for devices that have fewer resources. Also, as a result of this single-bit-of-data approach, if there’s an error in one symbol, it’ll be less likely to affect the next.

### How Can Stream Ciphers Be Vulnerable?
Some stream ciphers are vulnerable to bit-flipping (a type of man-in-the-middle attack) and key reuse attacks. A bit-flipping attack occurs if the attacker knows the format and portions of the plaintext message. If known, they can anticipate where parts of the message will be and potentially modify the encrypted message without the key. For example, if a ciphertext decrypts to "Transfer £1000”, then a middleman can flip a single bit in order for the ciphertext to decrypt to “Transfer £9000” because changing a single character in the ciphertext does not affect the state of a synchronous stream cipher.

Stream ciphers are also vulnerable to key reuse attacks if the same key is used twice or more. If you have two ciphertexts encrypted with the same key, XORing these together will eliminate the keystream entirely, leaving you with the XOR of the original plaintexts. In the 1940s and 1950s American cryptanalysts decoded thousands of Soviet spy messages and helped uncover espionage at the Manhattan Project as the Soviets made the mistake of reusing keys. For this reason, keys should never be reused for encryption.
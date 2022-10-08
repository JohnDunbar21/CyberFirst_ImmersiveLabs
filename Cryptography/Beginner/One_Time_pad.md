# One-Time Pad

## Quick Summary
A one-time pad is a form of symmetric encryption that closely resembles a stream cipher. As the only existing mathematically unbreakable encryption, the one-time pad has been historically used by KGB officers and various spy organisations and is still in use today in digital versions.

### What Is A One-Time Pad?
The one-time pad cipher is an unbreakable cipher in which the key is exactly the same as the length of the encrypted message. The key is made up of random symbols and as the name suggests, it's used one time only and never again for any other message to be encrypted. The key used for a one-time pad cipher is called 'pad' and comes from early implementations where the key material was distributed as a pad of paper, so the top sheet could be easily torn off and destroyed after use.

### How Does A One-Time Pad Cipher Work?
With a one-time pad, each bit or character from the plaintext is combined by a modular addition with a bit or character from a secret random key (or ‘pad’) of the same length as or longer than the plaintext, resulting in the ciphertext. This ciphertext, therefore, has no relation with the plaintext when the key is unknown. To encrypt a message we need either a Vigenere table or a modulo 26 calculation.

A Vigenere table looks like the following:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/ITvvxTrxW2ckTujfeMdY5-DaY2LMndi0_vjczJp2RuA.png">

To encrypt a letter, we write the key underneath the plaintext. We take the plaintext letter at the top and the key letter on the left. The cross-section of those two letters is the ciphertext. In the first letter example below, the crossing between the plaintext T and key X is ciphertext Q.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/M7M1QD1h0ghH1J_WSkp4iIF1lBme_ZEtQ0vsuK22E_M.png">

To decrypt a letter, we take the key letter on the left and find the ciphertext letter in that row. The plaintext letter is at the top of the column where you found the ciphertext letter.

Another way to calculate one-time pads is by using a modulo 26 calculation. We assign each letter a numerical value (ie. A=0, B=1, C=3 and so on through Z=25) to create the following table:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/GOxG6M3sI4_Ym2DMJlLqb_Ymp_-qUo9TYxUIaCP5BtM.png">

Text and key values are added together with modulo 26: if a value is more than 25, we subtract 26 by that value. Finally, we then convert the result back into letters. To decipher the message, we convert the ciphertext and one-time pad key into numerical values and subtract, by modulo 26, the one-time pad from ciphertext: if a value is less than 0 we add 26 to that value.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/FNwX8cBRaDoKFaVZBI99wJXqvzGWiZT1zMf-3BNzoa0.png">

To encrypt by addition, take the example above: **T(19) + X(23)**. The total of 42 in the conversion table represents the letter Q which is the encryption result. To decrypt by subtracting we then take **Q(16) - X(23)**. If the result would give a negative value (which is the case here) we take the greater equivalent of Q(16), which is 42 in the table. We can now find the deciphered letter with **Q(42) - X(23) = T(19)**.

The rules for unbreakable one-time pad encryption are as follows:

* The key should consist of truly random symbols.
* Only two copies of the one-time pad should exist (one for the sender and one for the receiver).
* The one-time pad should only be used once.
* Both copies of the one-time pad are destroyed immediately after use.

### Where Are One-Time Pads Used?
The one-time pad is one of the most practical methods of encryption where one or both parties must do all the work by hand, without the aid of a computer, which made it crucial in the pre-computer era. This method is still useful in situations where possession of a computer is illegal or incriminating or where trustworthy computers are not available. The one-time pad has been famously used for diplomatic communiques and by the KGB with exotic means of distributing, securing, and discarding secret keys. The breaking of poor Soviet cryptography by the British in the 1920s introduced the USSR to adopt one-time pads by around 1930. KGB spies are known to have used pencil and paper one-time pads more recently, including Rudolf Abel in the 1950s and the ‘Krogers’ (i.e. Morris and Lona Cohen) in the 1960s. The KGB one-time pads have been known to fit inside the palm of a hand or in a walnut shell.

If used correctly, this method of encryption has been proven to be impossible to crack. When the one-time pad is random and only used once, it is equally probable that each bit of the one-time pad is a one or a zero, and a zero or one in the ciphertext has an equal probability of being a zero or one in the plaintext. Small mistakes however can lead to successful cryptanalysis. One example is from 1944–1945; the US Army’s Signals Intelligence Service was able to solve a one-time pad system used by the German Foreign Office for its high-level traffic, codenamed GEE. GEE was insecure because the pads were not completely random as the machine used to generate the pads produced predictable output.

Additionally, the one-time pad for encryption imposes its own difficulties as it is almost essential for people to share the keys that are used in person, making the system unscalable for modern use cases such as online services. The efficiency of this method of cryptography is also questionable as we have to have a new piece of randomness for every letter of the plaintext. Therefore the one-time pad must be the same length as the plaintext. If our message was a page long, we would have to have a one-time pad that is also a page long. As these one-time pads must be kept secret, the longer the messages, the more paper needed to write them down on and therefore the harder they are to keep private.
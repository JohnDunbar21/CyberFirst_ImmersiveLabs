# Punycode

## Quick Summary
Punycode is an encoding method used to convert Unicode characters to ASCII – a smaller, more restricted character set. However, Punycode can also be exploited to launch a homograph attack, which lures victims into clicking on an illegitimate URL to steal sensitive data or infect a device. In this lab, you will use Cyberchef to decode and encode Punycode URLs to identify any suspicious modification. 

### What is Punycode?
Punycode is an encoding method that converts Unicode characters to a limited ASCII (American Standard Code for Information Interchange) character set.

This character set, called the Letter-Digit-Hyphen (LDH) subset, consists of:

Lowercase letters: a-z
Digits: 0-9
Special character: hyphen (-)
Punycode is primarily used to process Internationalized Domain Names (IDNs), which are limited to ASCII characters, as this allows for Unicode characters to be used in a hostname resolution in ASCII format. For example, if a domain is compromised of Chinese characters, Punycode will encode them into an ASCII format.

### How does it work?
Punycode allows domain names to include non-ASCII characters by creating a bootstring algorithm, which encodes Unicode characters used within a limited set of ASCII characters. The algorithm interprets any string passed to it and analyzes it for non-ASCII characters, then Punycode goes through a series of steps to create an encoded string usable on ASCII systems. Once complete, the algorithm performs some normalization functions on the string to eliminate ambiguities that may exist in the Unicode encoded text.

Step one:  The process of normalization is performed on the string to eliminate any Unicode text ambiguity. Normalization involves converting all characters into lowercase (a more ‘normal’ format), where applicable. The string is then searched for characters that exist within the ASCII character set. Any characters found within the set are ignored; however, any non-standard ASCII characters are removed and a hyphen is added to the end of the string.

Step two: If any non-standard ASCII characters are found, the prefix `xn--` is added to the string. This signifies that the string contains ACE (ASCII Compatible Encoding) and that the hyphen appended should be interpreted using Punycode rather than as part of the string itself.

Step three: Punycode analyzes the non-ASCII characters and appends a string of characters to the hyphen. Here, it uses ASCII characters to dictate which characters should be represented and where they should be placed within the string. While doing this, Punycode ensures that the end string does not exceed a 63-character limit.

To see these steps in action, we will use ‘adιdas.com’ but with the Greek letter ‘ι’ rather than ‘i’. Here, the ‘ι’ will be removed, the prefix `xn--` will be added to the start of the string to signify the presence of Unicode characters, and a hyphen will be added to the end of the string. Punycode will then add characters to the ending hyphen to represent the Unicode character.

Our final string would be: `xn--addas-rbe.com`

Though the resulting text is not the most straightforward to read, it accurately represents the original string of Unicode characters while using only previously allowed characters for domain names.

Here is an example of the process for a domain name using all Unicode characters:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/XjuvuvueynS-ehECIQVqMvS2kfePezaqbreBsictM0s.png">

Punycode allows the encoding of any 8, 16, or 32-bit character. In the example above, we have used the domain ‘www.날씨.co.kr'. The characters '날씨' are converted by Punycode to 'xn--i20bj30b'. The newly converted URL can now be represented by 'www.xn--i20bj30b.co.kr'. This means that if you bought the domain name 'www.날씨.co.kr', you would be actually be buying 'www.xn--i20bj30b.co.kr'.

By default, many web browsers use the `xn--` prefix to indicate that the domain is using Punycode to represent some Unicode characters. However, not all browsers show the Punycode prefix, leaving the potential for a homograph attack.

### Homograph attacks
Though Unicode characters may look the same in a web browser address, their appearance can be deceptive. For instance, many letters in the Roman alphabet look similar to letters in Greek and Cyrillic. This similarity means it can be easy for a malicious actor to replace ASCII characters with Unicode characters in a domain name.

For example, we could swap the English letter 'T' for a Greek Tau: ‘τ’ – an almost identical symbol to the naked eye. However, the Punycode URL would be 'xn--5xa' rather than just 'T', and if a browser address bar renders in a way that does not indicate that Punycode is present, these character changes can be hard to identify. This ambiguity can lead to a user unintentionally clicking on a harmful link.

The technique of swapping out ASCII characters for Unicode is called a homograph attack. The URL will look authentic, and the page content may appear the same, but it will be a different website set up with malicious intentions, such as stealing the victim's sensitive data or infecting their device. Homograph attacks use techniques like phishing, forced downloads, and scams to fulfill these aims. 

### How and why is it used?
Punycode is valuable for processing internationalized domain names. For example, characters in the Korean character system, Hangul, cannot be adequately encoded using ASCII. Therefore, Punycode takes Unicode encoded strings and converts them into a universally readable and resolvable ASCII string.

Before Punycode, companies and services operating in Korea (or other countries using a character-based language) had to adjust their domain name to fit the ASCII restrictions. For example, '날씨 ' translates to 'weather' in Korean. Pre-Punycode, a website would have had to change its domain name to an ASCII acceptable format, such as 'www.weather.co.kr'. Now, a website can use the domain name 'www.날씨.co.kr' intact with Unicode characters. This allows companies and services to keep their brand name identity while operating in markets that do not use the Latin alphabet. 
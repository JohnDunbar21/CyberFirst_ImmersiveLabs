# Base64 Encoding

## Quick Summary
Base64 is a binary-to-text encoding scheme used to transfer content-based messages over the internet. When binary data is transmitted to transfer media, systems can misinterpret the data and lose or corrupt it in the transmission process. Base64 is used to prevent this. In this lab you'll use CyberChef to encode and decode using Base64.

What is Base64 encoding?
Base64 is a binary-to-text encoding scheme that represents binary data and transforms it into an ASCII string format. Base64 encoding schemes are used when data needs to be stored and transferred over media designed to deal with text. 

### How does it work?
Base64 breaks binary data into 6-bit groups of three bytes (24 bits) and represents the groups as characters in ASCII. It does this in two steps:

Step one is to break down the binary string into 6-bit blocks. Base64 only uses six bits to ensure encoded data is printable and humanly readable. ASCII special characters are not used in this method.

The 64 characters of Base64 encoding (hence the name Base64) are 10 digits, 26 lowercase characters, 26 uppercase characters, the plus sign (+), and the forward-slash (/). The 65th character, known as pad, is the equals sign (=). Pad is used when the last segment of binary data doesn’t contain the full six bits.

All 64 characters in Base64 encoding can be found in the following table:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/ApoimuifNvpx-WeoUPfmfGu9y5qLYcbIWgDhdollKBU.png">

For example, say we want to convert the plaintext string ab@yz. The binary stream of this string is:

0110000101100010010000000111100101111010.

To encode to Base64 we first break the binary stream into groups of six bits:

011000 010110 001001 000000 011110 010111 101000 (note here that two 0s have been padded to the final grouping to complete the groups of six characters).

These binary numbers groupings translate into the decimal numbers 24, 22, 9, 0, 30, 23, and 40.

Step two is to convert these decimals using the Base64 encoding table.

The Base64 table shows us that:

24 is Y
22 is W
9 is J
0 is A
30 is e
23 is X
40 is o
YWJAeXo= (padded with '=' to account for extra bits added).

This two-step process is applied to the entire binary string that is being encoded.

### Why do we need it?
Base64 encoding is used to transfer data over a system that only supports ASCII formats. Examples of this are email messages on Multipurpose Internet Mail Extension (MIME) and Extensible Markup Language (XML) data. Base64 is also the industry-standard format for SSL certificate content. The most common web servers will generate certificate signing requests and accept SSL certificates in Base64 format.

Additionally, Base64 encoding is used when binary data found in media, such as images or video, is transmitted over systems designed to transmit data in an ASCII (plaintext) format.

Base64 encoding's necessity comes from the problems that can occur when media, such as those types mentioned above, are transmitted in raw binary format to text-based systems.

Because text-based systems like email interpret binary data as a wide range of characters (including command characters) binary data can be misinterpreted by those systems and lost or corrupted in the process of media transmission. Sending it as plain ASCII text in Base64 encoded format will avoid such transmission problems.
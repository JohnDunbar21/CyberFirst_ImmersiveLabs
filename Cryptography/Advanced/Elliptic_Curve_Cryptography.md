# Elliptic Curve Cryptography

## Quick Summary
Elliptic curve cryptography (ECC) is a relatively new method of encryption that provides more security for the same key length when compared to RSA. This lab will introduce you to the basics of elliptic curve cryptography and why more people are starting to use it for encryption. 

### What is elliptic curve cryptography?
In mathematics, elliptic curves are graphs with properties that make it easy to generate a sequence of numbers. Starting with the first point, it's easy to plot a sequence from beginning to end; however, this generated sequence cannot be reversed unless the whole sequence is known.

Elliptic curve cryptography (ECC) is a powerful approach to public-key cryptography that uses the structure of elliptic curves. It's a well-known alternative to RSA and uses the maths behind elliptic curves to generate security between two key pairs. 

<img src="https://assets.immersivelabs.online/uploads/asset/attachment/3833eee7283f83c288e4bfd6fa3bd163/attachment.png">

The above image is an example of elliptic curves plotted on a graph. Above and below the X axis is always symmetrical due to the nature of the equation used. 

### The maths
There's no denying that it's a tricky concept to grasp. For anyone who wants to explore the maths further, this article explains the basics.

https://hackernoon.com/what-is-the-math-behind-elliptic-curve-cryptography-f61b25253da3

### Types of ECC
ECC itself is a different form of cryptography, but it also has different curve types that different organisations and protocols apply in practice. Bitcoin, for example, uses ECC secp256k1, while NIST utilises P-224, P-256 and P-384. For a comprehensive (but not complete) list of ECC types, you can check out TLS support groups here. 

### Why use ECC?
ECC is becoming more popular than RSA due to its significantly smaller size (bits) of keys. Keys of the same size in RSA would provide inferior security.

ECC is now used by US governments to protect communications, while Bitcoin uses it to prove ownership of currency. Even Apple's iMessage service uses a form of ECC to encrypt DNS information. Many others are adopting this method, but like everything it has vulnerabilities.
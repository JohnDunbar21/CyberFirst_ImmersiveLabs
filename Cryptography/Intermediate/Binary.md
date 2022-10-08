# Binary

## Quick Summary
Binary is a numbering system that consists of only two possible values for each digit: 0 and 1. It's the primary language for computers and makes up all the raw data stored on our machines. In this lab, you will use CyberChef to encode and decode data to and from binary.

### What is binary?
Binary is a numbering system invented by Gottfried Leibniz in 1679 that consists of only two numbers or digits: 0 and 1. This numbering system is the basis of binary code, which is the primary language of computers.

The term binary can also refer to any digital encoding/decoding method with only two potential states. The 0 and 1 values in digital data memory, storage, processing, and communications are commonly referred to as ‘low’ and 'high', or 'off' and ‘on’, respectively.

A binary number is made up of eight bits, known as a byte. A bit, short for binary digit, is the smallest unit of data on a computer; each bit has one of two values: 1 or 0. Executable (ready-to-run) applications are identified as binary files with the file extension '.bin.' Programmers often call these executable files binaries.

### How does it work?
When typed out, binary numbers appear unreadable to the human eye. This is because the weight of the digits grows by powers of two rather than powers of ten. The placement of a binary digit determines its decimal value. For example, if we have an 8-bit binary number, the values will be calculated like so:

Bit 1: 2^0 = 1
Bit 2: 2^1 = 2
Bit 3: 2^2 = 4
Bit 4: 2^3 = 8
Bit 5: 2^4 = 16
Bit 6: 2^5 = 32
Bit 7: 2^6 = 64
Bit 8: 2^7 = 128

To read binary, we work from right to left. As shown above, the power of the right-most digit is zero, followed (towards the left) by two to the power of one, two, three, and so on. We can transform a binary number into a digital number by adding together all these values.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/WXbMiL1XwxzBREPgR_8FYdSZms-CWcruTAgDZyM5VaE.png">

We can express any decimal number from 0 to 255 in binary form by adding the different values when the bit has a value of 1. By adding more bits to the system, we can represent more significant numbers.

For example, the binary number 01011001 represents the decimal number 89 (1+0+0+8+16+0+64+0 = 89).

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/H09JD-z_zC86XppF7tPF_CvCOq4H4qSNgNzoXlRycnQ.png">

Here are the first 15 decimal numbers in binary form:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/KkTfIabFXC0qUi3AzMWyJ1WVXy6Gf46-WUqOoSbF3KE.png">

The transformation of letters into binary is defined by the rules set by UTF-8, in which each character is assigned a group of eight binary digits:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/xmOrNPQbedxZBWSPvmi-Emhark4cgHUaLyZsXUL2n_M.png">

### Why is it used and who might use it?
Binary is the primary language for computers and electronic devices, which can only understand and store data in this form.

However, at the most granular level of the data, complex media data such as images and videos are also stored in binary code. An image, for example, is made up of hundreds of thousands of pixels, with each pixel containing an RGB value (color value) stored in binary code.

Music is also stored in binary format, using a technique called pulse code modulation. This technique digitizes continuous sound waves by taking snapshots of their amplitudes every few milliseconds and storing amplitudes of the snapshots in binary. Each second of sound could have a possible 44,000 binary strings. The binary code of an audio file allows a computer to determine the frequency of the vibration in the coils of the speaker, which then projects the sounds we hear.
# Hexadecimal

## Quick Summary
Hexadecimal, also known as hex, is a base-16 numbering system used to shorten binary code and make it easier to understand. As computers can only read in 1s and 0s, hex transforms this data into a user-friendly format.

### What is hexadecimal?
Hexadecimal, also called base-16 or hex, is a number system that uses 16 unique symbols to represent a particular value. These symbols are the numbers 0-9 and the letters A-F (in capitals), which represent an equivalent binary or decimal number, starting with the least significant digit on the right-hand side.

The unique hexadecimal symbols appear in the following order:

0 1 2 3 4 5 6 7 8 9 A B C D E F

The decimal 12, for example, would be C in hexadecimal.

Computers only understand binary code (or base-2), which is challenging for humans to read, so programmers created hexadecimal to simplify the binary system. Hexadecimal takes one hexadecimal digit to represent four binary digits. Whereas eight binary digits represent one byte, only two hexadecimal digits are required to do so.

Hex is often used in computing due to its simplicity and the ease of converting it to binary. To learn more about the binary numbering system, visit our lab here:

### How does it work?
Counting in hex is very similar to decimal, except there are six extra non-numerical digits. Firstly, you count from zero to nine and then from A to F. Once you've reached F, you roll that place back to zero and increment the digit to the left by one. 

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/E82eSRibJbvFAB6pk8xAqtM-JkuJeXBJS5Oj8dg_dOI.png">

### Converting hex to/from binary
Converting between hex and binary is simple because each digit of a hexadecimal number represents four bits (a bit being an individual binary digit) of a binary value. So a byte (eight bits) can always be represented by two hexadecimal digits. Therefore, hex is a concise way to represent a byte or group of bytes.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/dlpXj_d3p2OfmYfEKgBwy2gtGfVvbwo_Dt1nZfx-VhU.png">

Converting from binary to hex
To convert binary data to hex, we base our workings on the fact that four binary digits represent one hex digit.

These are the steps for converting binary to hex:

Split the binary value into groups of four digits, starting at the right-hand side of the data.
Replace each group of four digits with its matching hex value in the table above.
For example: Convert the binary 0110110001001101 to hex.

Starting at the right-hand side of the binary number, we need to sort the 1s and 0s into groups of four:

Binary groups: 0110 1100 0100 1101

Then, we can use the table above to convert these groups into a single hex digit:

Binary groups: 0110 1100 0100 1101
Hex digit:               6         C        4       D

Our binary number 0110110001001101 is converted to 6C4D in hex.

Converting from hex to binary
To convert from hex to binary, we simply reverse the process:

For each hex digit, find the matching four-digit binary value in our table, and replace the one hex value with groups of binary digits.
For example: 

Convert the hex DECAF to binary.

First, sort the string into individual digits:

Hex digit: D E C A F

Now convert each hex digit into groups of four binary bits:

Hex digit:              D          E           C          A           F
Binary groups: 1101    1110    1100    1010    1111    

Our hex digit DECAF is converted to 11011110110010101111 in binary.

### How and why is hexadecimal used?
Computer error codes use a hexadecimal format. For example, the STOP codes displayed on the famous Windows Blue Screen of Death, are always hexadecimal.

Programmers use hexadecimal digits because their values are shorter than decimal equivalents and are more concise than binary. An example of this would be the hexadecimal value F4240. This value is equivalent to 1,000,000 in decimal and 1111 0100 0010 0100 0000 in binary, but the hexadecimal format allows you to store the same information while using less space.

It is also simple to convert between hexadecimal numbers and binary. Hex can therefore be used to represent large binary numbers in just a few digits. This makes it easier for us to read, write and understand data, which also reduces the possibility of human error when working with it.

Hexadecimal is commonly used as an HTML color code to represent a specific color on the color chart.

For example, the hex value FF0000 is used to define the color red. Breaking this down, the value becomes FF,00,00. This then defines the amount of red, green, and blue colors in this specific shade (RRGGBB), which in this example is 255 red, 0 green, and 0 blue.

Hexadecimal values can be expressed in two digits up to 255, and HTML color codes use three sets of two digits. This means over 16 million (255 x 255 x 255) possible colors can be represented in hexadecimal format, taking up less space than other formats like decimal or binary.
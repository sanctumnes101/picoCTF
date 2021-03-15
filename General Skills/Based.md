## Description

> To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with nc jupiter.challenges.picoctf.org 29956.


## Hints

> I hear python can convert things.
> It might help to have multiple windows open.


## Approach & Solution

So far we know about `bases` in computer science. Let's connect to the server using the following command: `nc jupiter.challenges.picoctf.org 29956`

Ok so we have a timer, and a bunch of 8bits binary numbers, and we have to enter a string input. If you followed my solutions and the articles I put, you know that each 4bits of binary are equivalent to 1bit in hex.
That means that each 8bits in binary are equivalent to 2bits in hex. We also know that each ASCII character has a hex value of 2bits. That means that each 8bits in binary represent a character in ASCII.
Of course we can convert each group of numbers manually from binary to hex then by looking at the ASCII table we can convert that to a character, but that will cost us a lot of time!

A better approach would be using converter! I preferably use online converters for these challenges, but you can convert it using python as well!

So let's find `binary to hex` and `hex to ascii` converters.
Steps to get the input word:

1. Open in multiple tabs [binary to hex](https://codebeautify.org/binary-hex-converter) converter and [hex to ASCII](https://www.online-toolz.com/tools/hex-to-ascii-converter.php) converter
2. Connect to the server using the following command: `nc jupiter.challenges.picoctf.org 29956`
3. Copy the binary numbers from the server and convert them using the `binary to hex` converter from step (1) and then copy the hex values and convert them to ASCII using the `hex to ASCII` from step (1)

We notice that there are other group of numbers came up. After finishing the previous challenges, we can easily identify the base used to encode the other string, which is `octal`(base 8).

Steps to get the second input word:

4. Open [octal to ASCII](http://www.unit-conversion.info/texttools/octal/) converter
5. Copy the octal numbers and convert them to ASCII using the `octal to ASCII` converter from step (4)

Another encoded string will show up. But this one is easily identifiable, there are numbers from 0-9 and letters from a-f so it must be `hex`

Steps to get the third input word:

6. Copy the hex string and convert it using the `hex to ASCII` converter from step (1)
7. the flag will show up: `picoCTF{learning_about_converting_values_b375bb16}`


## Final Answer

`picoCTF{learning_about_converting_values_b375bb16}`

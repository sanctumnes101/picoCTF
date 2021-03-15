## Description

> Can you convert the number 42 (base 10) to binary (base 2)?


## Hints

> 1. Submit your answer in our competition's flag format. For example, if your answer was '11111', you would submit 'picoCTF{11111}' as the flag.

## Approach & Solution

A **base** is the letters *and/or* numbers to use in a numbering system. In mathematics and daily life we use **base-10** numbering systems, meaning we can use the numbers 0,1,2,...,9.
In computer science, there are many other bases, the most important bases are:
+ Base-2 (Also called ***binary*** and uses the numbers 0 and 1)
+ Base-8 (Also called ***octal*** and uses the numbers 0,1,2,...,7)
+ Base-10(Also called ***decimal*** and uses the numbers 0,1,2,...,9)
+ Base-16(Also called ***hexa-decimal*** or shortened as ***hex*** and uses the numbers 0,1,2,...,9 and the letters a,b,c,d,e,f)

There are a lot of ***base to base converters*** online, but it's important(and easy) to understand and actually know how to manually convert from base to base.

Here's an [article](https://www.tutorialspoint.com/computer_logical_organization/number_system_conversion.htm) about how to convert from base to another that can be helpful.

42 in decimal is 101010 in binary. (1*(2^5) + 0*(2^4) + 1*(2^3) + 0*(2^2) + 1*(2^1) + 0*(2^0))

## Final Answer
`picoCTF{101010}`

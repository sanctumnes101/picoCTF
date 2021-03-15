## Description

> If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?


## Hints

> Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.


## Approach & Solution

[ASCII](https://en.wikipedia.org/wiki/ASCII) is, in short, a character encoding standard which is used by computers to represent text. 
For a character to be printed on screen, the assigned hex code to that character must be used.
You can read [this article](https://www.elprocus.com/hexa-to-ascii-and-ascii-to-hexa-conversion-with-example/) about how to convert from hex to ASCII for a deep understanding, but in short, if you have a long hex number, you divide it into slots of 2 digits, and then convert each character code(each 2 digits) to it's ASCII character.
You can find an ASCII table searching google. Here is [one](http://www.asciitable.com/) you can use.
If you look under the `hex` column and at the value `70` you will see the character `p`. 


## Final Answer

`picoCTF{p}`

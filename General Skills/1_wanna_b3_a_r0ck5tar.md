## Description

> I wrote you another song. Put the flag in the picoCTF{} flag format


## Hints

> None


## Approach & Solution

This is another rockstar programming language challenge. Let's try to do what we did in `mus1c` challenge:

1. Go to https://codewithrockstar.com/online
2. Copy and paste the lyrics and hit "ROCK"

We see nothing!

If we navigate the website, we can see that there are "DOCS" section, which explains the language and it's usage, and there is "CODE" section, where there are many transpilers for the language.
We can get the flag either ways, but I prefer the easy way using a transpiler. 

Steps to get the flag:

1. Head to https://codewithrockstar.com/code
2. Choose your favourite transpiler, i personally used python transpiler
3. Follow the instructions about installing the transpiler you chose and how to use it
4. Use it to decode the lyrics, you'll get the following ASCII numbers: `66 79 78 74 79 86 73`
5. [ASCCI to text](https://www.duplichecker.com/ascii-to-text.php) decode them, you'll get: `BONJOVI`


## Final Answer

`picoCTF{BONJOVI}`

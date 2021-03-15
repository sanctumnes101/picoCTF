## Description

> I wrote you a song. Put it in the picoCTF{} flag format.
 

## Hints

> Do you think you can master rockstar?


## Approach & Solution

By using the hint and the title, Search google for "rockstar music programming language". You'll see that there is a programming language called "rockstar" with an official [website](https://codewithrockstar.com/)
When visiting the website, there is a "TRY IT" button, which will redirect you to a decoder of this language.

Steps to get the flag:

1. Go to the website above
2. Hit the `try it` button
3. Copy and paste the lyrics from the file downloaded from the `Description` section and press "ROCK"
4. You will get these numbers: `114 114 114 111 99 107 110 114 110 48 49 49 51 114`. If you're familiar with ASCII you'll notice that these numbers are ASCII numbers.
5. Go to [ASCII to text](https://www.duplichecker.com/ascii-to-text.php) converter, and convert the numbers. You'll get: `rrrocknrn0113r`


## Final Answer

`picoCTF{rrrocknrn0113r}`

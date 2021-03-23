## Description

> Decrypt this message.


## Hints

> caesar cipher [tutorial](https://privacycanada.net/classical-encryption/caesar-cipher/)


## Approach & Solution

Let's open the message we got from the `Description` using notepad or any text editor. There is the following encrypted flag:

`picoCTF{gvswwmrkxlivyfmgsrhnrisegl}`

We know that the flag is encrypted using caesar encrytion. Use can follow the tutorial in the `Hints` to know more about it, but it's similar to ROT from the previous challenges.

Let's decrypt the flag using [this site](https://www.dcode.fr/caesar-cipher). Copy and paste `gvswwmrkxlivyfmgsrhnrisegl` into the box, and test all possibilities.

You can see that the only string that is understandable is `crossingtherubicondjneoach` which is +4, so it must be the flag.


## Final Answer

`picoCTF{crossingtherubicondjneoach}`

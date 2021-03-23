## Description

> The numbers... what do they mean?


## Hints

> The flag is in the format PICOCTF{}


## Approach & Solution

We're given an image full of numbers, and we have to know what those numbers mean.

The numbers are: `16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }`. We know that the flag looks like `PICOCTF{SOME_RANDOM_STRING}` from the hint.

So, `16 9 3 15 3 20 6` must be the word `PICOCTF`. Notice that `C` is the 3rd letter in the English alphabet, and `F` is the 6th. It is pretty easy to conclude that the numbers are the indexes of the alphabet characters.

Steps to find the flag:

1. Enumerate the English alphabet letters:
`a    b    c    d    e    f    g    h    i    j    k    l    m    n    o    p    q    r    s    t    u    v    w    x    y    z`
`1    2    3    4    5    6    7    8    9   10   11   12   13    14   15   16   17   18   19   20   21   22   23   24   25   26`

2. For each number, match the corresponding character, and form the flag: `PICOCTF{THENUMBERSMASON}`


## Final Answer

`PICOCTF{THENUMBERSMASON}`

## Description

> Let's decrypt this: ciphertext? Something seems a bit small.


## Hints

> RSA [tutorial](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
> How could having too small an e affect the security of this 2048 bit key?
> Make sure you don't lose precision, the numbers are pretty big (besides the e value)


## Approach & Solution

By reading the "Attacks against plain RSA" section in the article in the `Hints` section, we know that if we use a small `e` such that `c=m^e` < `n`, we can decrypt the `m` by taking the `eth` root of `c=m^e` to get `m`.

Let's do that with python. Compute the `cube` root of `c` in the given file, convert it to hex, then the hex to ascii. flag I got: `picoCTF{n33d_a_lArg3r_e_d0cd6eae}`.


## Final Answer

`picoCTF{n33d_a_lArg3r_e_d0cd6eae}`

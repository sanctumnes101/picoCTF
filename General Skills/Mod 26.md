## Description

> Cryptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}
 

## Hints

> This can be solved online if you don't want to do it by hand!


## Approach & Solution

The flag is given in the `Description`, but it is encrypted using ROT-13. ROT-x encryption is basically rotating each character by x characters. Google it for more information.

Steps to get the flag:

1. Go to any ROT-13 online decryption tool. For example [this one](https://rot13.com/)
2. Decrypt the flag: `picoCTF{next_time_I'll_try_2_rounds_of_rot13_wqWOSBKW}`. Side note: 2 rounds(or any even number) gives us the original text!


## Final Answer

`picoCTF{next_time_I'll_try_2_rounds_of_rot13_wqWOSBKW}`

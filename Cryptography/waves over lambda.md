## Description

> We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with nc jupiter.challenges.picoctf.org 39894.


## Hints

> Flag is not in the usual flag format


## Approach & Solution

Let's connect to the server. We get the following message:

```
ntybdzop ukdk ip htad fszb - fdkrakynh_ip_n_tekd_szlmqz_zbfsnbohak
-------------------------------------------------------------------------------
mkoxkky ap oukdk xzp, zp i uzek zsdkzqh pziq ptlkxukdk, ouk mtyq tf ouk pkz. mkpiqkp utsqiyb tad ukzdop otbkoukd oudtabu styb ckditqp tf pkczdzoity, io uzq ouk kffkno tf lzwiyb ap otskdzyo tf kznu toukd'p hzdypzyq keky ntyeinoityp. ouk szxhkdouk mkpo tf tsq fksstxpuzq, mknzapk tf uip lzyh hkzdp zyq lzyh eidoakp, ouk tysh napuity ty qknw, zyq xzp shiyb ty ouk tysh dab. ouk znntayozyo uzq mdtabuo tao zsdkzqh z mtj tf qtliytkp, zyq xzp othiyb zdnuioknoadzssh xiou ouk mtykp. lzdstx pzo ndtpp-skbbkq dibuo zfo, skzyiyb zbziypo ouk livvky-lzpo. uk uzq paywky nukkwp, z hksstx ntlcskjity, z podzibuo mznw, zy zpnkoin zpckno, zyq, xiou uip zdlp qdtcckq, ouk czslp tf uzyqp taoxzdqp, dkpklmskq zy iqts. ouk qidknotd, pzoipfikq ouk zynutd uzq bttq utsq, lzqk uip xzh zfo zyq pzo qtxy zltybpo ap. xk kjnuzybkq z fkx xtdqp szvish. zfokdxzdqp oukdk xzp piskynk ty mtzdq ouk hznuo. ftd ptlk dkzpty td toukd xk qiq yto mkbiy ouzo bzlk tf qtliytkp. xk fkso lkqiozoiek, zyq fio ftd ytouiyb mao cszniq pozdiyb. ouk qzh xzp kyqiyb iy z pkdkyioh tf poiss zyq kjraipiok mdissizynk. ouk xzokd putyk cznifinzssh; ouk pwh, xioutao z pcknw, xzp z mkyiby illkypioh tf aypoziykq sibuo; ouk ekdh lipo ty ouk kppkj lzdpu xzp siwk z bzavh zyq dzqizyo fzmdin, uayb fdtl ouk xttqkq dipkp iyszyq, zyq qdzciyb ouk stx putdkp iy qizcuzytap ftsqp. tysh ouk bsttl ot ouk xkpo, mdttqiyb tekd ouk acckd dkznukp, mknzlk ltdk ptlmdk kekdh liyaok, zp if zybkdkq mh ouk zccdtznu tf ouk pay.
```

It seems like we got no clue at all. Let's read the `Description` again. "We made a lot of substitutions". Let's google "Substitution encryption". We get a lot of articles, let's head to the [wikipedia page](https://en.wikipedia.org/wiki/Substitution_cipher) and read about it.

From what we understand, "Substitution Cipher" is basically replacing characters with another ones. I used [this](https://www.boxentriq.com/code-breaking/cipher-identifier) online cipher analyzer to detect which type the cipher is, and it is clearly "Monoalphabetic Substitution Cipher".

Let's decipher the text using automatic [online tool](https://www.boxentriq.com/code-breaking/cryptogram). We get the following decihpered message:

```
congrats here is your flag frequency is c over lambda agflcgtyue between us there was as i have already said somewhere the bond of the sea besides holding our hearts together through long periods of separation it had the effect of making us tolerant of each other s yarnsand even convictions the lawyerthe best of old fellowshad because of his many years and many virtues the only cushion on deck and was lying on the only rug the accountant had brought out already a box of dominoes and was toying a...
```

The flag is not in the traditional format as the hint says, so it must be: `frequency_is_c_over_lambda_agflcgtyue`


## Final Answer

`frequency_is_c_over_lambda_agflcgtyue`

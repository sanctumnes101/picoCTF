## Description

> Theres tapping coming in from the wires. What's it saying nc jupiter.challenges.picoctf.org 48247.


## Hints

> What kind of encoding uses dashes and dots?
> The flag is in the format PICOCTF{}


## Approach & Solution

Let's connect to the server in the `Description`. We get the following message: `.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. .---- ..--- -.... .---- ....- ...-- ---.. .---- ---.. .---- }`

Anyone who knows about morse code knows that this is a morse code encryption! But if you don't, you can google "dashes and dots encryption" and the result will tell you that this is a morse code encryption.

Let's decrypt the message using [this site](https://morsecode.world/international/translator.html). 

Copy the message, remove `{` and `}` because the site doesn't allow them, and decrypt the message. What we get is: `PICOCTFM0RS3C0D31SFUN1261438181`. Restore `{` and `}` to their possitions and that's it.


## Final Answer

`PICOCTF{M0RS3C0D31SFUN1261438181}`

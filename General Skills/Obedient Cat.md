## Description

> This file has a flag in plain sight (aka "in-the-clear"). Download flag.


## Hints

> Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
> To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
> $ man cat


## Approach & Solution

This is a newbie challenge, everything is pretty much written in the `Hints` section.

Steps to get the flag:

1. Connect to webshell.
2. Download the flag file using the following command: `wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag`
3. open the file to view the flag using the following command: `cat flag`


## Final Answer

`picoCTF{s4n1ty_v3r1f13d_1a94e0f9}`

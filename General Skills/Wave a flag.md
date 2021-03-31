## Description

> Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...


## Hints

> This program will only work in the webshell or another Linux computer.
> To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
> Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm
> -h and --help are the most common arguments to give to programs to get more information from them!
> Not every program implements help features like -h and --help.


## Approach & Solution

First of all read the `Hints` section. pretty much everything is in there.

Steps to get the flag:

1. Download the given file using the following command: `wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm`
2. Give the file `execute` permissions using the following command: `chmod +x warm`. You can read more about `linux file permissions` in google.
3. Invoke the `help` tool for the program using the following command: `./warm -h` and get the flag: `picoCTF{b1scu1ts_4nd_gr4vy_616f7182}`


## Final Answer

`picoCTF{b1scu1ts_4nd_gr4vy_616f7182}`

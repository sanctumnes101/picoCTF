## Description

> Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to jupiter.challenges.picoctf.org 4427.


## Hints

> Remember the flag format is picoCTF{XXXX}

> What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)


## Approach & Solution

From a previous challenge, we know how to connect to the given server at the given port using the `nc` tool.
If you try to connect to the server at the given port using the following command: `nc jupiter.challenges.picoctf.org 4427` on `webshell` we will see so many messages, and if you look for the flag (which we already know starts with picoCTF) we will not find it because the shell's (command line we're writing our commands on) number of output lines are limited to a specific number.

But notice that from a previous challenge about using `grep` tool, we looked for the flag in a bunch of random lines similar to the ones we got a moment ago when connecting to the server, so `grep` might be helpful!

The second hint gives us a link to a topic which is called `pipes`. pipes are simply used with this character: `|`. In short, pipes are used to redirect the **output** of program to be the **input** of another. So instead of printing to the screen, we can treat the output as a **file** with a content that was supposed to be printed on the screen, and we can use this file to do whatever it is we wanna do.

To get the flag, you will redirect the output that comes after connecting the server to be the input of `grep`, so we can easily look for the "picoCTF" pattern:

1. Connect to webshell with your username and password
2. Redirect the output of the server to be the input of grep using the following command: `nc jupiter.challenges.picoctf.org 4427 | grep picoCTF`
3. the flag will appear: `picoCTF{digital_plumb3r_5ea1fbd7}`


## Final Answer

`picoCTF{digital_plumb3r_5ea1fbd7}`

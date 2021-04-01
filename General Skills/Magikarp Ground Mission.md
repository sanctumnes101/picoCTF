## Description

> Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `ee388b88`


## Hints

> Finding a cheatsheet for bash would be really helpful!


## Approach & Solution

First of all let's launch an instance, using the `Launch Instance` button. It will give us a network service to connect to using [ssh](https://en.wikipedia.org/wiki/Secure_Shell_Protocol).

Connect to the network service using the command given: `ssh ctf-player@venus.picoctf.net -p 49188`.

We have to figure out where the flags are hidden. The first thing to do is viewing what files/folders we have using the `ls` command. Type `ls` in the command-line.

There are 2 files:

1. 1of3.flag.txt - a file containing the first part of our flag. To see it's content we'll use the `more` command: `more 1of3.flag.txt` - it gives us the following text: `picoCTF{xxsh_`
2. instructions-to-2of3.txt - a file containing info about how to get the 2nd part of the flag. Let's view it using `more`: `more instructions-to-2of3.txt`. It has the following text: `Next, go to the root of all things, more succinctly ``` `/` ```.

We'll have to go to the `/` directory in order to get our second flag. Let's do so by using `cd ..` command 2-3 times(remember to check the content of each directory using `ls` each time you execute this command).

When we get the `/` directory, there's a file called `2of3.flag.txt`. View it using `more` again: `more 2of3.flag.txt`. It gives us the following text: `0ut_0f_\/\/4t3r_`. By viewing the instructions to the 3rd flag using the same command, we get the following text: ```Lastly, ctf-player, go home... more succinctly `~` ```.

Let's go to `home` directory using the following command: `cd home`. There's one directory in it called `ctf-player`(use `ls` to view the content of `home`). Let's visit `ctf-player` using the same command. There it is, the 3rd part of the flag. View it using `more` again. We get the following text: `3ca613a1}`.


To exit the ssh session write `~.` (You won't see it while being written!)

## Final Answer

`picoCTF{xxsh_0ut_0f_\/\/4t3r_3ca613a1}`

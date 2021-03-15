## Description

> Using netcat (nc) is going to be pretty important. Can you connect to jupiter.challenges.picoctf.org at port 41120 to get the flag?


# Hints

> nc [tutorial](https://linux.die.net/man/1/nc)


## Approach & Solution

`nc`(short for **netcat**) is a tool which can do many things related to TCP and UDP connections. In this challenge we will open a connection and listen on a specified port. For more usages of `nc` use the link in the `Hints` section.
To get the flag follow the steps below:

1. Open `Webshell` (right top corner) and enter your username and password
2. Connect the given server at the given port using the follwing command: nc jupiter.challenges.picoctf.org 41120
3. A message from the server containing the flag will apear: `You're on your way to becoming the net cat master picoCTF{nEtCat_Mast3ry_3214be47}`

## Final Answer
`picoCTF{nEtCat_Mast3ry_3214be47}`

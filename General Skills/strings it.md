## Description

> Can you find the flag in file without running it?


## Hints

> [strings](https://linux.die.net/man/1/strings)


## Approach & Solution

By clicking the link in the `hints` section, we get redirected to the manual pages of [linux](https://en.wikipedia.org/wiki/Linux). `strings` is a tool which can be run from a command line in linux(also called Terminal), and is used to print the strings of printable characters in files as you can read in the manual.
Don't worry about the options you can use with `strings` for now. Let's `strings` the file given to us by following the steps below:

1. Download the file in the `Description` section to your linux operating system.
2. Move the file to Desktop.
3. On your Desktop, right click and press "Open Terminal".
4. Go to the Desktop path in your terminal by typing the following command: `cd Desktop`
5. Run the `strings` tool on the file named "strings" that you downloaded and save the output in out.txt: `strings strings > out.txt`
6. On your Desktop open the file "out.txt"
7. Press `ctrl+f` and find "picoCTF", you will see the flag: `picoCTF{5tRIng5_1T_7f766a23}`


## Final Answer 

`picoCTF{5tRIng5_1T_7f766a23}`

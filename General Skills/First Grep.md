## Description

> Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way.


## Hints

> grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)


## Approach & Solution

Following the link in the `Hints` section, you can read about the `grep` tool. In short, it is used to find patterns in a file. The syntax of grep can be found [here](https://linux.die.net/man/1/grep).
We know by now that flags start with "picoCTF".
To get the flag, follow the steps below:

1. Download the file given in the `Description` to your linux operating system.
2. Move the file to your Desktop.
3. Open Terminal and go to the Desktop path.
4. Write the following command: `grep picoCTF file` (grep is the command, picoCTF is the pattern, file is the file name)
5. the flag will be printed on your terminal: `picoCTF{grep_is_good_to_find_things_5af9d829}`


## Final Answer

`picoCTF{grep_is_good_to_find_things_5af9d829}`


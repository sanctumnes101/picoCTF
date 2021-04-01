## Description

> Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip


## Hints

> After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...


## Approach & Solution

First of all let's download the zip file given in the `Description` section by using the `wget` command: `wget https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip`.

Let's unzip the zip file using the `unzip` command: `unzip Addadshashanammu.zip`. Note that you don't have to write the name of the zip file manually, but rather use the `Tab` button on your keyboard.

Note that after unzipping the zip file there's a folder with bunch of other folders in it.(Use `ls` command to see the new unzipped folder). Get into the folders using the `cd {FOLDER_NAME}` command and by pressing `Tab` on your keyboard until there's no folder to get into.

In the last folder there's a program called `fang-of-haynekhtnamet`. Run it by using the `./{FILE_NAME}` command. Remember that you don't have to write it's name fully, but rather use the `Tab` button.

When you run it you'll get the flag: `picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}`


## Final Answer

`picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}`

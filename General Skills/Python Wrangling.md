## Description

> Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?


## Hints

> Get the Python script accessible in your shell by entering the following command in the Terminal prompt: $ wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py
> man python


## Approach & Solution

Let's download the python script, the password, and the flag file using the `wget` command. You can read about python and how to open python files using `man python`.

Steps to get the flag:

1. Download the given files using the `wget` command: `wget {URL_OF_FILE}`
2. Try to open the `ende.py` file using `python ende.py`, it won't work and will give us a `usage` message
3. Open the `ende.py` file using the following command: `python ende.py -d flag.txt.en`
4. Enter the password in the `pw.txt` file. ( You can get it using `cat pw.txt`)
5. Get the flag: `picoCTF{4p0110_1n_7h3_h0us3_192ee2db}`


## Final Answer

`picoCTF{4p0110_1n_7h3_h0us3_192ee2db}`

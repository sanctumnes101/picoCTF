## Description

> Can you look at the data in this binary: static? This BASH script might help!


## Hints

> None


## Approach & Solution

Let's download the binary file and the bash script using the `wget` command: `wget {URL_TO_FILE}`. Let's give `execute` permissions to both of the files using the following command: `chmod +x {FILE_NAME}`.

Now, let's try and run `static` file with: `./static`. We get a message saying the flag is here somewhere. We have to use the bash script in order to see what's hidden in the file.

Using the bash script to disassemble(to get the assembly of the binary file) the file using this command: `./ltdis.sh static` gives us 2 files, the disassembly of the file and strings in it.

Let's open the strings file and search for the flag. We get the following flag: `picoCTF{d15a5m_t34s3r_f5aeda17}` in offset `1020`.


## Final Answer

`picoCTF{d15a5m_t34s3r_f5aeda17}`

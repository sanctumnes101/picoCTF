## Description

> The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help UFJKXQZQUNB with the key of SOLVECRYPTO. Can you use this table to solve it?.


## Hints

> Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.
> Please use all caps for the message.


## Approach & Solution

We're given this table:

```
    A B C D E F G H I J K L M N O P Q R S T U V W X Y Z 
   +----------------------------------------------------
A | A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
B | B C D E F G H I J K L M N O P Q R S T U V W X Y Z A
C | C D E F G H I J K L M N O P Q R S T U V W X Y Z A B
D | D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
E | E F G H I J K L M N O P Q R S T U V W X Y Z A B C D
F | F G H I J K L M N O P Q R S T U V W X Y Z A B C D E
G | G H I J K L M N O P Q R S T U V W X Y Z A B C D E F
H | H I J K L M N O P Q R S T U V W X Y Z A B C D E F G
I | I J K L M N O P Q R S T U V W X Y Z A B C D E F G H
J | J K L M N O P Q R S T U V W X Y Z A B C D E F G H I
K | K L M N O P Q R S T U V W X Y Z A B C D E F G H I J
L | L M N O P Q R S T U V W X Y Z A B C D E F G H I J K
M | M N O P Q R S T U V W X Y Z A B C D E F G H I J K L
N | N O P Q R S T U V W X Y Z A B C D E F G H I J K L M
O | O P Q R S T U V W X Y Z A B C D E F G H I J K L M N
P | P Q R S T U V W X Y Z A B C D E F G H I J K L M N O
Q | Q R S T U V W X Y Z A B C D E F G H I J K L M N O P
R | R S T U V W X Y Z A B C D E F G H I J K L M N O P Q
S | S T U V W X Y Z A B C D E F G H I J K L M N O P Q R
T | T U V W X Y Z A B C D E F G H I J K L M N O P Q R S
U | U V W X Y Z A B C D E F G H I J K L M N O P Q R S T
V | V W X Y Z A B C D E F G H I J K L M N O P Q R S T U
W | W X Y Z A B C D E F G H I J K L M N O P Q R S T U V
X | X Y Z A B C D E F G H I J K L M N O P Q R S T U V W
Y | Y Z A B C D E F G H I J K L M N O P Q R S T U V W X
Z | Z A B C D E F G H I J K L M N O P Q R S T U V W X Y

```

And this encrypted flag: ` UFJKXQZQUNB`, and this key: `SOLVECRYPTO`

What we need to do is find the way that the key `SOLVECRYPTO` became the encrypted flag `UFJKXQZQUNB`, which means finding the real flag!

+ Look at the row of `S`, and find which letter gave us the letter `U`: it is `C`
+ Look at the row of `O`, and find which letter gave us the letter `F`: it is `R`
+ Look at the row of `L`, and find which letter gave us the letter `J`: it is `Y`
+ Look at the row of `V`, and find which letter gave us the letter `K`: it is `P`
+ Look at the row of `E`, and find which letter gave us the letter `X`: it is `T`
+ Look at the row of `C`, and find which letter gave us the letter `Q`: it is `O`
+ Look at the row of `R`, and find which letter gave us the letter `Z`: it is `I`
+ Look at the row of `Y`, and find which letter gave us the letter `Q`: it is `S`
+ Look at the row of `P`, and find which letter gave us the letter `U`: it is `F`
+ Look at the row of `T`, and find which letter gave us the letter `N`: it is `U`
+ Look at the row of `O`, and find which letter gave us the letter `B`: it is `N`


So the real flag is: `picoCTF{CRYPTOISFUN}`


## Final Answer

`picoCTF{CRYPTOISFUN}`


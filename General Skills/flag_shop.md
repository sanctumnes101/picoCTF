## Description

> There's a flag shop selling stuff, can you buy a flag? Source. Connect with nc jupiter.challenges.picoctf.org 9745.


## Hints

> Two's compliment can do some weird things when numbers get really big!


## Approach & Solution

**Open the file in notepad++**

Let's take a look and analyze the source file given to us.

We can see that we have an initial value of 1100 in the following line: `int account_balance = 1100;` (line 8)

We can see that there is a loop that will continue to be performed until con!=0: `while(con == 0)` (line 9)

Then inside the while loop, there are a few `printf` statements which if we read tell us to choose a number from 1 to 3 to perform an activity. Let's analyze the activities:

+ If we press '1' the server simply prints the account balance.
+ If we continue to the end in line 83, the variable `con` takes the value 1, which is not 0, so this will terminate the while loop and exit the server
+ Now to the interesting option, if we press '2', we get to choose to buy from 2 options depending on the value of the variable `auction_choice`.

We will now be focused into the buying flags option(option 2)
- If we choose to buy from option 1, we will pay 900 per flag, and as the messages in the `printf` statements say, the flag will not be found here.
- If we choose to buy from option 2, we will pay 10k per l33t flag, and a message says that there is only 1 l33t flag, so apparently this is the flag that we wanna buy!

Our initial account balance is 1100, the l33t flag costs 10k, and there are no activities(apparently) that increase our account balance, so how will we buy the l33t flag!?

Let's look at the hint. 2's complement. Basically numbers in computers are stored in [2's complement](https://en.wikipedia.org/wiki/Two%27s_complement) binary numbers. In short, this means that **positive** numbers start with 0 and **negative** numbers start with 1(talking in binary of course).

We also note that the `account_balance` is stored a variable of type `int`. `int` typically stores 4bytes(32bits) binary numbers, and it's max possible value is `INT_MAX`, which is the number +2147483647.

If we try to store a bigger number than +2147483647 then an undefined behaviour will occur(Search "MAX_INT overflow" for more info). one possible such behaviour is that the stored number becomes a negative one!

We can exploit this to make our `account_balance` increase because of subtracting a minus value in this line `account_balance = account_balance - total_cost;` (line 42).

So by overflowing to a big number(bigger than 10k) we can buy the l33t flag, and to do this:

+ We take the value of INT_MAX
+ Divide it by 900 so when we multiply it by 900 in line `total_cost = 900*number_flags;` (line 39) it overflows.
+ We multiply it with a value that gives us an account balance over 10k, I'll take 1.5

So: (INT_MAX/900)*1.5 = 3579138

Steps to get the flag:
1. Connect to the server using the following command: `nc jupiter.challenges.picoctf.org 9745`
2. Buy `3579138` flags from `Definitely not the flag Flag`, after buying your account balance will be over 10k
3. Buy `1` l33t flag from `1337 Flag`, you will get the flag: `picoCTF{m0n3y_bag5_65d67a74}`

## Final Answer

`picoCTF{m0n3y_bag5_65d67a74}`

## Description

> What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.


## Hints

> Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.


## Approach & Solution

If you're not familiar with this type of strings, they are called `hashes`. They are commonly used for encryption purposes, and the hash format above is a widely used one.

One way to identify hashes is using tools for that purpose. You can use google and search for "hash identifier". Here's [one](https://hashes.com/en/tools/hash_identifier).
Copy and paste the hash into the website above, the identification result will tell you that it's a `Base 64` encoded string, and it will also tell you what the decoded string is!
As you can see, the decoded string is `l3arn_th3_r0p35`.


## Final Answer
`picoCTF{l3arn_th3_r0p35}`

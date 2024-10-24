# Redirecting errors

## Code

```bash
/challenge/run > myflag 2> instructions
cat myflag
```
## Explanation

I learnt about A File Descriptor (FD)

and its types  FD 0: Standard Input ,FD 1: Standard Output,FD 2: Standard Error

and also that a > without a number implies 1> (standard output)

I used /challenge/run > myflag 2> instructions - where > is for standard output and 2> is for standard error

then i used cat myflag to get the flag

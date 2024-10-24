# Grepping errors

## Code

```bash
/challenge/run 2>&1|grep pwn.college
```
## Explanation

I used 2>&1 , redirects a standard error decipher to standard output decipher,

and then usingpipe operator i grepped it to find the flag ,

/challenge/run 2>&1|grep pwn.college

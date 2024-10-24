# Process Exit Codes

## Code

```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
43
hacker@processes~process-exit-codes:~$ /challenge/submit-code 43
CORRECT! Here is your flag:
pwn.college{oitkjpOWauvym6ot6FTJCIURmGY.dljN4UDLxkDN0czW}
```
## Explanation

I ran /challenge/get-code and then echo $? to retrieve the exit code 

then i ran /challenge/submit-code with the error code as an argument to get the flag

# Duplicating piped data with tee

## Code

```bash
/challenge/pwn | tee tmp | /challenge/college
cat tmp
/challenge/pwn --secret [SECRET_ARG]|tee tmp|/challenge/college
```
## Explanation

I used /challenge/pwn | tee tmp | /challenge/college to pipe /challenge/pwn to /challenge/college

but intercepted it by using tee tmp , then i used cat tmp to get the secret value

Then i used /challenge/pwn --secret [SECRET_ARG]|tee tmp|/challenge/college to get the flag

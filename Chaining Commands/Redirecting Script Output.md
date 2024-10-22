# Redirecting Script Output

## Code

```bash
touch script.sh
echo "/challenge/pwn" >> script.sh
echo "/challenge/college" >> script.sh
bash script.sh | /challenge/solve
```
## Explanation

I Created a script that runs multiple commands and redirect its output using piping.

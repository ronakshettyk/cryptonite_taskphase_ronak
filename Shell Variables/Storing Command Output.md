# Storing Command Output

## Code

```bash
PWN=$(/challenge/run)
```
## Explanation

I learned how to store the output of a command in a variable using command substitution, like PWN=$(command).
Took me some time to realize I have to use the $ sign to store the output from the command.
For this challenge, get output from /challenge/run into the PWN variable and then print it out to find the flag.

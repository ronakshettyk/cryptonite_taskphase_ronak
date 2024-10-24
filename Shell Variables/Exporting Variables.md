# Exporting Variables

## Code

```bash
export PWN=COLLEGE
COLLEGE=PWN
/challenge/run
```
## Explanation

I learned that variables set in a shell are local to that session and won't be inherited by child processes.
To share a variable with child processes, I need to export it using export VAR.
For this challenge, I need to export the PWN variable with the value COLLEGE and set the COLLEGE variable to PWN without exporting it.

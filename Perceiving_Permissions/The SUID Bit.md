# The SUID Bit

## Code

```bash
chmod u+s /challenge/getroot
/challenge/getroot
cat /flag
```
## Explanation

(SUID) permission allows users without root access to run programs with the privileges of the file's owner.
by applying the SUID bit to /challenge/getroot using chmod u+s, I made it executable with root privileges,
which enabled me to read the flag.

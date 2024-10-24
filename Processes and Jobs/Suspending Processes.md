# Suspending Processes

## Code

```bash
hacker@processes~suspending-processes:~$ /challenge/run
^Z
hacker@processes~suspending-processes:~$ /challenge/run
Yay, I found another version of me! Here is the flag:
pwn.college{8Gdgc24x3QCZgjbAlnCEM7Ce8uj.dVDN4QDLxkDN0czW}
```
## Explanation

Suspending processes in the terminal using Ctrl-Z, which sends them to the background.
For this challenge, I need to start /challenge/run, suspend it with Ctrl-Z, and then launch another copy while the first one is suspended.

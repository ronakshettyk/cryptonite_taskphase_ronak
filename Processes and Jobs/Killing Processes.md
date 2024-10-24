# Killing Processes

## Code

```bash
ps -ef | grep /challenge/dont_run
hacker        74      72  0 05:30 ?        00:00:00 /challenge/dont_run
kill 74
/challenge/run
```
## Explanation

Terminating processes in Linux using the kill command by providing the process ID (PID).
To find a process, I can use ps and grep, which took me some time to realize, since I didnt think of redirecting output and then grepping it, instead was manually doing it which takes a lot of time.
For this challenge, I need to locate the dont_run process and kill it to allow /challenge/run to execute.

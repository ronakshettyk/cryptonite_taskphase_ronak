# Permission setting practice

## Code

```bash
hacker@permissions~permissions-setting-practice:~$ /challenge/run
Round 0 (of 8)!
Current permissions of "/challenge/pwn": rw-r--r--
Needed permissions of "/challenge/pwn": rwx-wx-wx
hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,go=wx /challenge/pwn
You set the correct permissions!

Round 1 (of 8)!
Current permissions of "/challenge/pwn": rwx-wx-wx
Needed permissions of "/challenge/pwn": -wxr-xrw-
hacker@permissionspermissions-setting-practice:$ chmod u=wx,g=rx,o=rw /challenge/pwn
You set the correct permissions!

Round 2 (of 8)!
Current permissions of "/challenge/pwn": -wxr-xrw-
Needed permissions of "/challenge/pwn": r--------
hacker@permissionspermissions-setting-practice:$ chmod u=r,og= /challenge/pwn
You set the correct permissions!

Round 3 (of 8)!
Current permissions of "/challenge/pwn": r--------
Needed permissions of "/challenge/pwn": r-xrw----
hacker@permissionspermissions-setting-practice:$ chmod u=rx,g=rw,o= /challenge/pwn
You set the correct permissions!

Round 4 (of 8)!
Current permissions of "/challenge/pwn": r-xrw----
Needed permissions of "/challenge/pwn": --x-wx-wx
hacker@permissionspermissions-setting-practice:$ chmod u=x,go=wx /challenge/pwn
You set the correct permissions!

Round 5 (of 8)!
Current permissions of "/challenge/pwn": --x-wx-wx
Needed permissions of "/challenge/pwn": -------wx
hacker@permissionspermissions-setting-practice:$ chmod ug=,o=wx /challenge/pwn
/usr/bin/chmod: cannot access ',o=wx': No such file or directory
You set the correct permissions!

Round 6 (of 8)!
Current permissions of "/challenge/pwn": -------wx
Needed permissions of "/challenge/pwn": -wxr--r--
hacker@permissionspermissions-setting-practice:$ chmod u=wx,go=r /challenge/pwn
You set the correct permissions!

Round 7 (of 8)!
Current permissions of "/challenge/pwn": -wxr--r--
Needed permissions of "/challenge/pwn": -wxr-xr--
hacker@permissionspermissions-setting-practice:$ chmod u=wx,g=rx,o=r /challenge/pwn
You set the correct permissions!

You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
hacker@permissions~permissions-setting-practice:~$ chmod u=r /flag
hacker@permissions~permissions-setting-practice:~$ cat /flag
pwn.college{0BaVPpDI7ajnOaamYux6OI7wVdF.dNTM5QDLxkDN0czW}
```
## Explanation

Learnt how to set file permissions using chmod with the = operator, which overwrites existing permissions,
as opposed to simply adding or removing them with + and -.
This reinforced my understanding from the previous challenge while introducing the concept of chaining permissions for different user categories using ','.
Also taught me you can zero out permissions with u=  for example.

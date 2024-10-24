# Permission Tweaking Practice

# Explanation and Code

```bash
I changed the permission of the file 8 times to finally get the ownership of the /flag file

hacker@permissions~permission-tweaking-practice:~$ /challenge/run
Round 0 (of 8)!
Current permissions of "/challenge/pwn": rw-r--r--
Needed permissions of "/challenge/pwn": rwxr-xr-x
hacker@permissions~permission-tweaking-practice:~$ chmod o-r /challenge/pwn

Round 1 (of 8)!
Current permissions of "/challenge/pwn": rw-r-----
Needed permissions of "/challenge/pwn": rwxr-xr-x
hacker@permissions~permission-tweaking-practice:~$ chmod gou+x o+r /challenge/pwn

Round 2 (of 8)!
Current permissions of "/challenge/pwn": rwxr-xr-x
Needed permissions of "/challenge/pwn": rwxr-xrwx
hacker@permissions~permission-tweaking-practice:~$ chmod o+w /challenge/pwn

Round 3 (of 8)!
Current permissions of "/challenge/pwn": rwxr-xrwx
Needed permissions of "/challenge/pwn": rwxr--r--
hacker@permissions~permission-tweaking-practice:~$ chmod go-x o-w /challenge/pwn

Round 4 (of 8)!
Current permissions of "/challenge/pwn": rwxr--r--
Needed permissions of "/challenge/pwn": rwxrw-rw-
hacker@permissions~permission-tweaking-practice:~$ chmod go+w /challenge/pwn

Round 5 (of 8)!
Current permissions of "/challenge/pwn": rwxrw-rw-
Needed permissions of "/challenge/pwn": rw-rw-rw-
hacker@permissions~permission-tweaking-practice:~$ chmod u-x /challenge/pwn

Round 6 (of 8)!
Current permissions of "/challenge/pwn": rw-rw-rw-
Needed permissions of "/challenge/pwn": rw----rw-
hacker@permissions~permission-tweaking-practice:~$ chmod g-rw /challenge/pwn

Round 7 (of 8)!
Current permissions of "/challenge/pwn": rw----rw-
Needed permissions of "/challenge/pwn": rw-----w-
hacker@permissions~permission-tweaking-practice:~$ chmod o-r /challenge/pwn

You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!
Current permissions of "/flag": ---------
hacker@permissions~permission-tweaking-practice:~$ chmod u+r /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{s21wreeYKqOPNasSXAL982YHQ2_.dBTM2QDLxkDN0czW}
```

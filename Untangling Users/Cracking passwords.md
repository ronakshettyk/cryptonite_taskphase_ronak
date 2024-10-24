# Cracking passwords

## Code

```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04950g/s 288.2p/s 288.2c/s 288.2C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:aardvark
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{k9ivUg8nDB5ChgUILijvjdJzfkt.ddTN0UDLxkDN0czW}
```
## Explanation

For  security, user passwords are now kept in /etc/shadow instead of /etc/passwd.
The su command verifies the hashed password against the hash in /etc/shadow when switching users.
I performed a simulation of cracking a leaked password hash using John the Ripper,
which successfully uncovered Zardus' password. This allowed me to switch users and obtain the flag.

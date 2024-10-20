#Perceiving Permissions 
    
  ##Changing File Ownership
    
    you can change who owns a file in Linux by using the chown command.
    once I switched the ownership of the /flag file from root to my user account, I was able to open it without any problems.
    
    chown hacker /flag
    cat /flag
    
  ##Groups and Files
    
    in Linux, you can change the group ownership of a file.
    I changed the group of the /flag file to hacker by using chgrp hacker /flag, which gave me access to read the flag.
    
    chgrp hacker /flag
    cat /flag
    
   ##Fun with Group Names
    
    when I used the id command, I discovered my group name was randomly assigned as grp22807. 
    I then used chgrp grp22807 /flag to change the group ownership of the /flag file accordingly.
    
    id
    chgrp grp/16266 /flag
    cat /flag
    
  ##Changing Permissions
    
    I adjusted file permissions using the chmod command.
    By running chmod o+r /flag to grant read access to all others , I was able to read the flag successfully.
    
    chmod o+r /flag
    cat /flag
    
  ##Executable Files
    
    This challenge taught me about execute permissions.
    I realized I needed to give myself execute permission by using chmod u+x /challenge/run
    
    chmod u+x /challenge/run
    /challenge/run
    
  ##Permission Tweaking Practice 
    
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
    
   ##Permission setting practice
    
    Learnt how to set file permissions using chmod with the = operator, which overwrites existing permissions,
    as opposed to simply adding or removing them with + and -.
    This reinforced my understanding from the previous challenge while introducing the concept of chaining permissions for different user categories using ','.
    Also taught me you can zero out permissions with u=  for example.
    
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
    
  ##The SUID Bit
    
    (SUID) permission allows users without root access to run programs with the privileges of the file's owner.
    by applying the SUID bit to /challenge/getroot using chmod u+s, I made it executable with root privileges, which enabled me to read the flag.
    
    chmod u+s /challenge/getroot
    /challenge/getroot
    cat /flag
    
    
    
    
    
    
    
    
    
    
    
    
    

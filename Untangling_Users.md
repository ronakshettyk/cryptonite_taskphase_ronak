#Untangling Users 
    
  ##Becoming root with su
    
    We learnt about,
    su command, allows users to switch to the root account
    su binary has the SUID bit set, enabling it to run with root privileges
    and also that Modern systems very rarely have root passwords, and different mechanisms
    
    su
    Password:hack-the-planet
    cat /flag
    
   ##Other users with su
    
    i learnt
    su command can be used to switch to any user by specifying their username
    
    su zardus
    Password:dont-hack-me
    /challenge/run
    
  ##Cracking passwords
    
    For  security, user passwords are now kept in /etc/shadow instead of /etc/passwd.
    The su command verifies the hashed password against the hash in /etc/shadow when switching users.
    I performed a simulation of cracking a leaked password hash using John the Ripper,
    which successfully uncovered Zardus' password. This allowed me to switch users and obtain the flag.
    
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

  ##Using Sudo

     Linux systems prefer using sudo instead of su for administrative tasks, 
     as sudo allows users to execute particular commands as the root user based on their assigned permissions.

     hacker@users~using-sudo:~$ sudo cat /flag
     pwn.college{Y140_3TwOm8MTZXGVpFPBo15iNg.dhTN0UDLxkDN0czW}
    

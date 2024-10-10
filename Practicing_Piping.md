#Practicing Piping

  ##Redirecting output
    
    I learnt about redirection of outputs
    
    I used > to redirect the output of echo PWN to a file named COLLEGE
    
    i.e.  echo PWN > COLLEGE to get the flag 
    
   ##Redirecting more outputs
    
    I used /challenge/run > myfile to redirect the output of the command
    
    /challenge/run to the file named my file , then i used cat myfile to read the file to get the flag
    
   ##Appending Outputs
    
    I learnt about the appending the outputs,
    
    using >> instead of > i could append the outputs , instead of deleting the old contents
    
    I used /challenge/run >> /home/hacker/the-flag to append the output of /challenge/run 
    
    then i used cat /home/hacker/the-flag to get the flag
    
   ##Redirecting errors
    
    I learnt about A File Descriptor (FD
    
    and its types  FD 0: Standard Input ,FD 1: Standard Output,FD 2: Standard Error
    
    and also that a > without a number implies 1> (standard output)
    
    I used /challenge/run > myflag 2> instructions - where > is for standard output and 2> is for standard error
    
    then i used cat myflag to get the flag
    
  ##Redirecting input
    
    I used echo COLLEGE > PWN to redirect the output COLLEGE to PWN file
    
    then i used /challenge/run < PWN to redirect the input 
    
  ##Grepping stored results
    
    I used /challenge/run > /tmp/data.txt to redirect output of the command
    
    /challenge/run to the file , then i used grep pwn.college /tmp/data.txt to get the flag.
    
  ##Grepping live output
    
    I grepped the flag from /challenge/run using the pipe operator - |
    
    i used /challenge/run|grep pwn.college to get the flag
    
  ##Grepping errors
    
    I used 2>&1 , redirects a standard error decipher to standard output decipher,
    
    and then usingpipe operator i grepped it to find the flag ,
    
    /challenge/run 2>&1|grep pwn.college
    
  ##Duplicating piped data with tee
    
    I used /challenge/pwn | tee tmp | /challenge/college to pipe /challenge/pwn to /challenge/college
    
    but intercepted it by using tee tmp , then i used cat tmp to get the secret value
    
    Then i used /challenge/pwn --secret [SECRET_ARG]|tee tmp|/challenge/college to get the flag
    
  ##Writing to multiple programs
    
    I used the /challenge/hack command and duplicated its output as an input to /challenge/the and /challenge/planet
    
    i used /challenge/hack | tee >(/challenge/the) >(/challenge/planet) to get the flag
    
  ##split-piping stderr and stdout
    
    i used  /challenge/hack to get the challenge which told to direct standard output to /challenge/planet
    
    and standard error  to /challenge/the, i used /challenge/hack > >(/challenge/planet) 2> >(/challenge/the) to do it and get the flag
    

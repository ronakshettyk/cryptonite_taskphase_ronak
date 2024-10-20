 #Pondering PATH

    
   ##The PATH Variable
    
    I used PATH="" to disrupt the operation of the /challenge/run program, then ran /challenge/run which could not
    find the rm command and hence could not delete the flag
    
    PATH=""
    /challenge/run
    
  ##Setting PATH
    
    I set the path to the directory where the command was present and then executed the command directly
    
    PATH=/challenge/more_commands/
    /challenge/run
    
   ##Adding commands
    
    i used find / -name bash to get the bash to get the path to bash
    then used the ln command to create links between files .
    the command PATH=/home/hacker/:$PATH sets the PATH variable to include the /home/hacker/ directory at the beginning,
    ensuring that any executables in that directory are found first by the shell.
    
    ln -s /usr/bin/bash ./win
    PATH=/home/hacker/:$PATH
    /challenge/run
    cat /flag
    
    (REFERENCES : used help from chat gpt)
    
   ##Hijacking Commands
    
    I used ln command to create a link between the files then used the 
    command PATH=/home/hacker/:$PATH setting the PATH variable to include the /home/hacker/ directory at the beginning,
    ensuring that any executables in that directory are found first by the shell.
    then used /challenge/run to get the flag
    
    ln -s /usr/bin/bash ./rm
    PATH=/home/hacker/:$PATH
    /challenge/run

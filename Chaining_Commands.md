#Chaining Commands
    
  ##Chaining with semicolons
      
    you can chain commands in the shell using a semicolon (;), allowing multiple commands to run sequentially
    
    /challenge/pwn;/challenge/college
    
  ##Your First Shell Script
    
    I create a shell script called x.sh and run the commands /challenge/pwn and /challenge/college using echo
    
     touch x.sh
     echo "/challenge/pwn" >> x.sh
     echo "/challenge/college" >> x.sh
     bash x.sh
    
  ##Redirecting Scripts Output
    
     I Created a script that runs multiple commands and redirect its output using piping.
    
     touch script.sh
     echo "/challenge/pwn" >> script.sh
     echo "/challenge/college" >> script.sh
     bash script.sh | /challenge/solve
    
   ##Executable Shell Scripts
    
     I created a shell script , invoked /challenge/solve in it, made it executable and ran it without using bash command
    
     touch x.sh
     echo "/challenge/solve" >> x.sh
     ls -l x.sh
     chmod u+x x.sh
     ./x.sh
     
    
     
      
    

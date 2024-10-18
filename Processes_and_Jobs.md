#Processes and Jobs
    
  ##Listing Processes
    
    Listing running processes with the ps command.
    Unlikes and likes between ps -ef for details or ps aux.
    For this challenge, I need to find a renamed /challenge/run in the process list and relaunch it to get the flag.
    
    ps -ef
    /challenge/15088-run-30630
    
  ##Killing Processes
    
    Terminating processes in Linux using the kill command by providing the process ID (PID).
    To find a process, I can use ps and grep, which took me some time to realize, since I didnt think of redirecting output and then grepping it, instead was manually doing it which takes a lot of time.
    For this challenge, I need to locate the dont_run process and kill it to allow /challenge/run to execute.
    
    ps -ef | grep /challenge/dont_run
    hacker        74      72  0 05:30 ?        00:00:00 /challenge/dont_run
    kill 74
    /challenge/run
    
   ##Interrupting Processes
    
    Using Ctrl+C to interrupt and terminate processes running in the terminal.
    This sends an "interrupt" signal, allowing the application to exit cleanly.
    For this challenge, I need to use Ctrl+C to interrupt /challenge/run to get the flag.
    
    /challenge/run
    then i used CTRL+C to interrupt and get the flag
    
  ##Suspending Processes
    
    Suspending processes in the terminal using Ctrl-Z, which sends them to the background.
    For this challenge, I need to start /challenge/run, suspend it with Ctrl-Z, and then launch another copy while the first one is suspended.
    
    hacker@processes~suspending-processes:~$ /challenge/run
    ^Z
    hacker@processes~suspending-processes:~$ /challenge/run
    Yay, I found another version of me! Here is the flag:
    pwn.college{8Gdgc24x3QCZgjbAlnCEM7Ce8uj.dVDN4QDLxkDN0czW}
    
   ##Resuming Processes
    
    I learnt about resuming a process after suspending it
    /challenge/run
    ^Z
    fg
    
   ##Backgrounding processes
    
    I learnt about resume processes in the background with the bg command! 
    
    /challenge/run
    ^Z
    bg
    /challenge/run
    
   ##Foregrounding processes
    
    I learnt that you can foreground a backgrounded process with fg
    
    /challenge/run
    ^Z
    bg
    fg
    to get the flag
    
  ##Starting backgrounding processes
    
    Starting a process in the background by appending & to the command.
    This allows it to run without taking over the terminal.
    For this challenge, I need to launch /challenge/run in the background to get the flag.
    
    /challenge/run &
    
  ##Process Exit Codes
    
    I ran /challenge/get-code and then echo $? to retrieve the exit code 
    
    then i ran /challenge/submit-code with the error code as an argument to get the flag
    
    hacker@processes~process-exit-codes:~$ /challenge/get-code
    Exiting with an error code!
    hacker@processes~process-exit-codes:~$ echo $?
    43
    hacker@processes~process-exit-codes:~$ /challenge/submit-code 43
    CORRECT! Here is your flag:
    pwn.college{oitkjpOWauvym6ot6FTJCIURmGY.dljN4UDLxkDN0czW}
    

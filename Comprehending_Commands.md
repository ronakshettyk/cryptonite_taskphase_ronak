#Comprehending Commands

  ##cat: not the pet, but the command!

    I use cat flag to copy the flag to the flag file in my home directory and read it

  ##catting absolute paths
    
    Used cat /flag to read the flag using its absolute path
    
  ##more catting practice
    
    starting the program just gives me the absolute path of the flag,
    
    i use cat command to read the flag using its absolute path
    
   ##grepping for a needle in a haystack
    
    I learnt about a new command called grep
    
    used to search file lines for text containing the required text
    
    grep search_text <path> gave me the flag
    
   ##listing files
    
    using ls command I list the files in the /challenge directory
    
    and then i just use /challenge/<file name> to get the flag
    
  ##touching files
    
    i change my directory to tmp using cd command
    
    then i use touch command to create new files ,
    
    namely college and pwn and then use /challenge/run to obtain the flag
    
   ##removing files
    
    I use the rm command to delete a file already created 
    
    and then run /challenge/check to get the flag
    
   ##hidden files
    
    I use the cd command to go the / directory
    
    then i use the ls -a command to search for hidden files
    
    and then i read the hidden flag file using cat command
    
   ##An Epic Filesystem Quest
    
    Start by changing the directory to / using cd command
    
    then use ls command to list the files 
    
    use cat command to read the file and then cd command to changle the directory to the given one
    
    again repeat the process.
    
    for delayed type of file use ls to list the files
    
    for hidden file, list the files using ls -a command
    
    for trapped files , use ls <directory> to list the file
    
    and then use cat <directory><filename> to get the next clue
    
    repeating it multiple times finaly gives the flag.
    
   ##making directories
    
    I just use mkdir command to make a directory
    
    and then used touch command to make the file
    
  ##finding files
    
    I used "find / -name flag" to search the entire filesystem for the file named flag
    
    and then executed all the available files to get me the flag
    
  ##linking files
    
    i used ln -s /flag /home/hacker/not-the-flag to create symlink
    
    then used /challenge/catflag to fool it and obtain the flag.



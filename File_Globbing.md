#File Globbing

  ##Matching with *
    
    Here i learnt about the one of the globs , i.e '*'
    
    it tries to replace that argument with any files that match the pattern 
    
    except for /, i used cd /ch* , thus getting into the challenge directory 
    
    thus obtained the flag.
    
  ##Matching with ?
    
    Its similar to * but it replaces only single character
    
  ##Matching with [ ]
    
    its a limited form of ?, we use the brackets to write in potential characters
    
    i used cd /challenge/files to get into the directory and then
    
    /challenge/run files[habs] to get the flag
    
  ##Matching paths with []
    
    I start from my home directory and run
    
    /challenge/run /challenge/files file_[hasb]
    
    to get the flag
    
  ##Mixing globs
    
    I used cd /challenge/files to change directory
    
    then used ls to check all the files, where i found out all files have different starting alphabets
    
    thus i used /challenge/run/ [cep]* to get the flag
    
  ##Exclusionary globbing
    
    I learnt that [!] gives u all the the files that does not contain the letter given in the bracket
    
    i used /challenge/run [!pwn]* to get all the files that do not start with p,w or n.



#Pondering Paths



##The Root



I invoked the /pwn command to get the absolute path



##Program and absolute paths



I executed the program called "run" using /challenge/run command where /challenge is the directory



##Position thy self



I ran the /challenge/run command where it showed me the diretory i should be in ,

which was "/etc/apt/sources.list.d", i ran cd to change the directory to the given one

and executed /challenge/run again to get the flag.



##Position elsewhere



I ran the /challenge/run command where it showed me the diretory i should be in ,

which was "/home", i ran cd to change the directory to the given one

and executed /challenge/run again to get the flag.



##Position yet elsewhere



I ran the /challenge/run command where it showed me the diretory i should be in ,

which was "/sys/kernel", i ran cd to change the directory to the given one

and executed /challenge/run again to get the flag.

##implicit relative paths, from /

I learnt about the difference between relative and absolute path,

Relative path does not start with "/"

I ran the /challenge/run command where it showed me the diretory i should be in ,

which was "/", i ran cd to change the directory to the given on

and executed challenge/run to get the flag.



##explicit relative paths, from /



Here i learnt that relative paths do not need to start blank , they can start with ./ or ././ 

other things are similar to the previous one

##implicit relative path

here i learnt about a safety feature in linux which stops you to execute 

the program directly from the relative directory as we could accidentally execute programs

in our current directory.

I used ./run command to execute the program from the relative directory



##home sweet home



using cd ~ i go to my home directory

I used /challenge/run command with ~/r as an absoulte argument

to obtain the flag








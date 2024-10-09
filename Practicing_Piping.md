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


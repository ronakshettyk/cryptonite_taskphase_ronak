#Shell Variables

##Printing Variables

Pretty straight forward.
Understood how to use the echo command to print variable values in the shell, specifically using $ to reference variables like FLAG in this case.

echo $FLAG

##Setting Variables

Learnt how to assign values to variables in the shell using VAR=value without spaces around the =.
I also understood that I use $ only when I want to access the variable's value. For this challenge, I need to set the variable PWN to COLLEGE.

PWN=COLLEGE

##Multi-word Variables

Learnt about quoting in the shell to handle spaces in variable assignments.
Spaces are significant, so when I want to set a variable like VAR to a value that includes spaces, I need to use quotes so it considers it as one token.

PWN="COLLEGE YEAH"

##Exporting Variables

I learned that variables set in a shell are local to that session and won't be inherited by child processes.
To share a variable with child processes, I need to export it using export VAR.
For this challenge, I need to export the PWN variable with the value COLLEGE and set the COLLEGE variable to PWN without exporting it.

export PWN=COLLEGE
COLLEGE=PWN
/challenge/run

##Printing Exported Variables

Theenv command, which lists all exported variables in the current shell.
This allows me to find the FLAG variable among them for this case.

env

##Storing Command Output

I learned how to store the output of a command in a variable using command substitution, like PWN=$(command).
Took me some time to realize I have to use the $ sign to store the output from the command.
For this challenge, get output from /challenge/run into the PWN variable and then print it out to find the flag.

PWN=$(/challenge/run)

##Reading Input

Using the read command to take user input in the shell.
I can specify a prompt with -p, like read -p "INPUT: " MY_VARIABLE.
For this challenge, I need to use read to set the variable PWN to COLLEGE.

read -p "Input: " PWN
Input: COLLEGE

##Reading Files

Learnt that instead of using cat to read a file into a variable, I can use input redirection with the read command.
By doing read VAR < filename, I can directly read the contents of a file into a variable.
For this challenge, I need to read /challenge/read_me into the PWN variable to get the flag.

read PWN < /challenge/read_me

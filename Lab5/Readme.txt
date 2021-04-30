Go to your home directory and create a new file named as simple.sh
(vi simple.sh or nano simple.sh), then include following lines in your
simple.sh.
#!/bin/bash
#
#Simple Script
#
echo Congratulations! Now you know shell script!
echo -n "The current time and date are: "
date

Step 2: Save your file and exit editor.
Step 3: Execute this file by invoking its name.
$ simple.sh

1

Question 1) : What did you see in the output of step 3?
Step 4: Execute this file by adding ./ before the its name.
$ ./simple.sh
Question 2) : What did you see in the output of step 4?
Step 5: Try following command to make simple.sh executable.
$chmod a+x simple.sh
Step 6: Execute this file again.
$ ./simple.sh
Note: you must type ./ before the name. This is because current working directory is not in
PATH. However, you can modify the value of PATH variable and add current working
directory into it by referring to next part.
Question 3): Attach a screenshot of the output in step 6.
Question 4): Describe the meaning of -n option in echo command.
Read the slides #13 in Chapter 4 and then answer the following two
questions.
Question 5): Is "Simple Script" a comment? If not, what is the meaning of it or
why we use it?
Question 6): Is "#!/bin/bash" a comment? If not, what is the meaning of it or
why we use it in first line?

Part 2:
To discard the ./ before the script file name when executing it, we
need to change the PATH variable's value and add current working
directory into it.
Step 7: Print out the value stored in PATH variable.
Question 7) : How many directories you can find in the output?
Note: the directories are separated by colon.
Step 8: Try command below to insert current working directory at the
beginning of the string value stored in PATH variable.
$PATH=.:$PATH

2

Step 9: Execute simple.sh again by trying following command.
$simple.sh
$ simple.sh
Question 8) : Can you find errors prompted in step 9 ? If not, please briefly
describe why there is no need to put ./ before the file name.
Step 10: Log out the connection to the snowball server and reconnect to it. Or
simply close your terminal and then reopen your terminal.
Step 11: Print out the value stored in PATH variable again.
Question 9: Can you find the current working directory . in the PATH variable?

Step 11: Execute simple.sh again by trying following command.
$simple.sh
$ simple.sh
Question 10) : Can you find errors prompted in step 11 ? If yes, please explain
why?
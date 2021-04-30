In order to finish the tasks in this lab, you must connect to
snowball server to copy my checkError.sh
$cp /home/yye10/public/checkError.sh checkError.sh
In Lab 5, you may have tried the shell script checkError.sh in part
3. However, there are four errors on four different lines in that shell
script. Please correct all the four errors by writing down the line
number, the error and the correction as below:
Line #: Error: Correction:
Note: please use cat -n to check the line numbers.
$#/bin/bash
/* Check Error Script */
echo "Try to find out some errors!!!"
# Seach for the words which can be matched by regex [^a]*ce
# And save the output to file "Result"
echo "The regex [^a]*ce can match the string(s):" > Result
grep '^[^a]*ce$' << END >> Result lance
ace
brace
decide
piece
-ENDHERE
# Check the existence of file "Result"
# Send the content in "Result" to your emailbox
# $1 is replaced by your campusID
ls mail $1@student.gsu.edu < Result
# $1 is replaced by your campusID
echo "The result has been sent to ${1}@student.gsu.edu"
echo "Congratulations! You have corrected all the errors!"
1

Hints:
 Following is a sample of the output once all the errors are
corrected $ ./checkError.sh ylong4
Try to find out some errors!!!
checkError.sh Result
The result has been sent to ylong4@student.gsu.edu
Congratulations! You have corrected all the errors!
 You would also receive an email sent from your snowball account once all the
errors are corrected.
 You may need to use CTRL-C to terminate the execution of the command, especially for
the script file with errors.
Part 2:
Write a single shell script hello.sh which can finish the list of tasks
as below:
1. Greet user. E.g. Welcome to computer science society.
2. Contain a comment section with your name, and email address.
3. Print the date.
4. Print the number of directories in /home .
5. Print the value of variables PATH, USER and SHELL.
6. Print your disk usage (df).
7. Print Please, could you loan me $25.00?
8. Print if x = 2, x * x = 4 , x / 2 = 1
9. List all the .sh files with c at the beginning of the file name in current working
directory.
10. Tell the user Good bye and the current hour (see manual page of date command

refer to the webpage at http://www.thegeekstuff.com/2013/05/date-command-
examples )

Include the content of hello.sh in your answer sheet. Besides, please
also upload hello.sh as a separated file.
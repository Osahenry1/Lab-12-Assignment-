Go to your home directory (cd ~) and create a new file named as foo.sh (vi foo.sh

or nano foo.sh), then include following lines in your foo.sh.

Step 2: Save your file and exit editor.

Step 3: Try following command to make simple.sh executable.
$chmod a+x foo.sh
Step 4: Execute this file by invoking its name.
$./foo.sh

Note: when typing the shell script in your terminal, please be very careful of the spaces.

1

Questions:
1) Attach a screenshot of the output in step 4.

2) Describe what does the shell script foo.sh do?
Part B:
Step 1: Edit your foo.sh and change “ -le 3 ” to “ -le $1 ” .
Step 2: When finished, save the foo.sh and exit editor. Then try executing it again by typing
following command.
$./foo.sh 5
Question:
Attach a screenshot of the output.

Part C:
Step 1: Edit your foo.sh in part B by making following modifications:
 Add two new lines below between line “i=1” and line “while [ $i -le $1 ]”
echo please input a number
read num
 Change “ -le $1 ” to “ -le $num ” .
Step 2: When finished, save the foo.sh and exit editor. Then try executing it again by typing
following command and type 5 as the input of the number.
$./foo.sh
Question:
Attach a screenshot of the output.

Part D:
Write a Java program named foo.java to accomplish the same task as that in foo.sh of Part
A.
Note: If you want to run your Java program in terminal,
 to compile foo.java, please try
$javac foo.java
 To execute it, please try
$java foo

Question:

2

Then put the source code of foo.java in your answer sheet.

Part E:
Create and run Kernighan and Ritchie’s famous “hello,world” program.
Step 1: Go to your home directory (cd ~) and create a new file named as hello.c (vi hello.c
or nano hello.c), then include following lines in your hello.c .
#include <stdio.h>
int main(void)
{
printf("Hello,world\n");
return 0;
}
Step 2: Save your file and exit editor.
Step 3: Compile and link the hello.c program by following command.
$cc hello.c
Note: after this command, a default executable program named as “a.out” will be generated
in current directory if there are no errors with your C program. You can use ls to check the
existence of a.out .
Step 4: Run the executable program a.out
$./a.out

Questions:
1) Attach a screenshot of the output in step 4.
2) Try following command to compile and link hello.c again. And tell what new file is
generated after this command?
$cc -o hello hello.c
3) Try command below and attach a screenshot of the output.
$./hello
4) Now write a new C program named as myName.c based on hello.c. In this program,
print out your first name and last name instead of “Hello,world”. For example, the output
could be “My name is Yuan Long”.
Execute your myName.c and attach a screenshot of the output. Then write the source code

of myName.c in your answer sheet and upload your file myName.c to classroom.
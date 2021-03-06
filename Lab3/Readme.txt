Open your terminal and connect to snowball server. Change your directory to your
home directory (cd ~ ), and then create a new directory named as “Lab3” (mkdir
Lab3). After that, go to directory Lab3 (cd Lab3) and please download the file
"Try.c" (content shown in table below) by the following command (internet access
required):
cp /home/frondel1/Public/Try.c Try.c
Be sure it succeeds using “ls” to see the file name “Try.c” listed.

//Try.c
#include <stdio.h>
#include <stdlib.h> /* For exit() function */
int main(int argc, char *argv[]) {
FILE *fptr;
fptr=fopen("program.txt","a+");
if(fptr==NULL){
printf("Error!");
exit(1);
}
fprintf(fptr,"program is written");
printf("program is written in program.txt");
fclose(fptr);
return 0;
}

Try the following steps by issuing some commands in your vi
editor 1) Open "Try.c" with vi editor
$vi Try.c

1

2) Move cursor to the beginning of “Error!”
use UP DOWN LEFT RIGHT arrow to control cursor
3) Insert “xxx”.
i
type “xxx” (hit x three times)
4) Append a blank line after the current line.
Hit Esc to command mode
o (lowercase o)
5) Delete “xxx”.
Hit Esc to command mode.
Move cursor to the beginning of "xxx", press x three times
or press 3s to delete "xxx"
6) Copy the first 2 lines, move cursor to the beginning of file, and then paste it
after current line
:1,2y
:0
p
7) Delete the first 2 lines
:1,2d
8) Save it
:w
9) Replace all "fptr" with "FPTR"
:1,$s/fptr/FPTR/g
10) Save and exit.
:wq

2

Part 2: VI Editing - Large file
1) Go into your Lab3 directory.
$cd ~/Lab3
2) Copy "RealEstate.csv" from instructor's public directory to your Lab3 directory
again.
$cp /home/frondel1/Public/RealEstate.csv .
Please write the commands you will issue to complete the following tasks and
answering corresponding questions step by step in your report.
3) Use vi to open “RealEstate.csv”.
4) Move the cursor to the last line (without knowing the number of last line).
5) Display line number.
6) Search for the transaction for the estate located at "111 EAST"
Which line is this string located? (Please just write down the line number)
Delete this line.
7) Move the cursor to the line 50.
8) Substitute all comma "," with colon ":" from line 50 to line 54.
9) Copy line 50 to line 54 to the end of file.
10)Remove line 50 to line 54.
11) Describe how to enter the text mode and insert a new line "Recorded in year
2008" between line 1 and line 2.
12) Switch back to command mode.
13) Save the file and quit vi.

3

Part 3: Permissions for files
Follow the instructions step by step and finish the questions as required.
1) Go into your Lab3 directory.
$cd ~/Lab3
2) Check the file permissions for file "Try.c" in your own Lab3 directory.
$ls -l Try.c
3) You may see similar output as below, in which rw-rw-r-- of the first field is
the file permission string for "Try.c".
[frondel1@gsuad.gsu.edu@snowball Lab3]$ ls -l Try.c
-rw-rw-r--. 1 frondel1@gsuad.gsu.edu frondel1@gsuad.gsu.edu 379 Jan 28 11:57
Try.c
 The leftmost 3 characters rw- tells us that the user (owner of the file)
can only read and write the file.
 The middle 3 characters rw- tells us the other users in the same group
as the owner can only read and write the file.
 The last 3 characters r-- tells us the other users in the other groups
different from owner can only read the file.
Note: once you copy a file from other directory or download a file from other resources, you are
the owner of the new copied or downloaded file.
4) Remove the read permission for the owner (yourself).
$chmod u-r Try.c
5) Check the file permissions for file "Try.c" again.
$ ls -l Try.c
6) You may see similar output as below, in which -w-rw-r-- of the first field is
the file permission string for "Try.c".
[frondel1@gsuad.gsu.edu@snowball Lab3]$ ls -l Try.c
--w-rw-r--. 1 frondel1@gsuad.gsu.edu frondel1@gsuad.gsu.edu 379 Jan 28 11:58
Try.c
So -w- in the leftmost 3 characters tells us that the user (owner of the file )
only has the permission to write something into the file.
7) Try the vi editor again to modify the file.
$vi Try.c

4

8) However, you may find following message displayed at the bottom of
the screen which means you do not have the right to read "Try.c".
"Try.c" [Permission Denied] 0,0-1 All
9) Quit vi editor.
:q

10) Try read "Try.c" again using cat.
$cat Try.c
Attach a screenshot of the output.
11) Use chmod with an octal number to let all the users only have read
permission for "Try.c".
$chmod 444 Try.c
Note: The permission string to be set should be r--r--r--. Convert each group of three characters into
decimal to form an octal number, which should be 444.
12) Check the file permissions for file "Try.c" again. And explain the meaning of
each character in the file permission string.

13) Try the vi editor again to modify the file. Then remove one line by pressing dd
$vi Try.c
Move your cursor to some line and press dd
14) Try to save the file in the vi editor.
:w
15) Can you find some error message at the bottom of the screen? If yes, what is
it and how to quit the vi editor without saving the modification.
Write answer in your answer sheet.
16) Use chmod to add write the permission to all the users for "Try.c".
Write answer in your answer sheet.
17) Check the file permissions for file "Try.c" again. And explain the meaning
of each character in the file permission string.
Write answer in your answer sheet.

5

Part 4: Permissions for directories
The permissions also work for the directories. However, the permissions for the
directories may have different behaviors.
Let us learn the permissions for directories by only changing different permissions
to the owner of the file.
1) Go to your home directory and then check the permissions for directory Lab3.
$cd ~
$ls -ld ~/Lab3
Note: -d option will let you check the detailed information for the directory instead of its contents.
2) You may see similar output as below, in which rwxrwxr-x of the first field
is the permission string for directory Lab3.
ls -ld ~/Lab3
drwxrwxr-x. 4 frondel1@gsuad.gsu.edu frondel1@gsuad.gsu.edu 4096 Jan 28 11:58
/home/frondel1/Lab3
3) Use chmod with octal number to forbid all permissions to all users.
$chmod 000 ~/Lab3
4) Check the permissions for directory Lab3. You may see similar output as
below. The permission string is changed to ---------.
ls -ld ~/Lab3
d---------. 4 frondel1@gsuad.gsu.edu frondel1@gsuad.gsu.edu 4096 Jan 28
11:59 /home/frondel1/Lab3
5) Finishing the following tasks and fill out the blanks in the row for owner's
permission "---" in the table below. If the task or command can be executed
successfully, mark Y in the table, otherwise, mark N in the table. Please mark
N/A if the task or command is not executed.
A. Check the contents in directory Lab3.
$ls ~/Lab3
B. Create a directory named as "test" in Lab3.
$mkdir ~/Lab3/test
C. Create a file named as "test.txt" in Lab3.
$cat>~/Lab3/test.txt
A test
^D

6

D. If (B) succeeds, remove the created directory "test" of Lab3.
$rm -r ~/Lab3/test
E. If (C) succeeds, copy "test.txt" from your Lab3 into your home
directory.
$cp ~/Lab3/test.txt .

F. Go into directory Lab3.
$cd ~/Lab3

The blanks in row "---" have been filled out in the table. Please compare it to your
answers.
6) Fill out the blanks in other rows by repeating 3) to 5) when the owner is assigned
different permissions as in the first column of the table. However, when setting the
permissions, we still need to forbid all the permissions to all other users. So the
last two bits in the octal number should always be kept as 00.
For example, since owner's permissions is --x at next row, we should first set the file permission
by issuing the command chmod 100 ~/Lab3. And then fill out the blanks in the row for
permissions --x by repeating 5).

Owner's ls mkdir cat > rm cp cd
permissions A. Read B. Create C. Create file D. Remove E. Copy F. Enter into
contents sub-directory contents contents directory

from

--- N N N N/A N/A N
--x
-w-
-wx
r--
r-x

rw-
rwx

Note: Since you need to try at least 56 commands, to save the time, you can press upper arrow or down
arrow to repeat previous or next command.
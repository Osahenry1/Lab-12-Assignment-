Open your terminal and connect to snowball. Change your directory to your home
directory (cd ~ ), and then create a new directory named as “Lab2_P2” (mkdir
Lab2_P2). After that, go to directory Lab2_P2 (cd Lab2_P2) and download a test
file by the following command (internet access required):
cp /home/frondel1/public/RealEstate.csv .
Be sure it succeeds using “ls” to see the file name “RealEstate.csv” listed.
Then please write the commands you will issue to complete the following tasks
step by step. (You cannot use cd to change the working directory during the steps
except step (9). Each task requires only one command)
(1) You may be curious about what information is stored in this file. So please use
cat to display the content in "RealEstate.csv " using a relative pathname.
(2) We know that cat is good for showing the content of a small file. But since the
file contains many lines, maybe you still cannot find out what information this files
stores after step (1). So please use head to list the first three lines in
"RealEstate.csv ".
(3) Use wc to check the number of homes sold out in "RealEstate.csv ".
(4) Finish the task in step (3) by using the cat command.

(5) Use mkdir to create a new directory "public" under your own home directory
using relative pathname.
(6) Copy "RealEstate.csv" into your "public" directory and name it as
"myRealEstate.csv".
(7) Display the absolute pathname for current working directory.
(8) Check the existence of "myRealEstate.csv" using ls with an absolute pathname.
(9) Go into your "public" directory using relative pathname.
(10) Use mkdir to create a file structure as below in your "Public" directory using
relative pathnames.

Public

Regular Submission
Lab2 Lab3

(11) Rename the directory "Regular" as "Others".
(12) Use cp to copy directory "Lab2_P2" from your home directory to "Lab2"
using relative pathname.
(13) Remove the directory "Lab2_P2" which locates at your home directory.
(14) Use history to list the commands you previously typed.
(15) Store the last 50 commands you typed neatly into a file "Lab2_2.txt", one
command per line and submit it in Google Classroom.
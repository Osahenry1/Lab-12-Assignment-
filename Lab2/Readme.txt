(1) Check the manual page cat by typing the command below and press "Enter".
man cat
(2) The terminal only displays one window of the manual page. You can scan
through the whole manual page by press "f" or SPACE to forward one
window, and "b" to backward one window. Or you can press "h" to find out
more commands to scan through the manual page.
(3) Check the description for option -n. You may find the description as below:

(4) Check the description for option -s. You may find the description as below:

(5) Quit the manual page by press "q"
Part B: Unix basic commands on managing the files and directories.
(1) Make sure that you are connected to snowball successfully. Then go to your
home directory by typing the following command, followed by pressing "Enter".
cd ~

(2) Display current working directory:
pwd
- Question A): What is the working directory? Please write down the full path
(3) List the content in current working directory:
ls
(4) Create a new folder "csc3320" in your home directory:
mkdir csc3320

(5) Repeat step (3).
- Question B): What is the difference in the output compared to the output from
step (3) ? Describe what the difference is.
(6) Navigate to "csc3320":
cd csc3320
(7) Display current working directory.
- Question C): Which command should be typed?
(8) Create a new folder called "lab2" in csc3320.
- Question D): Which command should be typed?
(9) Go to the newly created "lab2" folder.
- Question E): Which command should be typed?

(10) Create a new file called "myLab2.txt" and put your own name in this file by
typing the command below:
cat > myLab2.txt <Enter>
My name is FirstName LastName <Enter>
<Ctrl-D>
Note : <Enter> means press the Enter key; <Ctrl-D> means hold Ctrl and press D
- Question F): There is a special character ">" between "cat" and "myLab1.txt".
What does this character do? And why we need to press "Ctrl-D" at the end of
input?
(11) Display the content in "myLab2.txt" with line numbers by typing the
command below and press "Enter".
cat -n myLab2.txt
- Question G): Attach a screenshot of the output.
(13) Go to your home directory using the absolute path by typing the command
below and press "Enter".
cd <Answer from step(2)>
Note : Please replace the blue part with the answer from step (2)
- Question H): Then issue the command pwd again. Attach a screenshot of the
output.
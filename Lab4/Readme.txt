Open your terminal and connect to snowball server. Change your directory to your
home directory (cd ~ ), and then create a new directory named as “Lab4” (mkdir
Lab4). After that, go to directory Lab4 (cd Lab4) and please download the file
"CSC_Course.txt" by the following command (internet access required):
cp /home/frondel/Public/CSC_Course.txt CSC_Course.txt
Be sure it succeeds using “ls” to see the file name “CSC_Course.txt” listed.
Try the following commands step by step and finish the required tasks from step 4)
to step 16).
Note: marks a single space.
1) $more CSC_Course.txt
Check the content of "CSC_Course.txt" using more.
Note: When viewing the file, you may need to use command f (forward one
screen), b (backward one screen) and q(quit).
2) $grep 'CSC 3320' CSC_Course.txt
Note: there is a single space between "CSC" and "3320"
Output the lines containing the string "CSC 3320"(search the course the
number of which is "CSC 3320")
3) $grep -i 'CSC 3320' CSC_Course.txt
Output the lines containing the string "CSC 3320" via ignoring case (search the
information related to CSC3320)
4) $ grep 'CSC 3' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.

1

5) $ grep 'CSC 3|CSC 1' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
6) $ grep -E 'CSC 3|CSC 1' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
Use extend regular expression
7) $ egrep 'CSC 3|CSC 1' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.

8) $ fgrep '3.000 Credit hours' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
9) $ fgrep -x '3.000 Credit hours' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
Only match the whole line
10) $ grep 'CSC.*Programming' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
11) $ grep '^CSC.*Programming$' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
12) $ grep --color 'CSC[^3]*3{2}' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
No result, {} is not a special character
13) $ egrep --color -w 'CSC[^3]*3{2}[^3]*' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
-w Select only those lines containing matches that form whole words.
14) $ grep 'CSC.*C++' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
+ is not a special character in basic regular expression
15) $ egrep 'CSC.*C\+\+' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
Convert +
16) $ egrep 'CSC.*C++' CSC_Course.txt
Please only describe what this command does.

2

Optional Part:
1) $ sed -E -n 's/(CSC 3[0-9]{3})(.*)/\1/p' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
2) $ awk -F'-' '/(CSC 3[0-9]{3})(.*)/{print $1}' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
3) $ sed -E -n 's/(CSC [0-9]{4})( - )(.*)/\3/p' CSC_Course.txt
Attach a screenshot of the output and describe what this command does.
4) $ sed -E -n 's/(CSC [0-9]{4})( - )(.*)/\3/p' CSC_Course.txt|
sort
Attach a screenshot of the output and describe what this command does.
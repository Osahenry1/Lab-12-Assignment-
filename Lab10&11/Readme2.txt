Write a function about string copy, the strcpy prototype "char* strcpy (char* strDest, const
char* strSrc);". Here strDest is destination string, strSrc is source string.
1) Write the function strcpy, don't call C string library.
2) Here strcpy can copy strSrc to strDest, but why we use char* as the return value of strcpy?

Part 2:
Write a program findStr.c that finds the "smallest" and "largest" in a series of words. After the
user enters the words, the program will determine which words would come first and last if the
words were listed in dictionary order. The program must stop accepting input when the user enters
a four-letter word. Assume that no word is more than 20 letters long. An interactive session with
the program might look like this:
Enter word: dog
Enter word: zebra
Enter word: rabbit
Enter word: catfish
Enter word: walrus
Enter word: cat
Enter word: fish
Smallest word: cat
Largest word: zebra
Hint: Use two strings named smallest_word and largest_word to keep track of the "smallest" and
"largest" words entered so far. Each time the user enters a new word, use strcmp to compare it with
smallest_word; if the new word is "smaller", use strcpy to save it in smallest_word. Do a similar
comparison with largest_word. Use strlen to determine when the user has entered a four-letter
word.
Questions:
1) Attach the source code of your C program into the answer sheet.
2) Run the C program, attach a screenshot of the output in the answer sheet.
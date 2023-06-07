**Lab Report 5**
For this lab, I will be going over an exploration of the command `find` similar to lab report 3. 

**Command-line Options for find**
---
**1. find -r**

**1. find -name**
`find -name <pattern>`: Searches for files and directories with a specific name or pattern. For example, find -name "*.txt" will find all files ending with ".txt" in the specified directory.**

For example, here I typed in `grep -r "truth"`. I expect it to search for the word "truth" recursively in the current directory.

Here I typed in `find -name "*.txt"` in the technical directory, so it should print out all the files ending in .txt

We can see here that it printed out a bunch of files with the .txt in the end. There are more files that it printed out but there were too many to be captured in the screenshot.

**2. grep -c**

`grep -c` is used to count the number of times a specific pattern appears in a file.

For example, here I typed in `grep -c "policy" plos/pmed.0020246.txt`. I expect it to print out the number of times "policy" appeared in the file plos/pmed.0020246.txt.

![Image](Screenshot 2023-05-08 175053.png)

The output is 3, which is what I expected because 3 represents the number of times the word "policy" appeared in the file.

Here I will show another example of using `grep -c` by putting in `grep -c "hummingbirds" plos/journal.pbio.0020350.txt`. I expect it to show me the number of times "hummingbirds" show up in the  file plos/journal.pbio.0020350.txt. I expect the answer to be 4 because from using `grep -r` I discovered that there are 4 lines in the file containing "hummingbirds".

![Image](Screenshot 2023-05-08 175510.png)

We can see that indeed the prediction is right. It printed out 4 because the word "hummingbirds" showed up 4 times in the file.

**3. grep-v**

`grep -v` is used to search for lines that do not contain the pattern in the single file.

For example, I typed in `grep -v "of" plos/pmed.0010023.txt`. I expect the output to print all the lines in the file that does not contain the string "of".

![Image](Screenshot 2023-05-08 182057.png)

This matches up with the prediction, we can see that the output contains the lines in the file plos/pmed.0010023.txt and none of these lines contain the string "of".

Another example of using `grep -v` is shown by putting in `grep -v "the" plos/journal.pbio.0020001.txt`. I expect it to print all the lines in the file that does not contain "the".

![Image](Screenshot 2023-05-08 182714.png)

It successfully printed out all the lines in the file plos/journal.pbio.0020001.txt and we can see that none of the lines printed out contains "the".


**4. grep -o**

`grep -o` is used to print only the matched parts of a matching line. If a pattern is put in and the file contains the patter, then it would only print out the specific pattern for however many lines that contain the pattern. 

For example, here I put in `grep -o "government" plos/pmed.0020246.txt`. I expect it to print out "government" for the number of lines that contain "government"/

![Image](Screenshot 2023-05-08 180828.png)

We can see that only the word "government" is printed, and it is printed 7 times because there are 7 lines that contain "government".


I will show another example of this by going back to our hummingbirds example. Here I put in `grep -o "hummingbirds" plos/journal.pbio.0020350.txt`. I expect it to print "hummingbirds" 4 times because we learned from the previous commands that there are 4 lines in the file that contain the word "hummingbirds".

![Image](Screenshot 2023-05-08 181442.png)

This matches up with our expectation. It printed out only the word "hummingbird" 4 times because "hummingbirds" appeared in 4 lines of the file.



That is it for our lab about some of the command-line options for `grep`. I hope you learned some more about `grep` from this tutorial!

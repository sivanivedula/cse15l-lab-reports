# **Lab Report 3: Researching Commands**
*The following report will provide examples for using the grep command.*

## grep "word" file.txt

* This version of grep finds the string given in the specified file and returns all lines where the string is present.
```
[cs15lsp23dk@ieng6-203]:Media:269$ grep "process" water_fees.txt
under Proposition 218, a process Tulare County Water Works
```
* In this example, I used grep to find the word "process" in the water_fees.txt file, and it returned the line "under Proposition 218, a process Tulare County Water Works" in which the word "process" is included.

```
[cs15lsp23dk@ieng6-203]:About_LSC:277$ grep "resulted" Progress_report.txt
streamlined. Some modifications resulted in more comprehensive
client issues have resulted in the expansion of services to
courts are now developing the goals and strategies that resulted
```
* In this example, I used grep to find the word "resulted" in the Progress_report.txt file, and it returned the 3 different lines "streamlined. Some modifications resulted in more comprehensive", "client issues have resulted in the expansion of services to", "courts are now developing the goals and strategies that resulted"
* My source for this command is chatGPT, and the input and output are pasted below. From the output from ChatGPT, I used the first example point as an idea for a grep command.

input:
> what are some common ways to use grep

output:
> Certainly! Here are some common and practical ways to use the grep command: 
> * Searching for a word in a file: Use grep to search for a specific word or pattern in a file. For example, grep "example" file.txt will search for the word "example" in the file named file.txt.
> * Searching for a word in multiple files: You can search for a word in multiple files using grep. For example, grep "example" file1.txt file2.txt file3.txt will search for the word "example" in the specified files.
Case-insensitive search: By default, grep performs a case-sensitive search. However, you can use the -i option to perform a case-insensitive search. For example, grep -i "example" file.txt will search for the word "example" case-insensitively in the file file.txt.
> * Searching recursively in directories: Use grep with the -r or -R option to search for a word recursively in directories and their subdirectories. For example, grep -r "example" /path/to/directory will search for the word "example" in all files within the specified directory and its subdirectories.
> * Displaying line numbers: Use the -n option to display line numbers along with the matched lines. For example, grep -n "example" file.txt will display lines containing the word "example" along with their line numbers in the file file.txt.
Inverting the match: Use the -v option to invert the match and display lines that do not contain the specified word or pattern. For example, grep -v "example" file.txt will display lines that do not contain the word "example" in the file file.txt.
> * Searching for whole words: Use the -w option to search for whole words instead of partial matches. For example, grep -w "example" file.txt will search for the whole word "example" in the file file.txt, excluding partial matches like "exampled" or "example123".
> * Using regular expressions: grep supports regular expressions for advanced pattern matching. You can use the -E option to enable extended regular expressions. For example, grep -E "ex[a-z]+le" file.txt will search for words that start with "ex," followed by one or more lowercase letters, and end with "le" in the file file.txt.
> * These are some common ways to use grep for searching and pattern matching. Remember to consult the grep manual or command-line help (man grep or grep --help) for more options and detailed information on using grep.

## grep -c "word" file.txt

* The -c stands for count, and this grep -c will find the number of times the "word" appears in the file.txt and return a count of how many times it appears. My source for this command is chatGPT.
```
[cs15lsp23dk@ieng6-203]:Media:289$ grep -c "process" water_fees.txt
1
```

* In this example, we are in the same water_fees.txt file as before, and we would expect the count returned to be "3" since there were 3 lines printed from the original grep command. The number returned matches the expectation.

```
[cs15lsp23dk@ieng6-203]:About_LSC:294$ grep -c "resulted" Progress_report.txt
3
```

* In this example, we are in the same Progress_report.txt file as before, and we would expect the count returned to be "3", since there were 3 lines printed from the original grep command. The number returned matches the expectation.
* My source for this command is chatGPT, and the input and output are pasted below. From the output from ChatGPT, I used the seventh example point as an idea for a grep command.

input:
> fun ways to use grep command

output:
> Sure! Here are some fun ways to use the grep command:
> * Search for a word in a file: Use grep to search for a word in a file. For example, grep "hello" file.txt will search for the word "hello" in the file named file.txt.
> * Search for a word in multiple files: You can search for a word in multiple files using grep. For example, grep "hello" x.txt will search for the word "hello" in all the files with .txt extension in the current directory.
> * Search for a word in a directory: You can search for a word in all the files in a directory and its subdirectories using grep. For example, grep -r "hello" /path/to/directory will search for the word "hello" in all the files in the directory /path/to/directory and its subdirectories.
> * Search for a word in a compressed file: Use grep to search for a word in a compressed file. For example, zgrep "hello" file.txt.gz will search for the word "hello" in the compressed file named file.txt.gz.
> * Search for a word with a regular expression: Use grep to search for a word using a regular expression. For example, grep -E "he.l." file.txt will search for words that start with "he", followed by any character, then "l", and then any character.
> * Show only the matching word: Use grep to show only the matching word. For example, grep -o "hello" file.txt will only show the word "hello" if it appears in the file file.txt.
> * Count the number of matches: Use grep to count the number of matches. For example, grep -c "hello" file.txt will count the number of times the word "hello" appears in the file file.txt.
> * Highlight the matches: Use grep to highlight the matches in the output. For example, grep --color "hello" file.txt will highlight the word "hello" in the output.

## grep -r "hello" /path/to/directory

* The -r means recurisvely and lets us search within directories, and this commands lets us search for a word within a set of files within a whole directory.

```
[cs15lsp23dk@ieng6-203]:government:305$ grep -r "latent" /home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/government
/home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/government/Media/Using_Tech_Tools.txt:clients "the latent market." Small firms and solos are ideal for
```
* In this example, I used grep -r to find the word "latent" in the complete government directory, and it returned a single line "clients "the latent market." Small firms and solos are ideal for" in which the word "latent" is included.

```
[cs15lsp23dk@ieng6-203]:technical:321$ grep -r "forkhead" /home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical
/home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/biomed/1471-2156-2-18.txt:          forkhead box genes 
/home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/biomed/1471-2199-2-12.txt:        by the forkhead family of transcription factors that appear
/home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/biomed/1471-2407-2-15.txt:        inactivation of the forkhead family of transcription
/home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/biomed/1471-2407-2-15.txt:        stimulating kinase; FKHR: forkhead related protein; cFLIP:
/home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/plos/pmed.0020161.txt:        forkhead box D1 (14.8-fold increase, 
/home/linux/ieng6/cs15lsp23/cs15lsp23dk/stringsearch/stringsearch-data/technical/plos/pmed.0020161.txt:          (Hs.408182 [http://www.ncbi.nlm.nih.gov/UniGene/clust.cgi?ORG=Hs&CID=408182; forkhead
```
* In this example, I used grep -r to find the word "forkead" in the complete technical directory, and it returned a few lines as shown above in which the word "forkhead" is included.
* My source for this command is chatGPT, and the input and output are pasted below. From the output from ChatGPT, I used the fourth example point as an idea for a grep command.

input:
> what are some common ways to use grep

output:
> Certainly! Here are some common and practical ways to use the grep command: 
> * Searching for a word in a file: Use grep to search for a specific word or pattern in a file. For example, grep "example" file.txt will search for the word "example" in the file named file.txt.
> * Searching for a word in multiple files: You can search for a word in multiple files using grep. For example, grep "example" file1.txt file2.txt file3.txt will search for the word "example" in the specified files.
Case-insensitive search: By default, grep performs a case-sensitive search. However, you can use the -i option to perform a case-insensitive search. For example, grep -i "example" file.txt will search for the word "example" case-insensitively in the file file.txt.
> * Searching recursively in directories: Use grep with the -r or -R option to search for a word recursively in directories and their subdirectories. For example, grep -r "example" /path/to/directory will search for the word "example" in all files within the specified directory and its subdirectories.
> * Displaying line numbers: Use the -n option to display line numbers along with the matched lines. For example, grep -n "example" file.txt will display lines containing the word "example" along with their line numbers in the file file.txt.
Inverting the match: Use the -v option to invert the match and display lines that do not contain the specified word or pattern. For example, grep -v "example" file.txt will display lines that do not contain the word "example" in the file file.txt.
> * Searching for whole words: Use the -w option to search for whole words instead of partial matches. For example, grep -w "example" file.txt will search for the whole word "example" in the file file.txt, excluding partial matches like "exampled" or "example123".
> * Using regular expressions: grep supports regular expressions for advanced pattern matching. You can use the -E option to enable extended regular expressions. For example, grep -E "ex[a-z]+le" file.txt will search for words that start with "ex," followed by one or more lowercase letters, and end with "le" in the file file.txt.
> * These are some common ways to use grep for searching and pattern matching. Remember to consult the grep manual or command-line help (man grep or grep --help) for more options and detailed information on using grep.


## grep -n "hello" *.txt

* This version of grep finds the string given in the specified text file and returns all lines where the string is present. The -n flag adds the line numbers along with the lines returned.

```
[cs15lsp23dk@ieng6-203]:Media:332$ grep -n "process" water_fees.txt
33:under Proposition 218, a process Tulare County Water Works
```

* In this example, I used grep to find the word "process" in the water_fees.txt file, and it returned the line "under Proposition 218, a process Tulare County Water Works" in which the word "process" is included. It also shows that this line is line 33 in the text file.

```
[cs15lsp23dk@ieng6-203]:About_LSC:337$ grep -n "resulted" Progress_report.txt
809:streamlined. Some modifications resulted in more comprehensive
961:client issues have resulted in the expansion of services to
1093:courts are now developing the goals and strategies that resulted
```
* In this example, I used grep to find the word "resulted" in the Progress_report.txt file, and it returned 3 lines in which the word "process" is included. It also shows that these lines are line 809, 961, and 1093 in the text file.
* My source for this command is chatGPT, and the input and output are pasted below. From the output from ChatGPT, I used the fifth example point as an idea for a grep command.

input:
> what are some common ways to use grep

output:
> Certainly! Here are some common and practical ways to use the grep command: 
> * Searching for a word in a file: Use grep to search for a specific word or pattern in a file. For example, grep "example" file.txt will search for the word "example" in the file named file.txt.
> * Searching for a word in multiple files: You can search for a word in multiple files using grep. For example, grep "example" file1.txt file2.txt file3.txt will search for the word "example" in the specified files.
Case-insensitive search: By default, grep performs a case-sensitive search. However, you can use the -i option to perform a case-insensitive search. For example, grep -i "example" file.txt will search for the word "example" case-insensitively in the file file.txt.
> * Searching recursively in directories: Use grep with the -r or -R option to search for a word recursively in directories and their subdirectories. For example, grep -r "example" /path/to/directory will search for the word "example" in all files within the specified directory and its subdirectories.
> * Displaying line numbers: Use the -n option to display line numbers along with the matched lines. For example, grep -n "example" file.txt will display lines containing the word "example" along with their line numbers in the file file.txt.
Inverting the match: Use the -v option to invert the match and display lines that do not contain the specified word or pattern. For example, grep -v "example" file.txt will display lines that do not contain the word "example" in the file file.txt.
> * Searching for whole words: Use the -w option to search for whole words instead of partial matches. For example, grep -w "example" file.txt will search for the whole word "example" in the file file.txt, excluding partial matches like "exampled" or "example123".
> * Using regular expressions: grep supports regular expressions for advanced pattern matching. You can use the -E option to enable extended regular expressions. For example, grep -E "ex[a-z]+le" file.txt will search for words that start with "ex," followed by one or more lowercase letters, and end with "le" in the file file.txt.
> * These are some common ways to use grep for searching and pattern matching. Remember to consult the grep manual or command-line help (man grep or grep --help) for more options and detailed information on using grep.



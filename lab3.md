# **Lab Report 3: Researching Commands**
*The following report will provide instructions to log into a course-specific account.*

## grep "word" file.txt

* This version of grep finds the string given in the specified file and returns all lines where the string is present. My source for this command is chatGPT.
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

## grep -r "hello" /path/to/directory

* The -r means recurisvely and lets us search within directories, and this commands lets us search for a word within a set of files within a whole directory. My source for this command is chatGPT.

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

## grep -n "hello" *.txt

* This version of grep finds the string given in the specified text file and returns all lines where the string is present. The -n flag adds the line numbers along with the lines returned. My source for this command is chatGPT.

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


# **Lab Report 3: Researching Commands**
*The following report will provide instructions to log into a course-specific account.*

## grep "hello" file.txt

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


## grep -c "hello" file.txt

## grep -r "hello" /path/to/directory

## grep "hello" *.txt

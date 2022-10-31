## What is grep?

Grep < string > < files > searches for patterns in each file. Grep prints matching lines. 

---
### Command-Line examples

*You can use grep as a filter for other commands. The first half displays files ending in .ps. The second half looks through the list of grep with the pattern Sep. Meaning, files created in the month of September.*
```
$ ls -l *.ps | grep "Sep"
```
#### Result
```
-rw-r--r--   1 user2    users      39245 Sep 27 09:38 changes.ps
-rw-r--r--   1 user2    users     827114 Sep 13 16:49 commands.ps
```

*Searches for all lines in current directory that **DON'T** contain a certain string.*
```
$ grep -L "milk" *
```

*Searches for string in group of files. When pattern matches, it prints the name of the file followed by a colon then the line*
```
$ grep ar *
```
#### Result
```
actors: Humphrey Bogart 
alaska:Alaska is the largest state in the United States.
wilde:book.  Books are well written or badly written.
```
---
### Command-Line In-Class Examples

```
find some-files/ | grep ".java" | xargs wc
```
#### Result
```
2   2   11  some-files//even-more-files/d.java
1   1   7   some-files//more-files/c.java
3   3   18  total
```
*Searches for any files that doesn't contain "c" in the current directory.*
```
find some-files/ | grep -L "c" *
```
*Searches for string in all of some-files for ar, then prints the name of the file*
```
find some-files/ | grep ar *
```


---
#### Sources:

[Week 5 Worksheets](https://ucsd-cse15l-f22.github.io/week/week5/)

[Docs Oracle](https://docs.oracle.com/cd/E19253-01/806-7612/filesearch-99633/index.html)

[Linux Manual Page](https://man7.org/linux/man-pages/man1/grep.1.html)
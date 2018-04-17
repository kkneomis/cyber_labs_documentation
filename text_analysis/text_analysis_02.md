# Text Analysis (continued)

### Text searching using grep

Grep allows you to search a file (or a set of files) for a given pattern. It returns the lines in the file that match the pattern.

At a basic level, we can use grep to search for a word inside a file.

__Usage:__ ```grep [searchterm] [filepath]```

Given the following file:

```console
user$ cat file.txt 
hello world, this is
the sample text that
I want to get
information
about using the wc command
```

Here's how we can search for all the lines containing the word "world."

```console
user$ grep "the" file.txt 
the sample text that
about using the wc command
```
### Searching for multiple terms (or)

If we want to search for a series of terms and match all lines with any of the terms, we can use the ```-e``` flag. This expression works similar to an "or" expression with the search terms.

__Usage__: ```grep -e [searchterm] -e [searchterm] ... [filepath]```

```console
user$ grep -e "world" -e "wc" file.txt 
hello world, this is
about using the wc command
```
### Searching for multiple terms (and)
If, instead, we wanted to search for the presence for two words in a line, we can simply grep for one term and grep the results for our second term.

```console
user$ cat file.txt  | grep about | grep command
about using the wc command
```
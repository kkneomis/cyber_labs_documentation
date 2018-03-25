# Text Analysis

### Reading a file

Use the ```cat``` command to ouput the content of your file to the console.

__Usage:__ ```cat [filepath]```

```console
user:~/topsecret/files$ cat file.txt 
hello world
```

Alternatively, we can use less to view the contents of the file one page at a time rather than dumping it all on the screen. Less allows us to scroll through the contents of the file and even search for keywords. This is useful for larger files.

__Usage:__ ```less [filepath```  or ```cat [filepath] | less```

### Count lines and words in a file

Use the ```wc``` command to get basic statistics on your file content. 

```wc -l``` will count the number of lines in your file.

```wc -m``` will count the number of words in your file. 

```console
user:~/topsecret/files$ cat file.txt 
hello world, this is
some sample text that
I want to get 
information
about using the wc command
user:~/topsecret/files$ wc -l file.txt 
       5 file.txt
user:~/topsecret/files$ wc -w file.txt 
      18 file.txt
```

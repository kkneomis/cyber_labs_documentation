# Linux command line basics (continued)

### cp 

The copy (cp) command allows us to duplicate a file. 

Usage: ```cp [o filename] [duplicate name]```

```console
user:~/topsecret/files$ ll
total 16
-rw-r--r--  1 simeonkakpovi  staff    18B 24 Mar 15:44 file2.txt
-rw-r--r--  1 simeonkakpovi  staff    10B 24 Mar 15:44 file1.txt
-rw-r--r--  1 simeonkakpovi  staff     0B 24 Mar 15:32 file3.txt

user:~/topsecret/files$ cp file2.txt file2copy.txt

user:~/topsecret/files$ ll
total 24
-rw-r--r--  1 simeonkakpovi  staff    18B 24 Mar 15:44 file2.txt
-rw-r--r--  1 simeonkakpovi  staff    18B 24 Mar 15:54 file2copy.txt
-rw-r--r--  1 simeonkakpovi  staff    10B 24 Mar 15:44 file1.txt
-rw-r--r--  1 simeonkakpovi  staff     0B 24 Mar 15:32 file3.txt
```

### mv

The move (mv) command allows us to move a file from one location to another.

Usage: ```mv [filename] [location]```

Here we move file1.txt to the parent directory.

```console
user:~/topsecret/files$ ls
file1.txt     file2.txt     file2copy.txt file3.txt
user:~/topsecret/files$ mv file1.txt ../
user:~/topsecret/files$ cd ..
user:~/topsecret$ ls
docs      file1.txt files     gifs      memes     pics
```

The mv command can also be used to change the name of file.
Usage: ```mv [filename] [newname]```

```console
user:~/topsecret/files$ ls
file1.txt file2.txt file3.txt
user:~/topsecret/files$ mv file1.txt newname.txt
user:~/topsecret/files$ ls
file2.txt   file3.txt   newname.txt
```

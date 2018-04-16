# Linux command line basics (continued)

### File Creation

The easiest was to create a file is using the ```touch``` command

Usage: ```touch filename```

```console
user:~/topsecret/files$ ls
user:~/topsecret/files$ touch file.txt
user:~/topsecret/files$ ls
file.txt
```

Alternatively, we can write text to a new file

Usage: ```echo "sometext" > newfile.txt```

```console
user:~/topsecret/files$ ls
user:~/topsecret/files$ echo "hello world" > file.txt
user:~/topsecret/files$ cat file.txt 
hello world
```

Using ```>``` writes the input to our file. However, it overwrite any content that is already inside the file. If we can to instead add to the content already in the file, we use ```>>```.

Usage:

```echo "data" > overwrite.txt```

```echo "data" >> append.txt```

```console
user:~/topsecret/files$ echo "goodbye" >> file.txt 
user:~/topsecret/files$ cat file.txt 
hello world
goodbye
user:~/topsecret/files$ echo "goodbye" > file.txt 
user:~/topsecret/files$ cat file.txt 
goodbye
```
__Delete a file:__

We use the remove (rm command)

```console
user:~/topsecret/files$ ls
file.txt
user:~/topsecret/files$ rm file.txt 
user:~/topsecret/files$ ls
```

### Folder Creation

Use the make direcotry (```mkdir```) command.

Here we create folder called "subfolder" and change our directory into it.

Usage: ```mkdir folder_name```

```console
user:~/topsecret/files$ ls
user:~/topsecret/files$ mkdir subfolder
user:~/topsecret/files$ ls
subfolder
user:~/topsecret/files$ cd subfolder/
user:~/topsecret/files/subfolder$
```

We can delete this folder using the "rmdir" command.

Usage: ```rmdir folder_path```

```console
user:~/topsecret/files$ ls
subfolder
user:~/topsecret/files$ rmdir subfolder/
user:~/topsecret/files$ lsuser
```
If there are files inside the directory, you would need to recursively delete the folder and everything inside it.

Usage: ```rm -r foldername__```

or ```__rm -rf foldername__``` (I would be very careful with this)

```console
user:~/topsecret/files$ ls
subfolder
user:~/topsecret/files$ ls subfolder/
file1.txt file2.txt
user:~/topsecret/files$ rm -rf subfolder/
user:~/topsecret/files$ ls
user:~/topsecret/files$
```
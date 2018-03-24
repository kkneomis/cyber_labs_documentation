# Linux command line basics (continued)

### File Creation

The easiest was to create a file is using the ```touch``` command

__touch filename__

```console
user:~/topsecret/files$ ls
user:~/topsecret/files$ touch file.txt
user:~/topsecret/files$ ls
file.txt
```

Alternatively, we can write text to a new file

__echo "data" > newfile.txt__

```console
user:~/topsecret/files$ ls
user:~/topsecret/files$ echo "hello world" > file.txt
user:~/topsecret/files$ cat file.txt 
hello world
```

Using ```>``` overwrites the file with our input. If we can to add to the file, we use ```>>```.

__echo "data" > overwrite.txt__

__echo "data" >> append.txt__

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

__mkdir folder_name__

```consoleuser
user:~/topsecret/files$ ls
user:~/topsecret/files$ mkdir subfolder
user:~/topsecret/files$ lsuser
subfolder
user:~/topsecret/files$ cd subfolder/
user:~/topsecret/files/subfolder$
```

We can delete this folder using the "rmdir" command.

__rmdir folder_path__

```console
user:~/topsecret/files$ ls
subfolder
user:~/topsecret/files$ rmdir subfolder/
user:~/topsecret/files$ lsuser
```
If there are files inside the directory, you would need to recursily delete the folder and everything inside it.

__rm -r foldername__

or __rm -rf foldername__ (I would be very careful with this)

```console
user:~/topsecret/files$ ls
subfolder
user:~/topsecret/files$ ls subfolder/
file1.txt file2.txt
user:~/topsecret/files$ rm -rf subfolder/
user:~/topsecret/files$ ls
user:~/topsecret/files$
```
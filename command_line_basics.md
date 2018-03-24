# Linux command line basics

### Change Directory (cd)

The cd command is used to navigate through directories on the command line. It is the equivalent of clicking into and out of folders in a GUI interface. 

The cd command is simple to use: ```cd [path]```

You can give it either a relative or absolute path.

Suppose we have the following folder structure:

![image1](assets/img1.png)

**Let's navigate into the memes folder**

```console
user:~/topsecret/$ pwd
/Users/user/topsecret

user:~/topsecret$ cd memes/
user:~/topsecret/memes$ 

user:~/topsecret/memes$ pwd
/Users/user/topsecret/memes
```

Here we simply change directories into the memes folder. Notice, in the second line, our path changed. We are now inside that folder.

__Let's navigate into the dank folder__ 

```console
user:~/topsecret$ pwd
/Users/user/topsecret

user:~/topsecret$ cd memes/dank/
user:~/topsecret/memes/dank$ 

user:~/topsecret/memes/dank$ pwd
/Users/user/topsecret/memes/dank
```
or 

```console
user:~/topsecret$ pwd
/Users/user/topsecret

user:~/topsecret$ cd memes/
user:~/topsecret/memes$ cd dank/
user:~/topsecret/memes/dank$

user:~/topsecret/memes/dank$ pwd
/Users/user/topsecret/memes/dank
```

We can either go into the "dank" folder by giving it the full path to that folder, or by navigating twice to the "memes" folder, then to the "dank" folder.

__Cd out of a folder__

If we want to change directories into the parent folder, we use "..".

- Up one folder: 	```cd ..```
- Up two folders: 	```cd ../../```
- Up three folder: 	```cd ../../../```
- etc...

```{r, engine='bash', count_lines}
simeonkakpovi@Simeons-MBP-2:~/topsecret/memes/dank$ pwd
/Users/simeonkakpovi/topsecret/memes/dank
simeonkakpovi@Simeons-MBP-2:~/topsecret/memes/dank$ cd ../../
simeonkakpovi@Simeons-MBP-2:~/topsecret$ pwd
/Users/simeonkakpovi/topsecret
```


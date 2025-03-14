## Copying files

Copying files with the [cp][] (copy) command is very similar to moving them. Remember to always specify a source and a target location. Let's create a new file and make a copy of it:

```bash
learning_unix$ touch file1
learning_unix$ cp file1 file2
learning_unix$ ls
file1  file2
```

What if we wanted to copy files from a different directory to our current directory? Let's put a file in our home directory (specified by `~` remember) and copy it to the current directory (`learning_unix`):

```bash
learning_unix$ touch ~/file3
learning_unix$ ls ~
a_directory another_directory file3 learning_unix
learning_unix$ cp ~/file3 .
learning_unix$ ls
file1  file2  file3
```

This last step introduces another new concept. In Unix, the current directory can be represented by a `.` (dot) character. You will mostly use this only for copying files to the current directory that you are in. Compare the following:

```bash
ls
ls .
ls ./
```

In this case, using the dot is somewhat pointless because `ls` will already list the contents of the current directory by default. Also note how the trailing slash is optional. You can use `rm` to remove the temporary files.

Finally, let's clean up this directory. Note the use of the `*` wildcard, which allows us to delete all three files at once.

```bash
learning_unix$ rm file*
```

[cp]: http://en.wikipedia.org/wiki/Cp_(Unix)
    
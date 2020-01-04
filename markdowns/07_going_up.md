Frequently, you will find that you want to go 'upwards' one level in the directory hierarchy. Two dots `..` are used in Unix to refer to the _parent_ directory of wherever you are. Every directory has a parent except the root level of the computer. Let's go into the `learning_unix` directory and then navigate up two levels:

```bash
~$ cd learning_unix/
learning_unix$ cd ..
~$ cd ..
home$
```

What if you wanted to navigate up _two_ levels in the file system in one go? It's very simple, just use two sets of the `..` operator, separated by a forward slash:

```bash
cd ../..
```
    
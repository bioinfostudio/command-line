## The root directory

Let's change directory to the root directory, and then into our home directory

```bash
inner$ cd /
/$ cd home
home$ cd bioinfo
~$
```

In this case, we may as well have just changed directory in one go:
```bash
cd /home/bioinfo/
```

The leading `/` is incredibly important. The following two commands are very different:

```bash
cd /home/bioinfo/
cd home/bioinfo/
```

The first command says go the `bioinfo` directory that is beneath the `home` directory that is at the top level (the root) of the file system. There can only be one `/home/bioinfo` directory on any Unix system.

The second command says go to the `bioinfo` directory that is beneath the `home` directory that is located wherever I am right now. There can potentially be many `home/bioinfo` directories on a Unix system (though this is unlikely).

Learn and understand the difference between these two commands.
    
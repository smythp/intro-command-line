## Navigation

### Your first command

When you're in the command line, you'll see a prompt that looks like this:

```
$
```

You may also see your username to the left of the `$`. Let's try our first command. Type the following and press enter:

```
$ whoami
```

The `whoami` command should print out your username. Congrats, you've executed your first command! This is a basic pattern of use in the command line: type a command and receive output.

### Folders

OK, we're going to try another command. But first, let's make sure we understand some things about how your computer's filesystem works.

Your computer's files are organized in what's known as a hierarchical file system. That means there's a top level or "root" folder on your system. That folder has other folders in it, and those folders have folders in them, and so on. You can draw these relationships in a tree:

```
Users
|
-- patrick
  |
  -- Photos
  -- Documents
```

The root or highest-level folder on OSX is just called `/`. We won't need to go in there, though, since that's mostly just files for the operating system. On Windows, the root directory is usually called `C:`.

OK, let's try a command that tells us where we are in the filesystem:

```
$ pwd
```

You should get output like `/Users/patrick`. That means you're in the `patrick` directory in the `Users` folder inside the `/` or root directory. On Windows, your output would instead be `C:/Users/patrick`. The folder you're in is called the working directory, and `pwd` stands for "print working directory."

OK, we know where we are. But what if we want to know what files and folders are in the `patrick` directory, a.k.a. the working directory? Try entering

```
ls
```

You should see a number of folders, probably including `Documents`, `Desktop`, and so on. You may also see some files. These are the contents of the current working directory. 

I wonder what's in the Desktop folder? Let's try moving to it with the following command:

```
$ cd Desktop
```

(Make sure the "D" in "Desktop" is capitalized. ) If the command was successful, you won't see any output. This is normal—often, the command line will succeed silently. 

So how do we know it worked? That's right, let's use our `pwd` command again. We should get

```
/Users/patrick/Desktop
```



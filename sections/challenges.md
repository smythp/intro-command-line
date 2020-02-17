[<<< Previous](grep.md)  
[<<< Return to introduction](../README.md)

# Further challenges

These challenges are ordered from easiest to hardest. No, it's not cheating if you ask for help.

## Challenge #1: create hidden file

Use the `touch` command to create a hidden file. Hidden files have a `.` in front of them, like this:

```
$ ls -A
.gitignore hello.txt
$ ls
hello.txt
```

You can also create hidden folders this way, but you only need to create a file to pass the challenge. 


## Challenge #2: create an alias

All these commands are great and all, but what if I want to make my own command? For example, maybe I want to make this happen:

```
$ peptalk
Good work
```

To do this, use the `alias` command:

```
$ alias peptalk="echo Good work"
```

To pass this challenge, make your own alias that does something different.

## Challenge #3: make a permanent alias

So you made an alias, but you realized it goes away when you close and reopen the terminal. (So unfair.) Make your alias permanent.

To do this, you will need to edit the configuration file that your terminal runs when it starts up. On Git Bash, that's going to be called `~/.bashrc`. (That's a `.bashrc` file in your home folder.) On OSX, the file is called `~/.bash_profile`. Just add the command you used to create the alias to the file with your text editor. Close and reopen the terminal to make sure your alias still works.

**Note to Windows users:** This could present a challenge, as `.bashrc` may not be created for you by default, and if you create it, Git Bash may not recognize it. [A Stack Overflow question here](https://stackoverflow.com/questions/6883760/git-for-windows-bashrc-or-equivalent-configuration-files-for-git-bash-shell) addresses the potential challenges.

## Challenge #4: create your own shell script 

Due to platform differences, Windows users should skip directly to Challenge #5.

You're having fun with aliases, but are they REAL programs, or just glorified shortcuts?

This challenge is to create a bash script, a REAL program written in bash. To do this, create a text file (I'll call this one `goto-projects.sh`) that begins with this line:

```
#!/bin/bash
```

Under that, write some lines of bash that you want to be executed. How about a program that goes to your projects folder from wherever you are?

```
cd ~/Desktop/projects
echo "Now you're in $PWD"
```

Your script should look like this when you're done.

goto-projects.sh:
```
#!/bin/bash

cd ~/Desktop/projects
echo "Now you're in $PWD"
```

Now run this command to make your script executable. This gives your computer permission to run it as a program:

```
$ chmod a+x goto-projects.sh
```

Now run your program like this:

```
$ ./goto-projects.sh
```

## Challenge #5: make your script run from anywhere

### Mac OS

Last challenge! So you've made a real program in bash, you're probably feeling pretty proud of yourself. Deservedly so. But you still need to be in a folder with your program, and you still need to use that annoying `./` to run it. Let's make our program accessible from anywhere on the system by moving it to the `/bin` folder.

This challenge must be performed differently in Mac OS and in Windows using Git Bash.

```
sudo mv goto-projects.sh /bin/goto-projects
```

This moves your script from its current folder to the `/bin` folder and renames it from `goto-projects.sh` to `goto-projects`. Now close your terminal with `exit` and reopen it. Type 


	$ goto-projects


from anywhere and see if that runs your script. If it does, congratulations! You're a force to be reckoned with on the command line.

### Windows

In this final challenge, we're going to write a real program in bash that can be used like any command on the command line.

Since Git Bash doesn't come with a `sudo` command that allows us to perform actions on folders that require special permissions, we'll need to approach this final challenge a little differently.

First, we'll need to open our text editor, VS Code, with special administrator permissions. Press the Windows button on your keyboard or click the start menu and type `Visual Studio Code` into the search box. Do not click or hit Enter to open VS Code. Instead, right click on the VS Code icon and select the `Run as Administrator` option from the dropdown menu. If you are prompted to allow the program to be run with administrator privileges, select `Yes`.

Once VS Code is open with administrator permissions, write out the following program:

```bash
#!/bin/bash

cd ~/Desktop/projects
echo "Now you're in $(pwd)"
```

The first line of the program is a special line that lets the command line know which program to use to run the script. The other lines are bash (command line) commands that will be run one after the other when our bash script is executed. As you may be able to guess, this script will first go to our Desktop folder and then print out a message letting us know where we are.

Once our script is written out, save it in the following folder on your system:

	c:\Program Files\Git\usr\bin
	
This is a folder where Git Bash looks to determine which commands are available when it starts up. Enter `goto-projects` as the filename, and VS Code should automatically add a `.sh` extension, indicating that the file is a bash script.

Close and reopen Git Bash. You should now be able to run your new command by typing

	goto-projects.sh
	
at the `$` prompt. If the command isn't appearing, you may want to use Git Bash to navigate to the `/usr/bin` folder and use `ls` to see if the command was saved correctly and what it is called.

[<<< Return to introduction](../README.md)

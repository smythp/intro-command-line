[<<< Previous](summary.md)  
[<<< Return to introduction](README.md)

## Glossary

### Synonyms for the command line

*bash* - the programming language used in the command line. (Yes, we tricked you, you're already programming!) Short for "Born Again SHell," for reasons people on the internet will happily tell you about.

*the terminal* - Particularly used to refer to the command line on OSX. This term made more sense when universities used mainframes and every computer was only a terminal.

*the shell* - The part of an operating system that interacts with a human. Technically, anything you do in a graphical interface is also in a shell, but in practice this is just another synonym for the command line.

*cli* - "Command Language Interpreter," this is a super technical term for the command line used to impress everyone around you.

### Other terms

*argument* - in the command line, an argument is an item or parameter that you give a program when you start it. For instance, if you 

*command* - a specific task or function given to a computer application (Terminal or Bash in this tutorial) to perform some kind of task or function. At first it may seem like aribtrary letters are pulled out of thin air to enact some sort of magic. In fact, these commands (`mkdir`, `ls`, etc.) have been written by people to fulfill express functions. Options (see below) were developed for specific commands based on the commands' functions. Most users only need a small set of the commands that come pre-installed in their command line interface to complete their desired tasks.

*flag* - otherwise known as an *option* or *switch*, a flag provides additional information for how you wish a program to run. For instance, when executing the command `grep`, you may want to add the flag `-i` to ignore capitalization. If you wish to know what flags belond to particular commands, you can check the m

*GUI* - "Graphical User Interface." Pronounced "gooey," like delicious gooey chocolate. Basically, anything on a computer that isn't in the command line. All familiar elements of day-to-day computer tasks such as images, windows, prompts, buttons, and progress bars are part of the GUI. The way most people interact with computers. Some tasks can only be done in a GUI, while others can only be done in the command line.

*option* - see *flag*

*prompt* - the `$` is known as the "prompt." It indicats that your command line is ready to receive commands.

*pipeline* - in the command line, a pipeline is a sequence of processes. The output of one command feeds directly as input into the next command.

*root* - A word for the administrative user on a system. You often need administrative privileges to install programs or access certain system folders using the command line. You can tell you're root when your `$` prompt turns into a `#` prompt. To become root, type `su` and enter the password you use to log in. (No characters or asterisks will appear, just type your password and press enter.) You can also run a single command as root by typing `sudo` before the command.

*syntax* - with computers, the syntax refers to the rules by which a command must be run so that the software can understand it. Some commands *need* an argument to follow the command. For example `mv` will only work if you provide the source file that you intend to move and the directory destination. 

*UNIX* - A family of operating systems that have a multi-user model and a particular design philosophy. Both OSX and Linux are UNIXes. Windows is not.

*REPL* - "Read Eval Print Loop" The process of typing something in to the command line and getting something back out. Like most things to do with the command line, not as complicated (or scary) as it sounds.

*wildcard* `*` - the wildcard character on the command line will revolutionize your world. When you are giving a command an argument, for instance instead of

````grep filename.txt````

type

````grep *.txt````

The wildcard, `*`, will tell the command to search for any file ending with a .txt extension. But the wildcard can work anywhere in the string! If, for example, you want to move all formats (.doc, .pdf, .jpg) of the same name to a different folder you would type:

````mv [filename.*] [foldername]````



Find so much more on the command line:

[Bash manual](https://www.gnu.org/software/bash/manual/bashref.html) - the no nonsense text descriptions of bash commands.  
[explain shell](https://explainshell.com/) - a site that explains commands you paste into the form. This site is fantastic for breaking down commands you find in the wild on the internet.  
[Easy shell guide](https://lucasviola.github.io/easyshell/) - a friendly, styled (pastel!) list of common commands you might want to try out.

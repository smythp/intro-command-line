## Creating a Cheat Sheet

In this section, we'll create a text file that we can use as a cheat sheet. You can use it to keep track of all the awesome commands you're learning. 

Instead of creating an empty file like we did with `touch`, let's try creating a file with some text in it. Make sure you're in the projects folder and run:

```
echo "This is my cheat sheet" > cheat-sheet.txt
```

Now let's check the contents of the directory:

```
$ pwd
/Users/patrick/projects
$ ls
cheat-sheet.txt
```

OK, so the file has been created. Let's check if there's any text in cheat-sheet.txt.

```
cat cheat-sheet.txt
This is my cheat sheet
```

As you can see, the `cat` command prints the contents of a file to the screen.

### Using a Text Editor

The challenge for this section will be adding some of the commands that we've learned to the newly created cheat sheet. To do this, you'll need a working text editor. These are programs designed specifically for editing text files. Do not use rich document editors like MS Word or Text Edit, as they will either not work or cause problems later. Recommended editors include [TextWrangler](http://www.barebones.com/products/textwrangler/) for OSX, [Notepad++](https://notepad-plus-plus.org/) for OSX and Windows, and Nano for the command line. (Check out the [About text editors](text-editors.md) page for more information.)

# Challenge

Use your text editor of choice to add some of the commands that you've learned to the newly-created cheat-sheet.txt file. If you're confused about which text editor to use, check the [About Text Editors](text-editors.md) page or ask a facilitator for help.

The example below uses Nano, an editor that is built into the terminal in OSX. The commands used are `nano cheat-sheet.txt` to open the file and `Control-x`, `Y`, and `Enter` in succession to save any changes. In Nano, the keys for different commands are always at the bottom of the screen.

[<<< Previous](creating-files-and-folders.md) - [Next >>>]()

### Example

![Creating a Cheat Sheet](cheat-sheet.gif)

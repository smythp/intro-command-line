[<<< Previous](data.md)

### Searching text data

So we've cleaned our data set, but how do we find entries that use a particular term? 

Let's say I want to find all the entries in our data set that use the term "Paris."

Here we can use the `grep` command. `grep` stands for "global regular expression print" and it processes text line by line and prints any lines which match a specified pattern. Regular expressions are infamously human-illegible commands that use character by character matching to return a pattern. `grep` gives us access to the power of regular expressions as we search for text.

```
$ cat nypl_items.csv | grep -i "paris"
[...]
```

This will print out all the lines that contain the word "Paris." (The `-i` flag makes the command ignore capitalization.) Let's use our `wc -l` command to see how many lines that is:

```
$ $ cat nypl_items.csv | grep -i "paris" | wc -l
191
```

### Challenge

Use the `grep` command to explore our .csv file a bit. What areas are best covered by the data set?

If you want to get a little more milage out of the grep command, refer to [this tutorial on grep and regular expressions](https://www.digitalocean.com/community/tutorials/using-grep-regular-expressions-to-search-for-text-patterns-in-linux). Regular expressions provide ways to search for text in more advanced ways, including specific wildcards, matching ranges of characters such as letters and numbers, and detecting features such as the beginning and end of lines.

### Before we finish...

Before you leave today, we're going to prepare a little for our upcoming sessions. In your projects folder on the desktop, we're going to create a folder to house our cheat sheets for the week, as well as a new folder for the upcoming databases workshop.

```
$ pwd
/Users/jojo/Desktop/projects
$ mkdir cheatsheets
$ mkdir databases
```

Then move your `cheat-sheet.txt` file into your `cheatsheets` folder and your `nypl_items.csv` into your `databases` folder with the `mv` command:

```
$ mv cheat-sheet.txt cheatsheets
$ mv nypl_items.csv databases
```

### What next?

That's the end of the command line session, but if you want to continue to learn about the command line, take a look at the [other useful commands](other-commands.md) or [additional challenges](challenges.md).

[<<< Previous](data.md)

[Go to other commands >>>](other-commands.md)  
[Go to further challenges >>>](challenges.md)  

### Example

![Searching a text file with grep](grep.gif)




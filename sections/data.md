[<<< Previous](pipes.md) | [Next >>>](grep.md)

## Exploring text data

So far the only text file we've been working with is our cheat sheet. Now, this is where the command line can be a very powerful tool: let's try working with a large text file, one that would be too large to work with by hand.

Let's download the data we're going to work with:

[Download nypl_items.csv](http://smythp.com/hosted/nypl_items.csv)

Our data set is a list of public domain items from the New York Public Library. It's in .csv format, which is a plain text spreadsheet format. CSV stands for "comma separated values," and each field in the spreadsheet is separated with a comma. It's all still plain text, though, so we can manipulate the data using the command line.

### Move command  

Once the file is downloaded, move it from your `Downloads` folder to the `projects` folder on your desktop--either through the command line, or drag and drop in the GUI. Since this is indeed a command line workshop, you should try the former! 

To move this file using the command line, you first need to navigate to your `Downloads` folder where that file is saved. Then type the `mv` command followed by the name of the file you want to move and then the file path to your `projects` folder on your desktop, which is where you want to move that file to (note that `~` refers to your home folder):
```
mv nypl_items.csv ~/Desktop/projects/  
``` 
You can then navigate to that `projects` folder and use the `ls` command to check that the file is now there.  

### Viewing data in the command line

Try using `cat` to look at the data. You'll find it all goes by too fast to get any sense of it. (You can click `Control` and `C` on your keyboard to cancel the output if it's taking too long.) 

Instead, let's use another tool, the `less` command, to get the data one page at a time:

```
$ less nypl_items.csv
[...]
```

`Less` gives you a paginated view of the data; it will show you contents of a file or the output from a command or string of commands, page by page. 

To view the file contents page by page, you may use the following keyboard shortcuts (that should work on Windows using Git Bash or on Mac): 
Click the `f` key to view forward one page, or the `b` key to view back one page. 

Once you're done, click the `q` key to return to the command line. 

Let's try two more commands for viewing the contents of a file:

```
$ head nypl_items.csv
[...]
$ tail nypl_items.csv
[...]
```

These commands print out the very first (the "head") and very last (the "tail") sections of the file, respectively.

### Interlude for Jojo's favorite command line feature: tab completion.

When you are navigating in the command line, typing folder and file names can seem to go against the promise of easier communication with your computer. Here comes `tab` completion, stage right! 

When you need to type out a file or folder name--for example, the name of that csv file we've been working with: nypl_items.csv--in the command line and want to move more quickly, you can just type out the beginning characters of that file name up until it's distinct in that folder and then click the `tab` key. And voilà! Clicking that `tab` key will complete the rest of that name for you, and it only works if that file or folder already exists within your working directory. 

In other words, anytime in the command line you can type as much of the file or folder name that is unique within that directory, and `tab` complete the rest!  

### Note: Clearing Text

If all the text remaining in your terminal window is starting to overwhelm you, you have some options. You may type the `clear` command into the command line, or click the `command` and `k` keys to clear the scrollback. In Mac OS terminal, clicking the `command` and `l` keys will clear the output from your most recent command.  

### Cleaning the data

We didn't tell you this before, but there are duplicate lines in our data! Two, to be exact. Before we try removing them, let's see how many entries are in our .csv file:

```
$ cat nypl_items.csv | wc -l
100001
```

This tells us there are 100,001 lines in our file. The `wc` tool stands for "word count," but it can also count characters and lines in a file. We tell `wc` to count lines by using the `-l` flag. If we wanted to count characters, we could use `wc -m`. Flags marked with hyphens, such as `-l` or `-m`, indicate options which belong to specific commands. See the [glossary](glossary.md) for more information about flags and options.

To find and remove duplicate lines, we can use the `uniq` command. Let's try it out:

```
$ cat nypl_items.csv | uniq | wc -l
99999
```

OK, the count went down by two because the `uniq` command removed the duplicate lines. But which lines were duplicated?

```
$ cat nypl_items.csv | uniq -d
[...]
```

The `uniq` command with the `-d` flag prints out the lines that have duplicates. 

### Challenge

Use the commands you've learned so far to create a new version of the `nypl_items.csv` file with the duplicated lines removed. (Hint: [redirects](creating_a_cheat_sheet.md#redirect-) are your friend.)

[<<< Previous](pipes.md) | [Next >>>](grep.md)

![exploring data](data.gif)


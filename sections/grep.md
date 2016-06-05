### Searching text data

So we've cleaned our data set, but how do we find entries that use a particular term? 

Say I want to find all the entries in our data set that use the term "Paris."

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

### What next?

That's the end of the command line session, but if you want to continue to learn about the command line, take a look at the [other useful commands](other-commands.md) or [additional challenges](challenges.md).

[<<< Previous](data.md) - [Next >>>](other-commands.md)

### Example

![Searching a text file with grep](grep.gif)




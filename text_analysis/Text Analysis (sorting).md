# Text Analysis (sorting)

### Text parsing using awk

Sometimes it can be useful to get some quick statistics about items in a file. This is an especially useful skill if you want when examining log files. For example, you may want to know how many times a suspicious ip address is present in your proxy logs.

# sort

The ```sort``` command sorts the lines in your files alphanumerically. It's also useful because it groups like values together. 

__Usage:__```cat file.txt | sort ```

```console
user$: cat file.txt
cat
dog
cow
cat
dog
dog
cow
cat
cow
cat
user$: cat file.txt | sort
cat
cat
cat
cat
cow
cow
cow
dog
dog
dog
```

# uniq

The ```uniq``` command merges (deduplicates) all adjacent lines of the same value. To count the number of uniq values, we can add a ```-c``` flag to the command.
__Usage:__```cat file.txt | uniq```

```console
user$: cat file2.txt
apple
banana
apple
apple
banana
banana
banana
user$: cat file2.txt | uniq
apple
banana
apple
banana
user$: cat file2.txt | uniq -c
   1 apple
   1 banana
   2 apple
   3 banana
```

# Unique values and histogram

Individually, these commands are moderately useful. However, they can be quite deadly when combines. You can, for example, combine them to find all the unique values that appear in the file. 

__Finding unique values__

If we sort the values before "uniquing" them, all the values are deduplicated because they have been grouped together. 

```console
user$: cat file2.txt
apple
banana
apple
apple
banana
banana
banana
user$: cat file.txt | sort | uniq
cat
cow
dog
```

__Histogram__

Once we have the set of unique values, we can tell the uniq command to tell us how many times each value is present. We can then reverse sort the value by the number of times they appear. The result is a list or "histogram" ranking the file values based on the number of times they appear.

```console
user$: cat file.txt
cat
dog
cow
cat
dog
dog
cow
cat
cow
cat
user$: cat file.txt  | sort | uniq -c | sort -rn
   4 cat
   3 dog
   3 cow
```
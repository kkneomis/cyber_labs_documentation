# Text Analysis (awk)

### Text parsing using awk

The ```awk``` command allows us to select text from a given column in a given file. By default, awk delimits columns by spaces. Suppose we had a text file with multiple columns delimited by spaces. Here is how we could select all the values in the first column.

```console
user$ cat data.txt  
Name Age Grade
Paul 15 A
Molly 18 C
Tyrone 17 A
Candice 16 B

user$: cat data.txt |  awk '{print $1}'
Name
Paul
Molly
Tyrone
Candice
```

Suppose, instead, we wanted to select the third column instead. We would change ```$1``` to ```$3``` to reflect the appropriate column.

```console
user$: cat data.txt |  awk '{print $3}'
Grade
A
C
A
B
```

If the columns are not delimited by spaces, we can use the ```-F``` flag to specify an alternate delimiter. In this example, we will instead delimit columns by commas.

```console
user$ cat data.txt
Name,Age,Grade
Paul,15,A
Molly,18,C
Tyrone,17,A
Candice,16,B

user$: cat data.txt |  awk -F "," '{print $1}'
Name
Paul
Molly
Tyrone
Candice
```

We can also add logic to our command. In this example we will print every in the file except for the header (first line).

```console
user$: cat data.txt | awk -F ',' '{if(NR>1) print}'
Paul,15,A
Molly,18,C
Tyrone,17,A
Candice,16,B
```


Awk can also be used to reformat the data to a prefered view.

```console
user$: cat data.txt | awk -F ',' '{if(NR>1) print}'|  awk -F "," '{print "Name: "$1 "\tAge: "$2 "\tGrade:"$3}' 
Name: Paul      Age: 15 Grade:A
Name: Molly     Age: 18 Grade:C
Name: Tyrone    Age: 17 Grade:A
Name: Candice   Age: 16 Grade:B
```

# awk Command

### awk '{ print }' filename.txt
* Prints every line in the file. 

### awk '{ print $1 }' filename.txt
* Prints the first column of text in the file. A whitespace ends a column.

### awk '{ print $2 }' filename.txt
* Prints the second column of text in the file. A whitespace ends a column.

### awk '{ print $1,$2 }' filename.txt
* Prints the first and second column of text in the file. A whitespace ends a column.

### awk '{ print $1.$2 }' filename.txt
* Concatenates the first and column of text in the file. A whitespace ends a column.

### awk '/regex-pattern/ { print }' filename.txt
* Prints everything in filename.txt that matches the regex /regex-pattern/.
* With awk, regex is written between / and /.

### awk '{ if ($1 ~ /regex-pattern/) print }' filename.txt
* Prints the everything on the first column of filename.txt that equals /regex-pattern/.
* With awk, ~ is an equal sign. 

### awk -f filename.awk filename.txt
* Executes the awk code stored in filename.awk on filename.txt. 
* You can write awk commands, like the ones previously shown, inside an awk file.
* filename.awk can be edited with any text editor. 

## Notes
* Thanks to https://www.youtube.com/watch?v=az6vd0tGhJI for the tutorial.

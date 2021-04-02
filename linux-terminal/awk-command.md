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

### for loop 
* Similar syntax to Java for-loop except no semi-colon at the end or data types specified.
* Placed within the curly braces, i.e. 
  * awk '{ for(i=1;i<10;i++) { print } }' filename.text

### function 
* Syntax examples:
  * func funcName(args) {
  
    }
  * func funcName(args) {
  
       return 'some text'
     
    }
* No datatype is specified for parameters or return value. 
* No semi-colon after function or return statement. 


## Notes
* awk commands can be piped into other commands or programs using |. For example,
  * awk '{ print }' filename.txt | grep "string-pattern-to-search-from-awk-output"
* Thanks to https://www.youtube.com/watch?v=az6vd0tGhJI for the tutorial.
* Thanks to https://www.youtube.com/watch?v=jJ02kEETw70 for the tutorial.

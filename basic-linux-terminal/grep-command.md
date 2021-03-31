# grep Command

grep stands for Global Regular Expression Print.




## 1. You must navigate to the directory where the file or files are located to use grep on them. 


### grep "string-pattern-to-search" filename.extension
* Returns text inside filename that matches "string-pattern-to-search". 
* Defaults to case-sensitive search.

### grep -w "string-pattern-to-search" filename.extension
* -w returns whole-word matches. 

### grep -i "string-pattern-to-search" filename.extension
* -i performs a case-insensitive search and returns any matches. 

### grep -wi "string-pattern-to-search" filename.extension
* -wi combines -w and -i. 

### grep -n "string-pattern-to-search" filename.extension
* -n Includes the line number of the match. 

### grep -win "string-pattern-to-search" filename.extension
* -win combines -w, -i, and -n

### grep -win -B 4 "string-pattern-to-search" filename.extension
* -win -B 4 combines -w, -i,-n, and -B 4. 
* -B 4 includes with the match the 4 lines before the match; it is used for context. 
* Any number of lines may be commanded. 

### grep -win -A 2 "string-pattern-to-search" filename.extension
* -win -A 2 combines -w, -i,-n, and -A 2. 
* -A 2 includes with the match the 2 lines after the match; it is used for context. 
* Any number of lines may be commanded. 

### grep -win -C 3 "string-pattern-to-search" filename.extension
* -win -C 3 combines -w, -i,-n, and -C 3. 
* -C 3 includes with the match the 3 lines after and before the match; it is used for context. 
* Any number of lines may be commanded. 

### grep -win "string-pattern-to-search" ./*
* ./* at the end of the command causes a search throughout the working directory.
* -win combines -w, -i, and -n. 

### grep -winr "string-pattern-to-search" ./
* -win combines -w, -i, -n, and -r.
* -r causes a recursive search.
   * Searches the current directory due to ./ at the end of the command and any subdirectories.

### grep -wirl "string-pattern-to-search" ./
* -wirl combines -w, -i, -r, and -l.
* -l causes the filenames that contain a match to be returned and not the match itself. 

### grep -wirc "string-pattern-to-search" ./
* -wirc combines -w, -i, -r, and -c.
* -c returns the same as -l, but it includes the number of matches found in each file. 

### Practical Examples:
* history | grep "git commit" 
    * Data returned by history is given to grep "git commit" and processed. 
    
* history | grep "git commit" | grep "-m Initial commit."
    * Data returned by history is given to grep "git commit" and processed, then to grep "-m Initial commit." and proccessed even further. 

## Note

* grep may be given a regular expression to search. For example, grep "\w+" filename.extension

* For regular expression to work make sure you use the GNU version of grep. Check for the version of grep by running grep -V


#### Thanks to Corey Schafer for the information. https://www.youtube.com/channel/UCCezIgC97PvUuR4_gbFUs5g

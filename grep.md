## grep command
The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern. The pattern that is searched in the file is referred to as the regular expression (grep stands for globally search for regular expression and print out). 

### Case inSensitive search(searching UNix word in test.txt file)
```
grep -i "UNix" test.txt
```

### Displaying the count of number of matches 
```
grep -c "unix" test.txt
```
###  Display the file names that matches the pattern
```
grep -l "unix" *
```
###  Checking for the whole words in a file 
```
grep -w "unix" test.txt
```
### Show line number while displaying the output using grep -n 
```
 grep -n "unix" test.txt
```

### find a username from /etc/passwd file
```
 cat /etc/passwd | grep testuser
```

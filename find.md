## find command
The find command in UNIX is a command line utility for walking a file hierarchy. It can be used to find files and directories and perform subsequent operations on them. It supports searching by file, folder, name, creation date, modification date, owner and permissions. 

### Search a file with specific name.
```
find /root -name sample.txt
```

### Search a file with pattern.
```
find /root -name *.txt 
```

### Search for empty files and directories.
```
find /root -empty
```

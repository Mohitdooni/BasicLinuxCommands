### chmod (change mode)
In Unix-like operating systems, the chmod command is used to change the access mode of a file.

The references are used to distinguish the users to whom the permissions apply i.e. they are list of letters that specifies whom to give permissions

<table>
  <tr><td><b>Reference</b>   </td><td><b>Class</b>   </td> <td><b>Description</b> </td></tr>
  <tr><td>u   </td><td>owner   </td> <td>file's owner </td></tr>
  <tr><td>g   </td><td>group   </td> <td>Member of file's group </td></tr>
  <tr><td>o   </td><td>other   </td> <td>Members those neither owner or file group members </td></tr>
</table>  

### Operators

<table>
  <tr><td><b>Operator</b>   </td> <td><b>Description</b> </td></tr>
  <tr><td>+   </td><td>owner   </td> <td>Add permission </td></tr>
  <tr><td>-   </td><td>group   </td> <td>To remove permission </td></tr>
  
</table>  

### Permission Modes
<table>
  <tr><td><b>Mode</b>   </td> <td><b>Description</b> </td></tr>
  <tr><td>r   </td> <td>Read Permission </td></tr>
  <tr><td>w   </td> <td>Write Permission </td></tr>
  <tr><td>x   </td> <td>Execute Permission </td></tr>
  
</table> 

### Mode Numeric values

<table>
  <tr><td><b>Value</b>   </td><td><b>Permissions</b></td> <td><b>Description</b> </td></tr>
  <tr><td>7   </td><td>rwx   </td> <td>Read Write Execute Permission </td></tr>
  <tr><td>6   </td><td>rw   </td> <td>Read Write  Permission </td></tr>
  <tr><td>5   </td><td>rx   </td> <td>Read Execute Permission </td></tr>
  <tr><td>4   </td><td>rx   </td> <td>Read Write Permission </td></tr>
  <tr><td>3   </td><td>wx   </td> <td>Write Execute Permission </td></tr>
  <tr><td>0   </td><td>---   </td> <td>No permission </td></tr>
  
</table> 

### Login with root user and create an empty file and check its permission
```
sudo su
touch tmpfile.txt
ls -l tmpfile.txt

output
-rw-r--r-- 1 root root 0 Sep 25 11:36 tmpfile.txt
```

### Change permission to this file owner can read and write but group users can read and other donot have any permission to access this file
```
chmod 640 tmpfile.txt
ls -l tmpfile.txt
```

### Login with a user and check other user can read it or notcat: tmpfile.txt: Permission denied
```
su testuser
cat tmpfile.txt

output will be
cat: tmpfile.txt: Permission denied
```

### Login agin with root user and provide read access to other users

```
exit
echo "Test file content" >> tmpfile.txt
chmod o+r tmpfile.txt

```
## Login with a user and check other user can read it or notcat: tmpfile.txt: Permission denied
```
su testuser
cat tmpfile.txt

output
Test file content
```






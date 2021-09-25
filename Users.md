### User Management in Linux
A user is an entity, in a Linux operating system, that can manipulate files and perform several other operations. Each user is assigned an ID that is unique for each user in the operating system. 

### Types of users
<ul>
  <li><b>Administrator(root or super user):-</b> It is automatically created when you install Linux.It has administrative privileges for all the services on Linux OS </li>
  <li><b>Regular User:-</b> The Linux Regular users have only the necessary privileges to perform standard tasks such as running services or applications etc. </li>
  <li><b>Service Users:-</b> Services like Apache,Jenkins,games,printing etc have their own service user account.These accounts allow these services to intreact with Linux OS </li>
</ul>

### Login to root user
```linux
$ sudo su 
```

### Create a user testuser
```
 useradd testuser
```

### Find the user details 
```
  cat /etc/passwd | grep testuser
```

### Delete the user
```
userdel testuser
```

### Create a user with its home directory(it is a directory where user profile is stored)
```
useradd -m -d /home/testuser testuser
```
### Delete a user alonw with removing  all its its including home directory
```
 userdel --remove testuser
```
### create a user with password
```
useradd testuser
passwd testuser
```

### Find the userid of a user
```
 id testuser
```

### Find the userid of current user
```
id
```

### Find the current user ( login user)
```
whoami
```

### Login with a specific user
```
su testuser
```

### Verify login user
```
 id
 whoami
```
### Exit from current user
```
exit

```
### Create a usergroup (login with root user)
```
groupadd testgroup
```

### Verify the group is created
```
cat /etc/group | grep testgroup
```

### Delete a usergroup
```
groupdel testgroup
```
### Add a user into an existing group
```
groupadd testgroup
usermod -a -G testgroup testuser
```

### Create a user to an existing group
```
useradd test1  -G testgroup

```

### Verify the group is created with user, it should show all the user under a group
```
cat /etc/group | grep testgroup
```



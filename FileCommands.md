## Linux file commands

### touch :- Create an empty file
### cat :- read/write/apend a file
### rm :- Delete a file
### cp :- Copy a file from source to destination directory
### mv :- Move or rename a file from source to destination directory
### vi,nano :- These are the Text editors to create or modify a file


### Examples ( Assume all the directories in below examples exists)

#### Create an empty file (App01.txt) under /tmp/test/testingTypes/unitTest directory
```
 touch /tmp/test/testingTypes/unitTest/App01.txt
```
#### Create 2 more empty filess (App02.txt and App03.txt) under /tmp/test/testingTypes/unitTest directory
```
  cd /tmp/test/testingTypes/unitTest
  touch App02.txt App03.txt
```

#### Copy App03.txt file to /home/ubuntu directory
```
cp App03.txt /home/ubuntu/.
```
#### Add some data inside /home/ubuntu/App03.txt file and read the contents
```
cd /home/ubuntu
echo "This is test case 3" >> App03.txt
cat App03.txt
```
#### Delete the App03.txt file from /tmp/test/testingTypes/unitTest
```
rm /tmp/test/testingTypes/unitTest/App03.txt
```

#### Move /home/ubuntu/App03.txt to /tmp/test/testingTypes/unitTest
```
mv App03.txt /tmp/test/testingTypes/unitTest/App03.txt
```
#### Open /tmp/test/testingTypes/unitTest/App02.txt in vi editor and add some text into this file(:wq! save and exit and :q! for quit without save)
```
 vi /tmp/test/testingTypes/unitTest/App02.txt
```
#### Remove all txt files under  /tmp/test/testingTypes/unitTest
```
rm  /tmp/test/testingTypes/unitTest/*.txt
```

## Assignment
<ul>
 <li> Create a ERPProj directory under /home/ubuntu/GithubProjects </li>
 <li> Create three more diectories and sub directories under ERPProj directories as mentioned below <br />
      /home/ubuntu/GithubProjects/ERPProj/Modules <br />
      /home/ubuntu/GithubProjects/ERPProj/Modules/BAL <br />
      /home/ubuntu/GithubProjects/ERPProj/Modules/DAL <br />
  /home/ubuntu/GithubProjects/ERPProj/Modules/UIL <br /> </li>
 <li>Create some dummy 3 files under  BAL and DAL </li>
 <li>Create some html files under /home/ubuntu directoy (like index.html and test.html) </li>
 <li>Move all these html file under /home/ubuntu/GithubProjects/ERPProj/Modules/UIL </li>
 <li>Create a new folder called /home/ubuntu/FinalProject </li>
 <li> Move ERPProj to FinalProject folder </li>
 <li> Read all files one by one check it is moved successfully or not </li>
</ul>      
  

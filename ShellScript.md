## Shell Scripts
The basic concept of a shell script is a list of commands, which are listed in the order of execution. A good shell script will have comments, preceded by # sign, describing the steps.

There are conditional tests, such as value A is greater than value B, loops allowing us to go through massive amounts of data, files to read and store data, and variables to read and store data, and the script may include functions.

We are going to write many scripts in the next sections. It would be a simple text file in which we would put all our commands and several other required constructs that tell the shell environment what to do and when to do it.

##### Note:-> Provide execute permission to your script so that it can be executed. chmod +x filename. sh filename to execute the file or ./ filename

### Example 1 (test.sh). Shell Script to display current director and list all the files
```
pwd
ls -la

```

### Example 2 use of Variable
```
echo "What is your name?"
read PERSON
echo "Hello, $PERSON"
```

### Example 3 readonly variable (whose value cannot be changed) below example throws the exception
```
NAME="John"
readonly NAME
NAME="Mathew"
```

### Special variables
<table>
  <tr><td><b>Variable & Description</b></td></tr>
  <tr><td> $0 The filename of the current script.</td></tr>
  <tr><td>$n These variables correspond to the arguments with which a script was invoked. Here n is a positive decimal number corresponding to the position of an argument (the first argument is $1, the second argument is $2, and so on).</td></tr>
  <tr><td>$# The number of arguments supplied to a script.</td></tr>
<tr><td>$* All the arguments are double quoted. If a script receives two arguments, $* is equivalent to $1 $2.</td></tr>
<tr><td>$@ All the arguments are individually double quoted. If a script receives two arguments, $@ is equivalent to $1 $2.</td></tr>
<tr><td>$? The exit status of the last command executed.</td></tr>
<tr><td>$$ The process number of the current shell. For shell scripts, this is the process ID under which they are executing.</td></tr>
<tr><td>$! The process number of the last background command.</td></tr>
 </table>
 
 ## Example
 ```
 echo "File Name: $0"
echo "First Parameter : $1"
echo "Second Parameter : $2"
echo "Quoted Values: $@"
echo "Quoted Values: $*"
echo "Total Number of Parameters : $#"

 ```
 ```
 Execute above script with test.sh linux toturial
 ```
 
 ### Example display all command line argument (sh test.sh linux tutorial)
 ```
 for TOKEN in $*
do
   echo $TOKEN
done
 ```
 
 ### Example if statement
 ```
 #!/bin/bash
# Basic if statement
if [ $1 -gt 100 ]
then
echo Hey that\'s a large number.
pwd
fi
date

 ```

### Exmaple (if else)
```
f [ $# -eq 1 ]
then
 echo "Exact no of argument"
else
 echo " more no of argument"
fi

```
### Example (if elif)
```
if [ $1 -ge 18 ]
then
echo "You may go to the party."
elif [ $2=='yes' ]
then
echo "You may go to the party but be back before midnight."
else
echo You may not go to the party.
fi

```

### Example case ... esac
```
case $1 in
start)
echo starting
;;
stop)
echo stoping
;;
restart)
echo restarting
;;
*)
echo don\'t know
;;
esac

```

### Example for loop
```
for a in 1 2 3 4 5 6 7 8 9 10
do
    echo "Iteration no $a"
done

```
### Example while loop
```
a=0
# -lt is less than operator

#Iterate the loop until a less than 10
while [ $a -lt 10 ]
do
    # Print the values
    echo $a

    # increment the value
    a=`expr $a + 1`
done

```

### Example until loop
```
a=0
# -gt is greater than operator

#Iterate the loop until a is greater than 10
until [ $a -gt 10 ]
do
	# Print the values
	echo $a
	
	# increment the value
	a=`expr $a + 1`
done

```

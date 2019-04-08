Shell Programming 

# Common commands
useradd/adduser, userdel,
paaword
groupadd, groupdel;

su
sudo
who
which: display commands save path
type
time 

touch:
cat:
tail:
head
more/less
wc [-c/-l/-w/-L-m]

pwd
mkdir
ls
mv
cp
rm

chmod
chown
file: check file type

find
grep

## System Management
ping
ifconfig
route
netstat
env

ps aux
top
free

df
fdisk


# Variables in Shell Script
Pass value:
```
#! /bin/bash

echo "Pass value to variable"

num=10
echo $num

num=100
echo $num

echo "Ending"
```

Variable input/output
```
#! /bin/bash
  
echo "Starting"
read num
echo "variable: "$num

echo -n "input"
read num
echo "variable: "$num
```

```
read -p: multiple input variables
read -t10: wait 10 seconds to accept input 
read -n10: quit input status until accept 10 inputs 
read -s: input data will not display on the monitor

echo -n: don't change line
echo -e: output special char
echo --help
echo --version
```

```
#! /bin/bash
  
echo "number of input: "$#
echo "script name: "$0
echo "first varuable: "$1
echo "second: "$2
echo "third: "$3

echo "input: "$*
```

```
$0: Script name
$1-$9: Input parameters
$#: Number of parameters
$?: return of the script
$*: contents of the parameter
```

# Pipe 
executes many commands 

&: runs as damon
  e.g. 001.sh&

# File Processing
file type: text; binary;  Dir; Link; Device; Pipe


# If-then 
```
if expression
then
commands
fi


if expressions
then
   commands1
 else
   commands2
fi 

```

```
echo 
if test 3 -le 5
then 
  echo 3 is less than 5
fi
  echo 

echo 
if test 5 -le 3
then 
  echo 5 is less than 3
fi
```

```
-le: less than
-ge: greater than 
```

```
case variable in
pattern1) commands1;;
pattern2|pattern3) commands2;;
*)command3;;
esac
```

```
select <variable> in <list>
do 
  commands
done
```

# Loop

```
for <variable> in <range list>
do
  commands;
done
```

```
for(expression1; expression2; expression3)
{

	loop code;
}

for((expression1; expression2; expression3))
do
  loop code;
done 
```

```
while test <expression>
do
  commands
done


while[$num -gt 3 -a $num -lt 6]
do 
   echo num=$num
let num++
done 
```


```
until test expression
do
  commands;
done;
```

```
break
continue
```

# Function

```
<function name>
{
	commands
}
```

```
name()
{
	echo "call name function"
}
```

```
return 
```

```
local num: 
num: default is global
```

```
nums1=(1,2,3,4,5)
```

# Optimization
- Redirection is better than Pipe while the script is doing a repeat thing

- We'd better no use high-level tools like awk, sed if the internal command can do it. (because it will create a new process, cost CPU and Memory resource)

Common options for commands
```
-a: display the whole content
-c: execute count function
-d: target directory
-e: unfold content
-f: fetch file from a target directory
-h: get help info
-r: process files in recursive way
-y: answer Yes for all following questions
-v: fetch verison info
-i: case insenstive
```

Arithmetic Operation
```
let command
(()) command
expr 
```

# Regular Expression

# grep 
grep [option] [pattern] [file list]
fetch a target file from a directory.

options:
-c: output count 
-i: case insenstive
-h: don't display file name
-n: display matching line and row lone
-s: don't display non-existed or non-matching error info
-v: 
-E:

egrep: search from one or more files

fgrep: search string from files


# sed
streaming editor

replace; delete; add; 


# gawk

# Script Control

nohup: the process will not terminated if you logout current shell
&: the process will terminated if you logout current shell
 
## Priority:
 PRI, NI.

Set priority:
nice[-n <priority level>][commands]
renice [priority level][-g <>][-p < >][-u < >]


# Project Plan
at: process one-time plan 

-m
-l
-d
-v
-c
-V
-q
-f
-t

atq: list all tasks in a queue

-q
-V

cron: process plan periodically

-e
-l


ftp
nfs


## Log
syslogd

tar
-x: unpack
-c: pack up
-t: list all file
-v: diaplay file during packing up
-z: if it has zip attribute
-f: use file package name
-p: use original file attribute































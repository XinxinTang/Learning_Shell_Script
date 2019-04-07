Shell 

# Common commands
useradd/adduser, userdel,
paaword
groupadd, groupdel;

su
sudo
who
which: display commands save path

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

































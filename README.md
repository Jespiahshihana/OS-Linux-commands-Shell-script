# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
![image](https://github.com/user-attachments/assets/1a2d6a2c-2d50-4cfa-bbe6-3363ce460282)

cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
![image](https://github.com/user-attachments/assets/cf2c6186-1003-41cd-986e-e9cff2d4fdbe)

### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/user-attachments/assets/f3eb5437-b4fb-41b2-95ae-a8e88da184a9)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/e243be37-be4b-44d3-bd71-d8a219f12bd5)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/f7696192-73fe-4d92-811b-c32424afa4a9)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/074422e8-1b59-4eee-8730-952d71254d83)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/79840b03-012e-4c6e-97f1-bbce30b4a2a8)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
![image](https://github.com/user-attachments/assets/e1fb79e4-af68-41be-a390-129693e060da)

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT


![image](https://github.com/user-attachments/assets/bad83333-5db6-405d-af74-2aedfbafdca7)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/bdc0aac8-7b71-4214-a629-5558d0610083)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/572004ef-6e55-48ae-9b67-8ead01d5306f)


cat < newfile 
```
Hello world
hello world
^d
````
![image](https://github.com/user-attachments/assets/278c7af3-61de-481a-8f8e-f5acbb3c0fff)
```
cat > newfile 
Hello world
hello world
 ```
![image](https://github.com/user-attachments/assets/b96eb731-4317-4853-a4fe-888482fba665)

grep Hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/da47d8f5-92ac-4c2e-b3b3-52adf2c38bfc)



grep hello newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/21520d83-59de-4023-a264-9aba22f71663)


grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/4cae5903-938d-4558-9978-f9817bd20a9e)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/7707988f-568b-4200-8107-08535bb79463)



cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/e4b8d66c-65dc-4c48-a94f-29db97392f86)


grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/aea3e907-2d08-49c8-9b78-f87e3be0cc44)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/9a594dbe-4629-419f-8fa1-9e09077e899d)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
![image](https://github.com/user-attachments/assets/7eca800b-2cd0-4522-92e1-808b86d3a8c1)

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
![image](https://github.com/user-attachments/assets/f326f080-78f6-4491-92e3-1e76d1d9b8f3)

egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/43c630af-0722-43e2-a302-a7b5049fe50f)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/8c2898d4-fca0-4a0f-8999-1c7a9f854e6b)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/72cd44a3-9ad8-472a-9c63-14cbf0f3ea09)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f2df7f96-65dd-4be7-9a4a-cd3e7b1e7ccb)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6df57dc3-6f34-46ba-abd3-f86dca04f5da)



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b434ba16-d286-481d-a4a9-d62bae4a779c)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/67efd3a9-54be-47bf-afb0-21ff0348321b)


egrep 'Linux.*world' newfile 
## OUTPUT


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a646ecd2-57f3-4e43-b6d9-fdfe93dc5d97)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/36354ff9-552d-4572-afb6-d21db980c45b)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/bed0d2c7-4bf0-4884-896b-8e29e4688009)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```
![image](https://github.com/user-attachments/assets/8f86174d-3808-408a-ac55-50f5d1bc7f46)


sed -n -e '3p' file23
![image](https://github.com/user-attachments/assets/6a341218-3a25-44d7-880e-bd756c9eef6c)

## OUTPUT
![image](https://github.com/user-attachments/assets/3d5529a7-1397-494a-ad54-16ba01a0527b)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c7b7fb58-22fd-425c-862c-30d741823536)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2b17fae8-49fe-4e84-ab44-5ef38fd45403)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/1a529b1d-cb80-49ee-ba01-a0ceb6bea4a6)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/f8b4aed7-b924-4445-a0eb-b8e71eb77096)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5d3183bc-02cd-46c9-9cb9-bf02f6162dee)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/4e865b02-bd12-4677-b15b-77b0b798d32a)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/f5fec9cb-26e4-4ee3-9b3b-a6d1d45d74e4)


seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/4e3a8b0b-9c37-49f5-8aec-65e57dc720e0)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/bada5aa8-a9a4-4d05-af7c-350d623c364a)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d9a70179-5597-4ef5-8a63-b309f78841d2)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/dfe09689-93ad-4233-9914-cf884ba304fc)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/c6e20d03-980f-403c-8657-ae651220ed9f)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/eb3c052f-2750-4d18-b89b-d522e5baebed)


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
![image](https://github.com/user-attachments/assets/abed95ef-284e-4af5-bacc-d00a4cd4f496)

## OUTPUT



cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22

![image](https://github.com/user-attachments/assets/a10de57a-0fbc-4d12-aba2-89cb64501114)
![image](https://github.com/user-attachments/assets/b5627394-d620-4756-9ce6-aacdbc6e62cc)
## OUTPUT



#Using tr command
![image](https://github.com/user-attachments/assets/6bcd85da-f895-49e6-ac79-cf9ad7ce43b2)


cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/eee77783-d947-4fcd-bc48-68759d52088b)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
![image](https://github.com/user-attachments/assets/749d3a78-cc3b-47d1-a88a-ae13d666200a)

cat urllist.txt | tr -d ' '
![image](https://github.com/user-attachments/assets/5f472f8a-f583-4b14-96c3-7eb68a029a3c)

 ## OUTPUT

![image](https://github.com/user-attachments/assets/c7219d21-86c8-4614-aa9d-771232289315)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
![image](https://github.com/user-attachments/assets/b5d082cf-7de0-4a0a-9e6d-193b2d1501fe)

tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
![image](https://github.com/user-attachments/assets/12313382-9680-459e-9047-a9cca309687d)

 
tar -tvf backup.tar
![image](https://github.com/user-attachments/assets/d6fc84fb-62a5-4edc-bc13-49a1081a6085)

## OUTPUT

![image](https://github.com/user-attachments/assets/d7265646-60a4-4958-8a56-4867745aedb6)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/1a8ba816-84fc-42e8-bf3d-ff1afb43be06)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/05f90ee2-c0b7-4c4e-b6bf-34abe1dbdd3c)

gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.

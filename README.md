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
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![Screenshot from 2024-09-12 15-55-39](https://github.com/user-attachments/assets/9b6b191e-5d33-4d2c-9d98-e70ed823436a)



cat < file2
## OUTPUT
![Screenshot from 2024-09-12 15-55-45](https://github.com/user-attachments/assets/83fe3a09-0b9b-4f6b-8f4d-03192d059997)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2024-09-12 15-44-21](https://github.com/user-attachments/assets/fa28ef8b-864e-4ba2-a9cb-cf2bcae5bd16)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-09-12 15-44-41](https://github.com/user-attachments/assets/6a14df2d-d139-42d9-98cc-41694d5a2efd)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-08-29 15-05-52](https://github.com/user-attachments/assets/bf116106-56bd-44ea-8247-928a28baf415)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![Screenshot from 2024-08-29 15-11-29](https://github.com/user-attachments/assets/93e51f30-1b07-428c-a41d-44e22fbbe020)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2024-08-29 15-12-04](https://github.com/user-attachments/assets/a2d8c8d0-5987-40c2-add7-6fd8d64ec330)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-08-29 15-12-16](https://github.com/user-attachments/assets/a02c0b0c-3404-4cb8-bd57-d56fbf42ea48)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![Screenshot from 2024-08-31 00-56-08](https://github.com/user-attachments/assets/b35a6efc-93ad-4979-98df-e01718a7a64a)



grep hello newfile 
## OUTPUT
![Screenshot from 2024-08-31 00-56-49](https://github.com/user-attachments/assets/6a407188-82af-432b-a9fe-1cf2ce499802)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-08-31 00-57-21](https://github.com/user-attachments/assets/a365b161-2217-41c8-9eae-9fbc574bc1f9)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2024-08-31 00-57-53](https://github.com/user-attachments/assets/979fb40a-3ed6-4590-98d1-f86e2c822821)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2024-08-31 00-58-07](https://github.com/user-attachments/assets/0963d6f9-0e02-40c2-9f9e-047e839f80d8)



grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-08-31 00-59-02](https://github.com/user-attachments/assets/e2d4880b-af28-4a9f-822d-86dc517d88e4)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-08-31 00-59-34](https://github.com/user-attachments/assets/8d321a17-df92-4f24-93ce-e729029d6c63)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![Screenshot from 2024-08-31 01-00-01](https://github.com/user-attachments/assets/14ac5520-e6fa-48cc-8343-c2e45c509519)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2024-08-31 01-00-13](https://github.com/user-attachments/assets/bf8d99fa-9fa5-4857-8e20-892a06d23725)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2024-08-31 01-00-32](https://github.com/user-attachments/assets/2a20ff34-f61a-4d63-af01-9c8553669e06)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-08-31 01-00-46](https://github.com/user-attachments/assets/fff7f5d7-19d5-4319-8757-f9c1aafc611b)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-08-31 01-00-54](https://github.com/user-attachments/assets/a97445d9-07bd-441e-88f4-70aa7058237f)



egrep '(World$)' newfile 
## OUTPUT

![Screenshot from 2024-08-31 01-01-06](https://github.com/user-attachments/assets/b377e444-0b9b-4189-801d-58f36bc26a2b)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2024-08-31 01-01-22](https://github.com/user-attachments/assets/b229e3fd-479d-45f5-a7b7-619d7a3b1436)


egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-08-31 01-02-22](https://github.com/user-attachments/assets/56e2a7f2-53d6-47e2-a729-541cd1a8aa1d)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-08-31 01-02-29](https://github.com/user-attachments/assets/045b01ea-5885-483c-872f-d310a6be96a6)



egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-08-31 01-02-36](https://github.com/user-attachments/assets/81f3ede0-4d22-4bc5-bf35-58ada0d31306)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-08-31 01-02-51](https://github.com/user-attachments/assets/84c53be3-af78-4073-a3d5-5701c819bb8b)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-08-31 01-03-04](https://github.com/user-attachments/assets/c6aee395-7976-4d29-8e86-81dfc9a1049a)


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


sed -n -e '3p' file23
## OUTPUT

![Screenshot from 2024-08-31 01-03-11](https://github.com/user-attachments/assets/b6cabca1-3a4a-44d7-82b5-6b39ae91b951)


sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2024-08-31 01-03-15](https://github.com/user-attachments/assets/a667993a-03f9-44d6-b462-79d7fc96f17c)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-08-31 01-03-38](https://github.com/user-attachments/assets/77d0369a-835d-4f89-b7d7-0cb5366d479b)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2024-08-31 01-03-51](https://github.com/user-attachments/assets/efb8d016-6b53-4ff8-8bfb-c1addec0262a)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-08-31 01-03-59](https://github.com/user-attachments/assets/a0e98077-4a95-4c38-b427-b2a8e17d055e)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-08-31 01-04-11](https://github.com/user-attachments/assets/0cbb6a1d-400c-4ada-8ca3-e16827877f5c)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2024-08-31 01-04-23](https://github.com/user-attachments/assets/b23b38e6-4547-4928-8e73-a937a15bfe22)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-08-31 01-04-28](https://github.com/user-attachments/assets/e055e93a-21af-421b-a7c6-528b7ecb57fd)



seq 10 
## OUTPUT
![Screenshot from 2024-08-31 01-04-50](https://github.com/user-attachments/assets/3e0340a0-2cc9-4770-ba6a-c4c0ad60c2a5)



seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2024-08-31 01-05-08](https://github.com/user-attachments/assets/ad838537-8589-4faa-b46c-82cb7c216bcd)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2024-08-31 01-05-21](https://github.com/user-attachments/assets/66a977f8-9955-402d-9a30-6d976f5b2139)


seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-08-31 01-05-27](https://github.com/user-attachments/assets/65b7ca6a-3726-4a8c-981e-a45965b73583)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-08-31 01-05-36](https://github.com/user-attachments/assets/eca581ee-412b-4043-9f5f-f277a3aee77a)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2024-08-31 01-05-44](https://github.com/user-attachments/assets/9dae29fa-ba1d-40d2-abd8-5a80745a9791)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2024-08-31 01-05-58](https://github.com/user-attachments/assets/a4cae7c3-7f2b-48bc-acf0-fa950705c447)


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
## OUTPUT
![Screenshot from 2024-08-31 01-05-52](https://github.com/user-attachments/assets/3cfe1443-24bf-46c7-b161-73ccbaf820be)


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
## OUTPUT



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-08-31 01-06-07](https://github.com/user-attachments/assets/86516f0a-566e-43cc-800f-e56b92d07a70)

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
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot from 2024-08-31 01-06-23](https://github.com/user-attachments/assets/70810c4e-49b7-4d8c-81ef-89f2a01c92b0)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2024-08-31 01-06-36](https://github.com/user-attachments/assets/9d6f9dcb-36f8-4341-a293-59ed906ca269)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-08-31 01-07-03](https://github.com/user-attachments/assets/5295562f-80fb-44f7-b764-75e8864b4da6)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2024-08-31 01-07-24](https://github.com/user-attachments/assets/cc21b39a-cd83-4caf-8255-939987d45ff8)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2024-08-31 01-07-38](https://github.com/user-attachments/assets/e58670c5-3268-40a5-8b42-180b66ebd770)

gzip backup.tar

ls .gz
## OUTPUT
![Screenshot from 2024-08-31 01-07-48](https://github.com/user-attachments/assets/b14968ae-f110-437b-a52c-2ca9a6300890)
 
gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2024-08-31 01-08-00](https://github.com/user-attachments/assets/59ab69b8-ccd7-4e9f-b62b-858c3f6ae774)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2024-08-31 01-08-09](https://github.com/user-attachments/assets/4ef16237-7254-4df2-9867-1ae5331b6134)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2024-08-31 01-08-17](https://github.com/user-attachments/assets/1a8de362-6a5d-482d-9259-b9eb1c84a762)


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
![Screenshot from 2024-08-31 01-08-34](https://github.com/user-attachments/assets/17e573a4-34d6-49bc-a9c4-5e974444aabf)

 
ls file1
## OUTPUT
![Screenshot from 2024-08-31 01-08-53](https://github.com/user-attachments/assets/4abe4551-6047-4a42-b8e4-5c5bdc40b15e)

echo $?
## OUTPUT 


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

![Screenshot from 2024-08-31 01-09-05](https://github.com/user-attachments/assets/4701bf55-db51-4626-976b-3156bee77473)

 
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
## OUTPUT

![Screenshot from 2024-08-31 01-09-20](https://github.com/user-attachments/assets/af119fdc-e30c-4aba-80c1-34091dd3ee9c)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2024-08-31 01-09-30](https://github.com/user-attachments/assets/665c7e4f-0456-4ad3-876b-fe5abb958866)


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
![Screenshot from 2024-08-31 01-09-38](https://github.com/user-attachments/assets/477a039d-918a-4e80-a2f2-be60cc8fa6e7)

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

![Screenshot from 2024-08-31 01-09-57](https://github.com/user-attachments/assets/ac167094-5f53-4608-96f8-3cf93d186549)


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
## OUTPUT
![Screenshot from 2024-08-31 01-10-03](https://github.com/user-attachments/assets/3a203a71-c981-4436-b6be-8dfd4400e2c9)

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
## OUTPUT
![Screenshot from 2024-08-31 01-10-03](https://github.com/user-attachments/assets/e3b2f6a0-ece2-4068-93ba-f6e8749e9ec6)

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
![Screenshot from 2024-08-31 01-10-16](https://github.com/user-attachments/assets/a6089fb6-9a2a-4ca5-9884-8829d6de5597)


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
![Screenshot from 2024-08-31 01-10-21](https://github.com/user-attachments/assets/9b071521-d320-4ca5-89f4-dff7851eeb48)

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
![Screenshot from 2024-08-31 01-11-21](https://github.com/user-attachments/assets/8be65f7c-5561-42b4-82df-3bd50b8e760f)

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
![Screenshot from 2024-08-31 01-12-07](https://github.com/user-attachments/assets/72f4749d-81b5-45b6-825d-656d487aa6c5)

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
![Screenshot from 2024-08-31 01-12-18](https://github.com/user-attachments/assets/afb0b997-c4bd-4e0f-83ed-e0a093ec65c0)

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

 ![Screenshot from 2024-08-31 01-12-29](https://github.com/user-attachments/assets/1ff9a818-5818-48c5-97c5-7f1f68f7eedf)

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
![Screenshot from 2024-08-31 01-12-43](https://github.com/user-attachments/assets/6b6278d0-ff46-45cc-9615-136418f7360f)

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
 ![Screenshot from 2024-08-31 01-12-43](https://github.com/user-attachments/assets/0ace5f35-a3f8-417d-8744-9e6b59b17c0a)

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
![Screenshot from 2024-08-31 01-12-49](https://github.com/user-attachments/assets/34d395e5-d3b4-41ac-9fe7-ce7f7920bc5d)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![Screenshot from 2024-08-31 01-12-56](https://github.com/user-attachments/assets/3979881c-e9bd-4234-a88f-f0b0f35f1514)



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
 ![Screenshot from 2024-08-31 01-13-09](https://github.com/user-attachments/assets/8c402693-4650-4099-a7c3-f0cffe914eaa)

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
 ![Screenshot from 2024-08-31 01-13-15](https://github.com/user-attachments/assets/08011c6b-9635-444c-b7a8-264fbf296aaa)

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
 ![Screenshot from 2024-08-31 01-13-24](https://github.com/user-attachments/assets/c552d9b8-3551-46e3-8d44-3e2dc0d74e0e)

 
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
 ![Screenshot from 2024-08-31 01-13-34](https://github.com/user-attachments/assets/c9942fa4-0d2b-47e9-93a5-803c9c135460)

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
![Screenshot from 2024-08-31 01-13-47](https://github.com/user-attachments/assets/19f0c21b-2b61-4823-a50e-f852858b39f0)


# RESULT:
The Commands are executed successfully.

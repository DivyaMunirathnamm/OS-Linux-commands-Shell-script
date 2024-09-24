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
s.n.da
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
## OUTPUT.

![366726041-9b6b191e-5d33-4d2c-9d98-e70ed823436a](https://github.com/user-attachments/assets/597b5c89-22dd-46cf-96ce-ecb15c24a9c6)



cat < file2
## OUTPUT

![366725981-83fe3a09-0b9b-4f6b-8f4d-03192d059997](https://github.com/user-attachments/assets/2084183a-7163-4b4a-89c7-f5443d80d3f6)


# Comparing Files
cmp file1 file2
## OUTPUT
![366726177-fa28ef8b-864e-4ba2-a9cb-cf2bcae5bd16](https://github.com/user-attachments/assets/30952f01-d061-4b41-b386-cd27c26100bc)


comm file1 file2
 ## OUTPUT
![366726133-6a14df2d-d139-42d9-98cc-41694d5a2efd](https://github.com/user-attachments/assets/cffffafc-6c67-4220-9d2c-0c45071b73ad)


diff file1 file2
## OUTPUT

![366726354-bf116106-56bd-44ea-8247-928a28baf415](https://github.com/user-attachments/assets/202dfab6-21c5-4ebf-b938-066f997ab79d)

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


![366726523-93e51f30-1b07-428c-a41d-44e22fbbe020](https://github.com/user-attachments/assets/b5ba31ef-bba4-47eb-a916-a8b7e9248454)



cut -d "|" -f 1 file22
## OUTPUT

![366726572-a2d8c8d0-5987-40c2-add7-6fd8d64ec330](https://github.com/user-attachments/assets/2d7a13ff-329b-47b8-a8dd-7ccd7a831428)


cut -d "|" -f 2 file22
## OUTPUT
![366726650-a02c0b0c-3404-4cb8-bd57-d56fbf42ea48](https://github.com/user-attachments/assets/08dd95f9-6bc3-4623-a8af-2d893079e107)



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

![366726692-b35a6efc-93ad-4979-98df-e01718a7a64a](https://github.com/user-attachments/assets/80662f07-c619-4f97-8455-9cea5f2da9be)

grep hello newfile 
## OUTPUT

![366726738-6a407188-82af-432b-a9fe-1cf2ce499802](https://github.com/user-attachments/assets/fde8236b-0b9e-48ea-a6c6-eb182db33a5a)


grep -v hello newfile 
## OUTPUT

![366726771-a365b161-2217-41c8-9eae-9fbc574bc1f9](https://github.com/user-attachments/assets/9ffd04ec-3d11-4076-af66-f821194f43bb)

cat newfile | grep -i "hello"
## OUTPUT
![366726824-979fb40a-3ed6-4590-98d1-f86e2c822821](https://github.com/user-attachments/assets/d332fd2c-ab9c-4fc0-bdbd-ff7e3735ad77)


cat newfile | grep -i -c "hello"
## OUTPUT

![366726867-0963d6f9-0e02-40c2-9f9e-047e839f80d8](https://github.com/user-attachments/assets/d957b202-bf1e-41c0-9652-1e6885018593)

grep -R ubuntu /etc
## OUTPUT
![366727064-e2d4880b-af28-4a9f-822d-86dc517d88e4](https://github.com/user-attachments/assets/e8d884d2-030a-49b1-9117-3ff160232b88)

grep -w -n world newfile   
## OUTPUT
![366727131-8d321a17-df92-4f24-93ce-e729029d6c63](https://github.com/user-attachments/assets/cb4d45d1-284d-4ee6-9bd9-2c8060b7b8cc)


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
![366727200-14ac5520-e6fa-48cc-8343-c2e45c509519](https://github.com/user-attachments/assets/978170df-b710-4204-9f97-2fe250582251)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![366727234-bf8d99fa-9fa5-4857-8e20-892a06d23725](https://github.com/user-attachments/assets/cc743417-d07b-4313-829e-b3eb76ae4482)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![366727264-2a20ff34-f61a-4d63-af01-9c8553669e06](https://github.com/user-attachments/assets/384dc944-e14d-42ef-b9b8-ef102b149d1f)



egrep '(^hello)' newfile 
## OUTPUT

![366727305-fff7f5d7-19d5-4319-8757-f9c1aafc611b](https://github.com/user-attachments/assets/a761cbe0-977f-42a5-9711-55c23dc57f59)


egrep '(world$)' newfile 
## OUTPUT

![366727343-a97445d9-07bd-441e-88f4-70aa7058237f](https://github.com/user-attachments/assets/7c7166db-367c-49da-91f5-a509697a3b8b)


egrep '(World$)' newfile 
## OUTPUT
![366727343-a97445d9-07bd-441e-88f4-70aa7058237f](https://github.com/user-attachments/assets/531067d6-1ca0-4cc8-b46b-05a79a4dc4ad)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![366727410-b229e3fd-479d-45f5-a7b7-619d7a3b1436](https://github.com/user-attachments/assets/76b4e121-a36e-4eae-b96d-b4256cdc8721)


egrep '[1-9]' newfile 
## OUTPUT

![366727462-56e2a7f2-53d6-47e2-a729-541cd1a8aa1d](https://github.com/user-attachments/assets/e7a36e91-f8f6-4a15-9895-8a5e132de55b)


egrep 'Linux.*world' newfile 
## OUTPUT
![366727536-045b01ea-5885-483c-872f-d310a6be96a6](https://github.com/user-attachments/assets/f7be7f9c-a16b-4bd5-b691-65ac8fc182dd)


egrep 'Linux.*World' newfile 
## OUTPUT
![366727536-045b01ea-5885-483c-872f-d310a6be96a6](https://github.com/user-attachments/assets/6b08a443-0bb7-404a-a5e6-77215d046a74)


egrep l{2} newfile
## OUTPUT

![366727695-84c53be3-af78-4073-a3d5-5701c819bb8b](https://github.com/user-attachments/assets/25fd9619-0034-489a-8072-20b1dc516309)


egrep 's{1,2}' newfile
## OUTPUT 
![366727734-c6aee395-7976-4d29-8e86-81dfc9a1049a](https://github.com/user-attachments/assets/41b8c77c-b941-4386-8cd9-d5f380caa5ca)


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
![366727791-b6cabca1-3a4a-44d7-82b5-6b39ae91b951](https://github.com/user-attachments/assets/c7bf3a5c-6f31-4396-af04-97f5bfa8b272)



sed -n -e '$p' file23
## OUTPUT

![366727823-a667993a-03f9-44d6-b462-79d7fc96f17c](https://github.com/user-attachments/assets/088023b1-2de9-4784-a5e8-f68202871d20)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/785fea5f-89a5-4170-84bc-653d92d43d85)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![366727940-efb8d016-6b53-4ff8-8bfb-c1addec0262a](https://github.com/user-attachments/assets/f4370443-5e37-401e-950a-ab32c546a4f9)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![366727958-a0e98077-4a95-4c38-b427-b2a8e17d055e](https://github.com/user-attachments/assets/ca1ccd7b-4db9-421d-83cf-ce8d2cab658a)


sed -n -e '1,5p' file23
## OUTPUT

![366728002-0cbb6a1d-400c-4ada-8ca3-e16827877f5c](https://github.com/user-attachments/assets/ccc5c432-54bc-4a03-a476-ae8edfb6c31b)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![366728031-b23b38e6-4547-4928-8e73-a937a15bfe22](https://github.com/user-attachments/assets/be60705c-2d15-43d5-a19b-32a7296ff6dd)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![366728061-e055e93a-21af-421b-a7c6-528b7ecb57fd](https://github.com/user-attachments/assets/e8201c8f-16df-404e-bfdb-9505cdab0ea8)


seq 10 
## OUTPUT
![366728106-3e0340a0-2cc9-4770-ba6a-c4c0ad60c2a5](https://github.com/user-attachments/assets/a4c542d7-0f46-4d6a-b4f6-be62dbb19844)



seq 10 | sed -n '4,6p'
## OUTPUT

![366728122-ad838537-8589-4faa-b46c-82cb7c216bcd](https://github.com/user-attachments/assets/9a8791d4-f523-4540-9984-25850016f098)


seq 10 | sed -n '2,~4p'
## OUTPUT

![366728170-66a977f8-9955-402d-9a30-6d976f5b2139](https://github.com/user-attachments/assets/5dab593a-2ddd-4258-ae8a-c78d0d73bfa6)


seq 3 | sed '2a hello'
## OUTPUT
![366728222-65b7ca6a-3726-4a8c-981e-a45965b73583](https://github.com/user-attachments/assets/bd56fd0e-c4a1-494a-949b-ecdc495b7e3b)



seq 2 | sed '2i hello'
## OUTPUT

![366728260-eca581ee-412b-4043-9f5f-f277a3aee77a](https://github.com/user-attachments/assets/e08a0b76-43d7-4f08-8a18-0a87af358400)

seq 10 | sed '2,9c hello'
## OUTPUT
![366728311-9dae29fa-ba1d-40d2-abd8-5a80745a9791](https://github.com/user-attachments/assets/a81727ab-4b40-4677-9209-3ccbb8fb0987)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![366728491-a4cae7c3-7f2b-48bc-acf0-fa950705c447](https://github.com/user-attachments/assets/faf2e9f7-8ab4-4200-a3ac-318011b9682a)


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
![366728599-3cfe1443-24bf-46c7-b161-73ccbaf820be](https://github.com/user-attachments/assets/b4392c86-82a0-4cb8-9578-3ec71c87151b)


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

![366729029-86516f0a-566e-43cc-800f-e56b92d07a70](https://github.com/user-attachments/assets/8d9e8b72-8230-4dca-9973-dbd71b6ec5dd)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![366729029-86516f0a-566e-43cc-800f-e56b92d07a70](https://github.com/user-attachments/assets/9d5b0bd5-fa83-4c19-a7cf-3ff37666a8fd)

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

![366729098-70810c4e-49b7-4d8c-81ef-89f2a01c92b0](https://github.com/user-attachments/assets/f9071865-280d-4ad6-a83b-e43d73f6e635)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![366729135-9d6f9dcb-36f8-4341-a293-59ed906ca269](https://github.com/user-attachments/assets/caec1a3f-0fe9-4119-8b1a-5458c2862156)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![366729209-5295562f-80fb-44f7-b764-75e8864b4da6](https://github.com/user-attachments/assets/606f76c0-7793-418b-9408-33971f681475)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![366729279-cc21b39a-cd83-4caf-8255-939987d45ff8](https://github.com/user-attachments/assets/3a294dd2-5af3-4a49-b55e-f99e57d4925a)


tar -xvf backup.tar
## OUTPUT
![366729353-e58670c5-3268-40a5-8b42-180b66ebd770](https://github.com/user-attachments/assets/4609c4bd-dc93-4a77-8e67-ba2972891464)

gzip backup.tar

ls .gz
## OUTPUT
 ![366729430-b14968ae-f110-437b-a52c-2ca9a6300890](https://github.com/user-attachments/assets/47f006bc-41b3-46a0-a9ce-bf57921c5f98)

gunzip backup.tar.gz
## OUTPUT

 ![366729573-59ab69b8-ccd7-4e9f-b62b-858c3f6ae774](https://github.com/user-attachments/assets/bfa5f9b2-cf67-4758-b6ae-78b254628381)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![366729652-4ef16237-7254-4df2-9867-1ae5331b6134](https://github.com/user-attachments/assets/9028a3e7-09d4-4826-9711-cc7c1358180e)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![366729690-1a8de362-6a5d-482d-9259-b9eb1c84a762](https://github.com/user-attachments/assets/a1fa18b3-e93d-41f7-b53e-c80b48bf4bd7)


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
![366729745-17e573a4-34d6-49bc-a9c4-5e974444aabf](https://github.com/user-attachments/assets/4630de64-b17f-403c-a136-d349e997b62d)

 
ls file1
## OUTPUT
![366729790-4abe4551-6047-4a42-b8e4-5c5bdc40b15e](https://github.com/user-attachments/assets/9c1c5a98-1c88-4f63-acda-a3941e2e8724)

echo $?
## OUTPUT 


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

![366729930-4701bf55-db51-4626-976b-3156bee77473](https://github.com/user-attachments/assets/85477858-72f1-401f-a50b-6ee3a58bee38)

 
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

![366729995-af119fdc-e30c-4aba-80c1-34091dd3ee9c](https://github.com/user-attachments/assets/a8f1b6fc-9948-4888-b678-7c9e5a16bac3)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![366730203-665c7e4f-0456-4ad3-876b-fe5abb958866](https://github.com/user-attachments/assets/11a32e51-8865-42bb-85a0-770b3789856a)


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
![366730254-477a039d-918a-4e80-a2f2-be60cc8fa6e7](https://github.com/user-attachments/assets/1174d68f-91b5-4131-979a-8dcf55945ea2)

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

![366730337-ac167094-5f53-4608-96f8-3cf93d186549](https://github.com/user-attachments/assets/28783638-8466-4e7d-b88b-bb4fa72b67ca)


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
![366730337-ac167094-5f53-4608-96f8-3cf93d186549](https://github.com/user-attachments/assets/49dc1ac1-a61f-4b37-b8fd-2d795b495523)

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
![366730508-e3b2f6a0-ece2-4068-93ba-f6e8749e9ec6](https://github.com/user-attachments/assets/8c6fc40e-8579-4a5c-a59a-43808784b80a)

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

![366730579-a6089fb6-9a2a-4ca5-9884-8829d6de5597](https://github.com/user-attachments/assets/0a965529-d98c-423b-8edb-a7fb2d0fd29b)


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
![366730615-9b071521-d320-4ca5-89f4-dff7851eeb48](https://github.com/user-attachments/assets/c5dd1c54-ddfa-49b8-9f06-abc66039b54a)


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

![366731148-8be65f7c-5561-42b4-82df-3bd50b8e760f](https://github.com/user-attachments/assets/a9a02c16-8f44-4912-8429-f06e02381141)

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

![366731347-72f4749d-81b5-45b6-825d-656d487aa6c5](https://github.com/user-attachments/assets/a581d9af-26d1-4fff-b0e0-0123c5b4b5b3)

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
![366731347-72f4749d-81b5-45b6-825d-656d487aa6c5](https://github.com/user-attachments/assets/dcf0fcbe-77a2-4702-8093-e9808058f67b)

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
![366731406-afb0b997-c4bd-4e0f-83ed-e0a093ec65c0](https://github.com/user-attachments/assets/8f8cee6b-d0bc-43a1-9c9b-03a7e1e2fd63)

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
![366731347-72f4749d-81b5-45b6-825d-656d487aa6c5](https://github.com/user-attachments/assets/ef48bf6f-e809-4ee8-ba93-a2572017a2d8)

 
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
![366731406-afb0b997-c4bd-4e0f-83ed-e0a093ec65c0](https://github.com/user-attachments/assets/360f1a97-4b28-4d2a-a6b0-5c31ed8067cf)

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
 ![366731754-0ace5f35-a3f8-417d-8744-9e6b59b17c0a](https://github.com/user-attachments/assets/190f581b-b89f-40d8-866b-57c3cf509233)

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
![368693722-34d395e5-d3b4-41ac-9fe7-ce7f7920bc5d](https://github.com/user-attachments/assets/a69222a7-41d7-4afb-8481-066e7d0400d0)



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
## OUTPUT.
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
 ![368693892-8c402693-4650-4099-a7c3-f0cffe914eaa](https://github.com/user-attachments/assets/09c5e6a3-239d-4f40-80e4-26ad38e934da)

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
 ![368693961-08011c6b-9635-444c-b7a8-264fbf296aaa](https://github.com/user-attachments/assets/612ea892-4494-433d-a834-c187f95e1151)

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

![368694004-c552d9b8-3551-46e3-8d44-3e2dc0d74e0e](https://github.com/user-attachments/assets/d62b0c59-a9f7-4e05-86cd-c25f51645177)

 
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
 ![368694035-c9942fa4-0d2b-47e9-93a5-803c9c135460](https://github.com/user-attachments/assets/c92753e5-c24f-4736-b20a-8ed85bfdaeff)

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
![368694098-19f0c21b-2b61-4823-a50e-f852858b39f0](https://github.com/user-attachments/assets/378f9ac8-e25b-47cb-af40-7c43e8bf4c18)


# RESULT:
The Commands are executed successfully.

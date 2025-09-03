NAME: GOPIKA A

REG NO: 212224100017

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

cat < file2
## OUTPUT
<img width="728" height="306" alt="image" src="https://github.com/user-attachments/assets/36fc9ba4-b817-439a-9099-f69f8664bba0" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="798" height="56" alt="image" src="https://github.com/user-attachments/assets/ef5c9cac-4320-4d8a-b804-7791bfc93db6" />

comm file1 file2
## OUTPUT
<img width="760" height="327" alt="image" src="https://github.com/user-attachments/assets/759387d3-6cf5-4cfd-a7bb-45f9b1623d5e" />

 
diff file1 file2
## OUTPUT
<img width="772" height="234" alt="image" src="https://github.com/user-attachments/assets/9c92313b-a80a-48c4-bc9d-657990475cf5" />


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

<img width="768" height="98" alt="image" src="https://github.com/user-attachments/assets/9f57147f-5f61-48d4-85d2-dd2e5ff06434" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="836" height="116" alt="image" src="https://github.com/user-attachments/assets/2a61e0fb-64dd-4ecc-be02-5d100f360ac9" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="842" height="119" alt="image" src="https://github.com/user-attachments/assets/63ec6ca6-78ad-4b93-bc2a-1cdeab451a82" />


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
<img width="817" height="49" alt="image" src="https://github.com/user-attachments/assets/b5eae0a4-23c3-44f2-8945-48fb8602d882" />



grep hello newfile 
## OUTPUT
<img width="786" height="54" alt="image" src="https://github.com/user-attachments/assets/47937302-0211-46b8-a2a4-5adf8e69d5b3" />




grep -v hello newfile 
## OUTPUT

<img width="836" height="47" alt="image" src="https://github.com/user-attachments/assets/a417340d-add9-40ad-8473-9315e027298b" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="916" height="50" alt="image" src="https://github.com/user-attachments/assets/7e621d2b-e0f7-4a3e-83af-19b5c40ac282" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="955" height="48" alt="image" src="https://github.com/user-attachments/assets/88b1fc8b-4e6c-4d4a-b7c2-f8abdf520f35" />




grep -R ubuntu /etc
## OUTPUT

<img width="1027" height="862" alt="image" src="https://github.com/user-attachments/assets/481df47b-8a79-47ac-a440-cd69e448bec0" />


grep -w -n world newfile   
## OUTPUT
<img width="733" height="41" alt="image" src="https://github.com/user-attachments/assets/d387ba0d-f943-49d4-bf81-8ab511e42961" />


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

<img width="932" height="73" alt="image" src="https://github.com/user-attachments/assets/94b63c1c-fe55-4d74-98b7-36db833a0d06" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="906" height="74" alt="image" src="https://github.com/user-attachments/assets/27328d18-7223-4ca2-81bb-9b7deb927a3f" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="940" height="71" alt="image" src="https://github.com/user-attachments/assets/9b06b7f3-f992-44e7-b0af-f46c65ab5fb5" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="858" height="49" alt="image" src="https://github.com/user-attachments/assets/a37aa5b0-e94f-4ce4-9f79-af1b1f3fb901" />



egrep '(world$)' newfile 
## OUTPUT
<img width="861" height="76" alt="image" src="https://github.com/user-attachments/assets/2e9accf9-d869-4226-ba71-d94f460643e0" />



egrep '(World$)' newfile 
## OUTPUT
-<img width="872" height="53" alt="image" src="https://github.com/user-attachments/assets/47b9cc2b-fb7a-42ea-8f57-3b3d7669d725" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="935" height="96" alt="image" src="https://github.com/user-attachments/assets/d7ea9146-1dd3-4783-8e4a-c83e05095ff7" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="845" height="52" alt="image" src="https://github.com/user-attachments/assets/26985069-303e-414a-839b-5437446bb59c" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="923" height="49" alt="image" src="https://github.com/user-attachments/assets/c2490f34-52b4-4ee9-bd8a-2f0b2b86f7bf" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="911" height="49" alt="image" src="https://github.com/user-attachments/assets/61b4f74d-d47a-4814-8afc-b3dcc6e4f896" />


egrep l{2} newfile
## OUTPUT
<img width="789" height="75" alt="image" src="https://github.com/user-attachments/assets/9b8a5fba-fd6f-4558-9171-9b9e2e546c63" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="857" height="98" alt="image" src="https://github.com/user-attachments/assets/0973b89b-88e7-478f-a254-affe9677b82e" />


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

<img width="823" height="47" alt="image" src="https://github.com/user-attachments/assets/5d6c2c93-127e-41d8-8aac-98c9e7d1903e" />


sed -n -e '$p' file23
## OUTPUT
<img width="821" height="48" alt="image" src="https://github.com/user-attachments/assets/d6143aaf-6a9b-4258-8006-e728e27b0568" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="891" height="231" alt="image" src="https://github.com/user-attachments/assets/ab786e02-c7ea-4b90-b0db-bd5d53ea6e7c" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="915" height="225" alt="image" src="https://github.com/user-attachments/assets/f3eb7f92-1d4d-41aa-8d58-4f3d68480e41" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="932" height="236" alt="image" src="https://github.com/user-attachments/assets/7593c9ae-dbbd-4183-9903-abedbc26e937" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="853" height="139" alt="image" src="https://github.com/user-attachments/assets/6c1e1872-2c12-45cb-866b-34d2dcc8d184" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="894" height="95" alt="image" src="https://github.com/user-attachments/assets/cafc9116-1a78-45a7-bce2-523899a6b302" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="957" height="69" alt="image" src="https://github.com/user-attachments/assets/272c8e89-134d-4354-b58f-e848f12c593c" />


seq 10 
## OUTPUT
<img width="662" height="246" alt="image" src="https://github.com/user-attachments/assets/8fbf8636-3c3b-4d3e-988e-dac7ce7bbea2" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="848" height="85" alt="image" src="https://github.com/user-attachments/assets/43d74060-8191-4ab6-b88c-ad2bb66528da" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="845" height="90" alt="image" src="https://github.com/user-attachments/assets/2c97f607-dc9c-4a88-95e1-9f1fd2cf9b2c" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="841" height="115" alt="image" src="https://github.com/user-attachments/assets/5e66c48f-4144-4edb-b553-acabf94f0f38" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="832" height="99" alt="image" src="https://github.com/user-attachments/assets/fe5ebe1f-f6d5-4aca-91e8-c93f1aac9069" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="886" height="93" alt="image" src="https://github.com/user-attachments/assets/7e9968d3-64a7-4be5-aa56-148acff70c7b" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="954" height="88" alt="image" src="https://github.com/user-attachments/assets/2d7060d1-4ff1-4078-96a9-7fadecf08cda" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="935" height="100" alt="image" src="https://github.com/user-attachments/assets/62525479-d10e-40fc-844e-69f719bc92f9" />


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

<img width="711" height="139" alt="image" src="https://github.com/user-attachments/assets/50a37338-746b-4eb2-8f74-3311b88217e4" />

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
<img width="701" height="140" alt="image" src="https://github.com/user-attachments/assets/82dc391d-c0ff-4819-92f2-0ab893bfb3ce" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT

<img width="990" height="212" alt="image" src="https://github.com/user-attachments/assets/84dd3527-1aef-4247-94e2-1760ee828c23" />

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

<img width="928" height="96" alt="image" src="https://github.com/user-attachments/assets/f97e3563-cb1a-42c5-a696-04336bb06885" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1041" height="96" alt="image" src="https://github.com/user-attachments/assets/3ed92d98-f02d-4b5c-bb54-75869f6989da" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
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
<img width="775" height="55" alt="image" src="https://github.com/user-attachments/assets/71dc68fa-aa72-48bb-abc2-d3bd05f92319" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="796" height="97" alt="image" src="https://github.com/user-attachments/assets/7f7fa1dc-4300-4d4a-80a1-3a13483738db" />


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
<img width="812" height="395" alt="image" src="https://github.com/user-attachments/assets/e87b4b3e-4053-447e-84dc-6b1cee9da12d" />

 
ls file1
## OUTPUT
<img width="691" height="44" alt="image" src="https://github.com/user-attachments/assets/57995a6d-eb01-4bf2-9d9a-fb56e99e1764" />

echo $?
## OUTPUT 
<img width="657" height="47" alt="image" src="https://github.com/user-attachments/assets/d2c779c9-cdee-4e9c-981f-c9a1589ff156" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
## OUTPUT

<img width="657" height="47" alt="image" src="https://github.com/user-attachments/assets/d8b3d1bb-47a0-499d-b6a7-dc8d55a18080" />

 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="803" height="99" alt="image" src="https://github.com/user-attachments/assets/86647e51-da22-49de-ab90-5e676422f984" />


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
<img width="807" height="101" alt="image" src="https://github.com/user-attachments/assets/16944b49-970d-4f54-bb8d-7419069aa21d" />

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
<img width="738" height="137" alt="image" src="https://github.com/user-attachments/assets/aacefc29-8808-4b17-a6b1-4bb870bbbe64" />



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
<img width="801" height="122" alt="image" src="https://github.com/user-attachments/assets/c9655846-4768-4f25-b860-806c8c1c78db" />

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
<img width="757" height="145" alt="image" src="https://github.com/user-attachments/assets/988fb782-7289-40a2-b107-519cdcf86ef9" />

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

<img width="810" height="73" alt="image" src="https://github.com/user-attachments/assets/fc251150-5444-4b5f-916f-f4998599ecb0" />

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
<img width="853" height="70" alt="image" src="https://github.com/user-attachments/assets/99f99f1c-b6cc-47d2-bfd8-1dfcfcc24ee2" />

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

## OUTPUT
<img width="751" height="49" alt="image" src="https://github.com/user-attachments/assets/97384d9c-c842-48b4-82a0-179c72d49936" />

 
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
$ ./forin2.sh 
## OUTPUT

<img width="717" height="169" alt="image" src="https://github.com/user-attachments/assets/e6a56e97-d8f2-4241-9f1f-ec6e2aaf17a6" />

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

## OUTPUT
<img width="716" height="90" alt="image" src="https://github.com/user-attachments/assets/a82fdc99-8e8b-4b40-a533-3fb218e67e8a" />

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
## OUTPUT
<img width="723" height="160" alt="image" src="https://github.com/user-attachments/assets/18c9fb09-71ec-48b8-9a11-a8b503f48879" />

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
<img width="847" height="324" alt="image" src="https://github.com/user-attachments/assets/f2d9ec45-a7f9-4495-b2b8-7b9535737b4a" />


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
<img width="772" height="145" alt="image" src="https://github.com/user-attachments/assets/05f99366-2925-4e27-a920-3a09aa181093" />

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
<img width="754" height="148" alt="image" src="https://github.com/user-attachments/assets/3dcf2ac1-3f8d-48fb-8e0b-04b0f530873c" />

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
<img width="791" height="304" alt="image" src="https://github.com/user-attachments/assets/deec8cb6-9d5f-4c41-aa6b-2b52379df67f" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
<img width="878" height="106" alt="image" src="https://github.com/user-attachments/assets/63841084-df44-402b-beda-e34e358779fc" />


cat forcontinue.sh 
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
<img width="951" height="142" alt="image" src="https://github.com/user-attachments/assets/a523768a-ecd2-4eb0-9e56-b039fa0c85c4" />

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
<img width="754" height="75" alt="image" src="https://github.com/user-attachments/assets/8d2092b8-6831-4691-aa6c-19bb9f978715" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
```
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT

<img width="831" height="80" alt="image" src="https://github.com/user-attachments/assets/f2a00bd5-0a6e-489d-9b36-6fcc3e8dfc7a" />

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
 
<img width="769" height="102" alt="image" src="https://github.com/user-attachments/assets/c7da56d5-a6e9-4066-a89f-0f1993293ad8" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="823" height="96" alt="image" src="https://github.com/user-attachments/assets/e6f3c706-a804-4941-90e9-4a1270b0ff8e" />


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
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="804" height="103" alt="image" src="https://github.com/user-attachments/assets/360c1101-6a5b-4e95-9399-bccf5b4f760a" />

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
 
<img width="783" height="348" alt="image" src="https://github.com/user-attachments/assets/4287ef7d-cf37-482d-bae6-acafe1260004" />

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
<img width="899" height="328" alt="image" src="https://github.com/user-attachments/assets/07f74a77-db69-40c0-a0ba-c1dc13e6faa7" />

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

<img width="836" height="550" alt="image" src="https://github.com/user-attachments/assets/cf979ebc-9e77-4e7f-b2b9-d7e5be220a38" />

# RESULT:
The Commands are executed successfully.

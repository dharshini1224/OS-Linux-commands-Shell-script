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

<img width="439" height="151" alt="image" src="https://github.com/user-attachments/assets/b57213bc-70cd-49a5-953a-8b4c5e21d80c" />



cat < file2
## OUTPUT

<img width="495" height="179" alt="image" src="https://github.com/user-attachments/assets/db067188-13fe-4542-87c5-d7e88027dc72" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="453" height="75" alt="image" src="https://github.com/user-attachments/assets/166b0fd7-0762-4228-9e6b-5f0a205918cb" />

 
comm file1 file2
 ## OUTPUT

 <img width="390" height="402" alt="image" src="https://github.com/user-attachments/assets/b928350e-2463-47b7-bd24-b4670bbfcbc9" />



 
diff file1 file2
## OUTPUT
<img width="307" height="359" alt="image" src="https://github.com/user-attachments/assets/f06e328a-1754-4aa2-94db-a230335fbedc" />




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

<img width="300" height="135" alt="image" src="https://github.com/user-attachments/assets/2d66f228-cd9b-403d-831a-193db4b1d0f2" />





cut -d "|" -f 1 file22
## OUTPUT

<img width="291" height="160" alt="image" src="https://github.com/user-attachments/assets/ee14a542-5763-4d17-a1d6-1661e339296b" />




cut -d "|" -f 2 file22
## OUTPUT

<img width="303" height="163" alt="image" src="https://github.com/user-attachments/assets/5458f95e-77eb-476f-9c22-69fd157659b2" />




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
<img width="295" height="62" alt="image" src="https://github.com/user-attachments/assets/4badf7b3-d65e-4081-adb2-bc36d73d8df3" />




grep hello newfile 
## OUTPUT

<img width="271" height="102" alt="image" src="https://github.com/user-attachments/assets/ddc765fc-78f6-4042-84e1-fbe0d52d1c71" />





grep -v hello newfile 
## OUTPUT

<img width="288" height="84" alt="image" src="https://github.com/user-attachments/assets/e5929007-f52f-4ba3-bb99-767999fdfeb6" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="379" height="101" alt="image" src="https://github.com/user-attachments/assets/c4aa3883-7037-451c-a6a0-d6927dd78b22" />





cat newfile | grep -i -c "hello"
## OUTPUT

<img width="399" height="80" alt="image" src="https://github.com/user-attachments/assets/bd18d752-c32b-44cc-9be4-2e2791449a38" />





grep -R ubuntu /etc
## OUTPUT

<img width="850" height="503" alt="image" src="https://github.com/user-attachments/assets/b6aa5d38-af93-466d-9360-e3f24c721c60" />

<img width="852" height="600" alt="image" src="https://github.com/user-attachments/assets/6535e433-d9b1-4ee7-ac6f-e191a55b3576" />




grep -w -n world newfile   
## OUTPUT

<img width="310" height="109" alt="image" src="https://github.com/user-attachments/assets/326223e7-c246-4b63-aab0-b56333e6f102" />



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

<img width="330" height="206" alt="image" src="https://github.com/user-attachments/assets/a81978e2-72e5-4b04-8f2e-853be0e63822" />




egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="375" height="103" alt="image" src="https://github.com/user-attachments/assets/f77e6aec-b42f-40e1-8076-794aa2aca4a2" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="359" height="110" alt="image" src="https://github.com/user-attachments/assets/5eea84cb-4477-47b7-8773-f815423ab9dc" />





egrep '(^hello)' newfile 
## OUTPUT

<img width="406" height="117" alt="image" src="https://github.com/user-attachments/assets/54960b88-e6d9-4d7c-8540-4788826cc37b" />




egrep '(world$)' newfile 
## OUTPUT

<img width="322" height="79" alt="image" src="https://github.com/user-attachments/assets/3a09b9a3-37ae-498c-a2ea-3b22d88b0893" />



egrep '(World$)' newfile 
## OUTPUT

<img width="331" height="101" alt="image" src="https://github.com/user-attachments/assets/f1a5f251-6271-4880-8b28-b7db717c0e41" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="367" height="152" alt="image" src="https://github.com/user-attachments/assets/8b9e6b8e-dd41-4def-8907-522472de77ab" />




egrep '[1-9]' newfile 
## OUTPUT

<img width="300" height="85" alt="image" src="https://github.com/user-attachments/assets/cfaf91b0-4226-468e-b013-5ed47a3240e6" />




egrep 'Linux.*world' newfile 
## OUTPUT

<img width="365" height="77" alt="image" src="https://github.com/user-attachments/assets/3e053aed-00f3-4043-a1d4-8a21aead84ff" />




egrep 'Linux.*World' newfile 
## OUTPUT

<img width="356" height="76" alt="image" src="https://github.com/user-attachments/assets/229ba547-9cb3-4e94-be96-d35cb4e9fe80" />



egrep l{2} newfile
## OUTPUT

<img width="276" height="103" alt="image" src="https://github.com/user-attachments/assets/cc9e6a44-6e29-4aea-b919-cc2bc8d5f20a" />




egrep 's{1,2}' newfile
## OUTPUT 

<img width="310" height="135" alt="image" src="https://github.com/user-attachments/assets/7cd754d8-15d9-4175-92e8-0a50c699647a" />



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

<img width="298" height="76" alt="image" src="https://github.com/user-attachments/assets/60f62874-3d0b-4c38-b0b5-60c1a2c74f46" />





sed -n -e '$p' file23
## OUTPUT

<img width="319" height="86" alt="image" src="https://github.com/user-attachments/assets/413a43f2-14c8-46fb-b81c-b3d6b72a0878" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="357" height="282" alt="image" src="https://github.com/user-attachments/assets/67d89bd3-e55c-409d-8d3a-c5285dca1b03" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="351" height="285" alt="image" src="https://github.com/user-attachments/assets/42bfa6ec-56b9-498b-b1df-3253101308d6" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="392" height="281" alt="image" src="https://github.com/user-attachments/assets/18322c6e-d9af-4893-b597-5409b4f7f9fe" />




sed -n -e '1,5p' file23
## OUTPUT

<img width="319" height="203" alt="image" src="https://github.com/user-attachments/assets/87c7b57f-6739-4cd5-a23b-b0bd4974874c" />




sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="355" height="133" alt="image" src="https://github.com/user-attachments/assets/f8220b09-e65b-4328-8458-269c3baf3670" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="391" height="105" alt="image" src="https://github.com/user-attachments/assets/236e234d-7ba2-4e16-a14c-6c53095e77e9" />








seq 10 | sed -n '4,6p'
## OUTPUT

<img width="315" height="119" alt="image" src="https://github.com/user-attachments/assets/5985d49a-064e-40ac-b43b-0db7e6dcf79a" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="310" height="126" alt="image" src="https://github.com/user-attachments/assets/8179f8fa-c742-47c9-a452-275d87bb83ce" />




seq 3 | sed '2a hello'
## OUTPUT

<img width="307" height="155" alt="image" src="https://github.com/user-attachments/assets/d6ad6cae-5b7f-474f-96a4-caa418463bfe" />




seq 2 | sed '2i hello'
## OUTPUT

<img width="304" height="119" alt="image" src="https://github.com/user-attachments/assets/190f7dc2-7b9d-4565-9315-6577db5482d7" />



seq 10 | sed '2,9c hello'
## OUTPUT

<img width="330" height="132" alt="image" src="https://github.com/user-attachments/assets/568b3d03-cf4f-44e6-b3e4-9aa777f68c31" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="369" height="131" alt="image" src="https://github.com/user-attachments/assets/1095d770-6be1-4bed-9644-6cffd7ce643e" />



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

<img width="313" height="405" alt="image" src="https://github.com/user-attachments/assets/44ca604b-dba5-44e2-9351-8ffbdacc9942" />



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

<img width="325" height="422" alt="image" src="https://github.com/user-attachments/assets/7dcc3da4-099e-4e58-9074-e06ef8aa2143" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="428" height="278" alt="image" src="https://github.com/user-attachments/assets/2806f10b-0fa8-4cd7-8944-2830e143ba8d" />


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

 <img width="329" height="312" alt="image" src="https://github.com/user-attachments/assets/4330e1be-8fe0-47e1-aa3e-d57cf96e0525" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="350" height="135" alt="image" src="https://github.com/user-attachments/assets/48d33f15-9807-45f7-8a37-b0df9d563d00" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="832" height="579" alt="image" src="https://github.com/user-attachments/assets/4e6fc9a7-fb8b-4410-bda0-b7a9cf6146cc" />





mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="832" height="579" alt="image" src="https://github.com/user-attachments/assets/f6915ca0-d09b-412e-835f-6dd360d8279d" />



tar -xvf backup.tar
## OUTPUT

<img width="548" height="714" alt="image" src="https://github.com/user-attachments/assets/e81efe6e-8261-4fea-885e-ab0a0106bc56" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="396" height="51" alt="image" src="https://github.com/user-attachments/assets/51e9962b-afab-4b92-836d-487df0d93ffc" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="371" height="352" alt="image" src="https://github.com/user-attachments/assets/b94450cc-8224-468e-a4a8-8799a489bfde" />



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

<img width="264" height="70" alt="image" src="https://github.com/user-attachments/assets/898f8942-dc4e-4d6d-9893-827cdbcd96b8" />




 
ls file1
## OUTPUT

<img width="296" height="88" alt="image" src="https://github.com/user-attachments/assets/738e1bbd-cb1d-4671-a5df-9ec34e813139" />


echo $?
## OUTPUT 

<img width="274" height="82" alt="image" src="https://github.com/user-attachments/assets/18ed24b9-28d3-4c36-98f8-b18d37af1197" />




 
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

<img width="347" height="303" alt="image" src="https://github.com/user-attachments/assets/98db1652-14f1-40a7-ad8b-b7693d771c5b" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="369" height="112" alt="image" src="https://github.com/user-attachments/assets/2b1082df-4d46-4b6e-b1ad-4f139831cc75" />



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

<img width="646" height="128" alt="image" src="https://github.com/user-attachments/assets/3ae14f50-5bef-4fb8-bc9d-108dc742f2f2" />


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

<img width="413" height="176" alt="image" src="https://github.com/user-attachments/assets/cd841f8a-67ba-4669-b116-1c11e2ca58d5" />



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

## output

<img width="358" height="152" alt="image" src="https://github.com/user-attachments/assets/d50fd929-7a62-4d5e-b0c7-6e3232643f6f" />

 
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

## output 

<img width="555" height="470" alt="image" src="https://github.com/user-attachments/assets/0ca64b77-e0a7-4b12-b4d7-69a5f6fe86e8" />

 
 
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

<img width="434" height="177" alt="image" src="https://github.com/user-attachments/assets/ade44b1c-6850-4b41-834f-165556b1747a" />

 
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

<img width="512" height="202" alt="image" src="https://github.com/user-attachments/assets/eb1db0c2-8e01-437a-8e10-fd328a4fd3d5" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 





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

<img width="332" height="227" alt="image" src="https://github.com/user-attachments/assets/c24a1beb-0188-4f2c-9dfe-f8d3fd666c56" />

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

<img width="344" height="203" alt="image" src="https://github.com/user-attachments/assets/fac34b2b-83c3-4dd7-a1ec-adeea314182f" />

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

<img width="407" height="508" alt="image" src="https://github.com/user-attachments/assets/35b97044-a380-404f-a3b9-848b410e3bd1" />

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

<img width="315" height="413" alt="image" src="https://github.com/user-attachments/assets/b9e2567f-8db0-4aae-8452-10843f00a29d" />

 
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

<img width="333" height="352" alt="image" src="https://github.com/user-attachments/assets/36569308-c1c9-4d5c-a86c-9e21fb1c11bc" />



# RESULT:
The Commands are executed successfully.

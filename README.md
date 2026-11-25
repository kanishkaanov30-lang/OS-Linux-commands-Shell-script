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
<img width="626" height="182" alt="image" src="https://github.com/user-attachments/assets/ed3ba678-37f4-468f-b9d4-6f69be87bccf" />



cat < file2
## OUTPUT
<img width="655" height="206" alt="image" src="https://github.com/user-attachments/assets/18f3f15d-7051-4087-925c-0722b67fea70" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="575" height="79" alt="image" src="https://github.com/user-attachments/assets/f9e745db-9250-4667-8eec-6f4e87cf627c" />

comm file1 file2
 ## OUTPUT
<img width="579" height="204" alt="image" src="https://github.com/user-attachments/assets/75a8cc94-ff1a-4e91-85b1-def03a7f4ee8" />

 
diff file1 file2
## OUTPUT
<img width="680" height="314" alt="image" src="https://github.com/user-attachments/assets/86cb0f40-a0aa-44b8-9258-826fe054a392" />


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
<img width="626" height="112" alt="image" src="https://github.com/user-attachments/assets/c5ed8b47-e306-418e-adcb-a44a15aa2a99" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="655" height="129" alt="image" src="https://github.com/user-attachments/assets/cee034fa-1382-45ce-95ca-a5aa2bffccc3" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="633" height="123" alt="image" src="https://github.com/user-attachments/assets/af21b15d-6036-4015-92e0-8b970c96dd3e" />


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
<img width="566" height="74" alt="image" src="https://github.com/user-attachments/assets/814a4082-28eb-43c5-be64-19e559ab282c" />



grep hello newfile 
## OUTPUT
<img width="566" height="74" alt="image" src="https://github.com/user-attachments/assets/0873dcbf-0044-49cf-a061-c6c239119bfa" />




grep -v hello newfile 
## OUTPUT
<img width="588" height="70" alt="image" src="https://github.com/user-attachments/assets/8fa7acb5-b6bf-4811-84bc-5060ba0c83c2" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="588" height="70" alt="image" src="https://github.com/user-attachments/assets/3918edb7-2d73-4dc6-ba0e-93a77faa4e17" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="573" height="74" alt="image" src="https://github.com/user-attachments/assets/e320668a-3ec6-4737-9c72-e75263bb0ea0" />



grep -R ubuntu /etc
## OUTPUT
<img width="804" height="590" alt="image" src="https://github.com/user-attachments/assets/8af86774-fb37-46cf-a181-60dfcae5430a" />



grep -w -n world newfile   
## OUTPUT
<img width="565" height="96" alt="image" src="https://github.com/user-attachments/assets/9ae6f126-bc9e-4599-81bb-3a27448cd13f" />


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
<img width="534" height="96" alt="image" src="https://github.com/user-attachments/assets/87ac9943-048e-4114-b112-72a6d7e10ea4" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="542" height="87" alt="image" src="https://github.com/user-attachments/assets/1b75a009-58c4-420f-9502-01cb0b6f222a" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="570" height="101" alt="image" src="https://github.com/user-attachments/assets/82c96f60-a1c9-49f3-92c6-caf3e2d4796b" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="570" height="101" alt="image" src="https://github.com/user-attachments/assets/3c8396e6-0ebb-4473-a99c-885dd251d993" />


egrep '(world$)' newfile 
## OUTPUT
<img width="553" height="68" alt="image" src="https://github.com/user-attachments/assets/a8fc3083-812b-4151-9fa3-1dcf9d86e2db" />



egrep '(World$)' newfile 
## OUTPUT
<img width="541" height="92" alt="image" src="https://github.com/user-attachments/assets/37c42846-beca-47e9-a2a1-a97d1cacdf63" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="614" height="127" alt="image" src="https://github.com/user-attachments/assets/04d55aa0-e70f-4c52-811f-9c2ee1dd5644" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="568" height="80" alt="image" src="https://github.com/user-attachments/assets/8e36f3c5-8eff-48d8-bc30-6daac306eb6b" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="513" height="66" alt="image" src="https://github.com/user-attachments/assets/634c90a5-cdcf-46f6-bc8c-a6606a8921c2" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="540" height="76" alt="image" src="https://github.com/user-attachments/assets/73cf19e4-8d8c-481d-ab58-54f890e4a632" />


egrep l{2} newfile
## OUTPUT
<img width="531" height="110" alt="image" src="https://github.com/user-attachments/assets/c7fe02ea-6065-4db6-8b2e-d87543f1b830" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="610" height="126" alt="image" src="https://github.com/user-attachments/assets/f3f8ca05-ce11-4e3d-8ea9-3a9fdeee6de1" />


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

<img width="573" height="73" alt="image" src="https://github.com/user-attachments/assets/e4523f33-75bd-4648-87dd-6510d7f21e11" />


sed -n -e '$p' file23
## OUTPUT
<img width="535" height="73" alt="image" src="https://github.com/user-attachments/assets/b1a75801-1fdf-4a11-be0f-45c5f4241bd9" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="542" height="268" alt="image" src="https://github.com/user-attachments/assets/7804538e-ca7d-44e7-a303-d809b0b84dd4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="550" height="272" alt="image" src="https://github.com/user-attachments/assets/b2392a5d-ea66-43c8-bd4e-c5cbf69634d1" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="541" height="283" alt="image" src="https://github.com/user-attachments/assets/3f05e083-3ed4-4c19-b30c-774294667bbf" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="543" height="177" alt="image" src="https://github.com/user-attachments/assets/b5701207-bfc6-4c9b-b289-8586f9546ead" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="537" height="125" alt="image" src="https://github.com/user-attachments/assets/88d2534a-5983-46ee-b107-49b4d6ba224d" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="527" height="103" alt="image" src="https://github.com/user-attachments/assets/398b4fb6-4eda-4943-a44f-3508fbfd6f4e" />



seq 10 
## OUTPUT
<img width="533" height="295" alt="image" src="https://github.com/user-attachments/assets/86e55bec-a0ff-444f-99f1-71caf19e4cfd" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="552" height="111" alt="image" src="https://github.com/user-attachments/assets/43d77151-db76-47f2-b011-9af54ea1086a" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="530" height="125" alt="image" src="https://github.com/user-attachments/assets/c3d53be4-c195-42c1-af33-9f193eef0be2" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="519" height="154" alt="image" src="https://github.com/user-attachments/assets/0b1bf05e-dbdd-49a3-bef4-3252f4756183" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="528" height="124" alt="image" src="https://github.com/user-attachments/assets/b84f64c8-0d6a-42e8-8d5f-555352a09550" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="587" height="129" alt="image" src="https://github.com/user-attachments/assets/b16c959c-0954-40d7-bfd9-9f82ab1662e9" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="524" height="125" alt="image" src="https://github.com/user-attachments/assets/ce86fff3-bdd6-4c96-8127-eda501a0a349" />



sed -n '2,4{s/$/*/;p}' file23
<img width="532" height="132" alt="image" src="https://github.com/user-attachments/assets/e9464b22-d253-42b5-a4ab-6acd38b514b5" />


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
<img width="598" height="146" alt="image" src="https://github.com/user-attachments/assets/d95f7013-6da5-479f-8014-260f4289a35d" />


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
<img width="572" height="157" alt="image" src="https://github.com/user-attachments/assets/db93b714-5eb0-4800-85cf-4c57d4fbc9da" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="555" height="274" alt="image" src="https://github.com/user-attachments/assets/b8789fda-cf96-4191-90d1-b31e4d9fdd75" />

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
<img width="521" height="135" alt="image" src="https://github.com/user-attachments/assets/ea12c748-039f-4ab0-9a31-97a5f63c4451" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="544" height="121" alt="image" src="https://github.com/user-attachments/assets/0c29ad55-7a00-42f6-b080-4afc0b790702" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="798" height="568" alt="image" src="https://github.com/user-attachments/assets/81980602-0c73-40af-8332-285b1335dad8" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="793" height="605" alt="image" src="https://github.com/user-attachments/assets/38e8b9a5-085b-4dfa-88e2-d2ee5348a961" />


tar -xvf backup.tar
## OUTPUT
<img width="784" height="565" alt="image" src="https://github.com/user-attachments/assets/11093ff4-0c98-46a8-a244-345aaa88d465" />

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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="419" height="125" alt="image" src="https://github.com/user-attachments/assets/48b51027-2984-4937-85c8-cc35b0db600b" />


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
<img width="548" height="72" alt="image" src="https://github.com/user-attachments/assets/2cd2e0b4-7a32-45ee-aadb-22a0604c4d7c" />

echo $?
## OUTPUT 

 
echo $?
## OUTPUT 
<img width="423" height="76" alt="image" src="https://github.com/user-attachments/assets/007c7b01-9f78-480d-bbec-3be5b7d0369f" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="423" height="76" alt="image" src="https://github.com/user-attachments/assets/6592970c-ea0b-4915-8e11-eb440f8a9154" />


 
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
<img width="404" height="296" alt="image" src="https://github.com/user-attachments/assets/dd4cf067-383b-4296-9d07-1dbf56ca2e9d" />



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
<img width="462" height="71" alt="image" src="https://github.com/user-attachments/assets/d0013603-06eb-4f3c-a7c6-7a1682f05554" />

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
<img width="539" height="502" alt="image" src="https://github.com/user-attachments/assets/86d0644b-3f1d-48b0-9223-da3f810f7b44" />



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
<img width="611" height="397" alt="image" src="https://github.com/user-attachments/assets/d51f1787-0d42-4295-80f8-d6353214f44c" />

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
<img width="602" height="497" alt="image" src="https://github.com/user-attachments/assets/7b3d9d2b-61db-4fea-8748-7078ccbc68ef" />

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

<img width="485" height="65" alt="image" src="https://github.com/user-attachments/assets/32fbb235-c77d-4300-995a-2fd11d50faec" />

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
<img width="510" height="65" alt="image" src="https://github.com/user-attachments/assets/5e604cc3-f031-4591-a525-da8081388cfc" />

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
<img width="503" height="72" alt="image" src="https://github.com/user-attachments/assets/abdcf2d4-5c4e-47a2-acdd-4f215f5e0f0e" />
 
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
 <img width="494" height="232" alt="image" src="https://github.com/user-attachments/assets/10ea6dd3-2ed3-4ddf-a03a-874816e5f022" />

 
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
 
 <img width="516" height="133" alt="image" src="https://github.com/user-attachments/assets/2e79407a-6107-49f2-bfb5-d1c965fd4837" />

 
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
 <img width="510" height="179" alt="image" src="https://github.com/user-attachments/assets/6265c461-b640-4e17-a4ab-039a340af740" />

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
 <img width="490" height="121" alt="image" src="https://github.com/user-attachments/assets/74d08da7-03a6-4666-a9c1-521755ae453d" />

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
<img width="531" height="161" alt="image" src="https://github.com/user-attachments/assets/e735b8ea-9e7a-4da5-9515-5fc3be05ebe5" />

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
<img width="528" height="273" alt="image" src="https://github.com/user-attachments/assets/912b29a6-e4cd-4f97-86c4-5ee1e2e3f204" />


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
<img width="491" height="141" alt="image" src="https://github.com/user-attachments/assets/68c51b14-ca91-4a6e-be22-fc5f6e0842ff" />

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
<img width="503" height="132" alt="image" src="https://github.com/user-attachments/assets/ef94af3a-d5c4-4dd1-8d99-bdbbddb20171" />

 
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
<img width="536" height="268" alt="image" src="https://github.com/user-attachments/assets/8b423aac-90f7-40ef-9992-76e46fc8da6b" />

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
 <img width="475" height="101" alt="image" src="https://github.com/user-attachments/assets/5c20a44a-aaac-4111-9143-802af2c9d2c1" />

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

<img width="491" height="136" alt="image" src="https://github.com/user-attachments/assets/6aef05c2-5597-4294-b0e2-2d750a0413f1" />

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
<img width="475" height="55" alt="image" src="https://github.com/user-attachments/assets/c1761927-bafb-4a62-a520-d0eabea18676" />

 
 ./funcex.sh 1 2
<img width="442" height="47" alt="image" src="https://github.com/user-attachments/assets/919145a9-3951-42c3-88ff-81c2185591d7" />

 
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
 <img width="462" height="99" alt="image" src="https://github.com/user-attachments/assets/b47105f1-2c16-4372-9a5c-407856ea53d6" />

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
 <img width="507" height="100" alt="image" src="https://github.com/user-attachments/assets/15fe3e71-d296-418d-af50-2cdec99578d2" />

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
 <img width="509" height="311" alt="image" src="https://github.com/user-attachments/assets/29b29bc2-7d90-4fba-bd4c-38104071ab29" />

 
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
<img width="473" height="275" alt="image" src="https://github.com/user-attachments/assets/3d18f1c4-0c99-4239-9806-a00447698ac4" />
 
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
<img width="523" height="290" alt="image" src="https://github.com/user-attachments/assets/595c946d-7929-4eca-8c9b-4bab7f1a55a2" />


# RESULT:
The Commands are executed successfully.

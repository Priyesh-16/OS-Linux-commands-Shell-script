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

<img width="473" height="160" alt="image" src="https://github.com/user-attachments/assets/12720680-e1de-4ebe-92d7-975a417c5433" />

cat < file2
## OUTPUT

<img width="473" height="179" alt="image" src="https://github.com/user-attachments/assets/7735a382-1a45-4242-9320-9ea1be53dcb7" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="497" height="72" alt="image" src="https://github.com/user-attachments/assets/ea58f7e2-8071-4a48-b048-8e02eb354ae5" />

comm file1 file2
 ## OUTPUT
 
<img width="539" height="277" alt="image" src="https://github.com/user-attachments/assets/10bd4ade-a6b4-4fa7-91bf-37faf2cf83fe" />

 
diff file1 file2
## OUTPUT

<img width="539" height="246" alt="image" src="https://github.com/user-attachments/assets/f55ae54d-c639-4655-9af1-de0eddbae3d7" />


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

<img width="556" height="74" alt="image" src="https://github.com/user-attachments/assets/c1908838-9d1d-4a03-95c2-0c3854afec5d" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="551" height="119" alt="image" src="https://github.com/user-attachments/assets/ca484423-611a-41de-9dee-3fe3dd31a682" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="551" height="119" alt="image" src="https://github.com/user-attachments/assets/c934a4b4-8553-49ad-8c1b-c21583c3fa04" />


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

<img width="557" height="65" alt="image" src="https://github.com/user-attachments/assets/eb96ac7f-fa3b-4353-ae82-a006ff5e0282" />



grep hello newfile 
## OUTPUT

<img width="557" height="65" alt="image" src="https://github.com/user-attachments/assets/7840592d-0310-47de-b3b7-a1b83cae5333" />



grep -v hello newfile 
## OUTPUT

<img width="698" height="88" alt="image" src="https://github.com/user-attachments/assets/56e54a73-c97e-4731-8798-0f85a72d45c8" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="698" height="88" alt="image" src="https://github.com/user-attachments/assets/ebf64154-9470-46c4-98af-667b9d451b98" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="685" height="66" alt="image" src="https://github.com/user-attachments/assets/2e2ab043-2ec6-4f0b-bdbe-16bd43eb28fc" />




grep -R ubuntu /etc
## OUTPUT

<img width="698" height="243" alt="image" src="https://github.com/user-attachments/assets/a88df949-c01d-4bd7-9bfe-f31b55d4e7be" />


grep -w -n world newfile   
## OUTPUT

<img width="717" height="83" alt="image" src="https://github.com/user-attachments/assets/794f431d-156d-4854-9cec-53330072d2b3" />

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

<img width="710" height="79" alt="image" src="https://github.com/user-attachments/assets/013e6a3b-cd4f-4771-9101-501b0e3b8ed1" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="704" height="68" alt="image" src="https://github.com/user-attachments/assets/ae6a6ff3-ea8b-47c9-b1e9-c03a9e315fbe" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="710" height="79" alt="image" src="https://github.com/user-attachments/assets/562cec8f-ab5b-49f1-9848-c21bd64b3921" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="710" height="61" alt="image" src="https://github.com/user-attachments/assets/36512478-e165-455f-8823-76d58ff666c4" />


egrep '(world$)' newfile 
## OUTPUT

<img width="709" height="77" alt="image" src="https://github.com/user-attachments/assets/2174f24b-8d80-45fb-97c7-adaf22e602b1" />



egrep '(World$)' newfile 
## OUTPUT

<img width="695" height="64" alt="image" src="https://github.com/user-attachments/assets/374f8010-ffe1-49f4-946b-1ae4df969717" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="701" height="104" alt="image" src="https://github.com/user-attachments/assets/d7d1a240-70de-4610-9ed4-c6de9a33157f" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="697" height="60" alt="image" src="https://github.com/user-attachments/assets/83e5aace-11b3-430d-a79c-0e961d44737a" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="697" height="60" alt="image" src="https://github.com/user-attachments/assets/b2b30d52-6a76-4715-954c-bea8b1cc8b7a" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="697" height="60" alt="image" src="https://github.com/user-attachments/assets/7bc6a6de-0f26-4cd8-9924-0a81353e3591" />


egrep l{2} newfile
## OUTPUT

<img width="706" height="82" alt="image" src="https://github.com/user-attachments/assets/c1088208-aae0-4fb8-9df3-ef564a71927c" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="704" height="98" alt="image" src="https://github.com/user-attachments/assets/0df72640-fbd0-4d23-aec9-cd7e3e5a1764" />

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

<img width="889" height="44" alt="image" src="https://github.com/user-attachments/assets/0c5e120e-9925-4161-80af-d1d38979562d" />


sed -n -e '$p' file23
## OUTPUT

<img width="889" height="44" alt="image" src="https://github.com/user-attachments/assets/bdecca4f-d07b-4ee0-b391-dda1bc892231" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="940" height="169" alt="image" src="https://github.com/user-attachments/assets/9e10192d-6d96-4ab3-b8a1-72c6c8f2a64c" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="950" height="169" alt="image" src="https://github.com/user-attachments/assets/93e1a501-9e76-46f8-85e5-69cc13d494ae" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="950" height="169" alt="image" src="https://github.com/user-attachments/assets/a3ebc6a2-4962-49ae-af75-5098953b36f1" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="952" height="117" alt="image" src="https://github.com/user-attachments/assets/62cf31d6-6eef-4f78-a417-be779de48daf" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="951" height="78" alt="image" src="https://github.com/user-attachments/assets/c5b7f236-48ac-4662-96ad-e53da62d5453" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="969" height="62" alt="image" src="https://github.com/user-attachments/assets/4c96205a-d2ec-4a20-8116-51ab84670141" />


seq 10 
## OUTPUT

<img width="754" height="198" alt="image" src="https://github.com/user-attachments/assets/90b63d40-f852-494a-8850-d442ecebd00a" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="888" height="79" alt="image" src="https://github.com/user-attachments/assets/98cddbc5-8b77-4527-adb8-3266469756f9" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="892" height="76" alt="image" src="https://github.com/user-attachments/assets/272fadc5-e264-4aa6-a6f6-726f1954c536" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="891" height="94" alt="image" src="https://github.com/user-attachments/assets/7eed39f2-0b2a-4127-ba53-2b65488ababb" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="890" height="82" alt="image" src="https://github.com/user-attachments/assets/a93b62ba-cee6-414e-8f19-c2178a85f0ad" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="910" height="80" alt="image" src="https://github.com/user-attachments/assets/4d502e2c-3ed1-4a37-bdaf-19b9cf67d5e6" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="954" height="76" alt="image" src="https://github.com/user-attachments/assets/f99f6a6f-c139-495f-aa11-788498d3a2f7" />


sed -n '2,4{s/$/*/;p}' file23

<img width="954" height="76" alt="image" src="https://github.com/user-attachments/assets/deaafc7f-b85f-4687-9517-d6c39d93cbce" />


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

<img width="796" height="112" alt="image" src="https://github.com/user-attachments/assets/1a68335e-80ab-4ddf-a2ac-52bf14ed8bcc" />


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

<img width="796" height="112" alt="image" src="https://github.com/user-attachments/assets/aa4e5f61-3e38-40c7-881f-7ed7d3c210fe" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
<img width="1006" height="169" alt="image" src="https://github.com/user-attachments/assets/7f7056fe-6baa-4395-9749-e08bc53a3556" />

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
 
<img width="858" height="74" alt="image" src="https://github.com/user-attachments/assets/e4a2ff11-cbc9-4ede-a5f6-e45f5c94b42b" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="947" height="75" alt="image" src="https://github.com/user-attachments/assets/52674bd6-9c43-4684-be96-a876ab9ee022" />

<img width="1055" height="76" alt="image" src="https://github.com/user-attachments/assets/31eb8410-7545-4c03-8589-1e9ff27045fa" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="892" height="363" alt="image" src="https://github.com/user-attachments/assets/2ce71065-56f0-443d-bcaa-2619ccbb82e7" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="967" height="1001" alt="image" src="https://github.com/user-attachments/assets/d310c3b7-711c-4e33-a8ee-6377156113cd" />

tar -xvf backup.tar
## OUTPUT
<img width="967" height="1001" alt="image" src="https://github.com/user-attachments/assets/2efc11bd-ded3-40c5-9723-521b2783bde7" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="861" height="44" alt="image" src="https://github.com/user-attachments/assets/140b9e4a-4fee-40fe-a70f-635b6ea83f0e" />

gunzip backup.tar.gz
## OUTPUT

<img width="1662" height="279" alt="image" src="https://github.com/user-attachments/assets/6ec5d895-6877-4e1f-ace1-4f5f53707b46" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="1110" height="134" alt="image" src="https://github.com/user-attachments/assets/0195e8f8-67a1-4ccb-a762-e16cb2cf2c70" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="942" height="161" alt="image" src="https://github.com/user-attachments/assets/203dd3f2-3cd8-49ba-b98b-0c8d704211c7" />


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

 <img width="901" height="507" alt="image" src="https://github.com/user-attachments/assets/5170010d-87ce-4689-8beb-1bf1aefb9bce" />

ls file1
## OUTPUT

<img width="773" height="35" alt="image" src="https://github.com/user-attachments/assets/063731d6-d699-4c46-a229-297e669ade1b" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="773" height="45" alt="image" src="https://github.com/user-attachments/assets/0869792a-e702-4498-96f4-21a2227a0ca5" />

echo $?
## OUTPUT 

 <img width="769" height="185" alt="image" src="https://github.com/user-attachments/assets/e1077e2a-2459-45aa-b429-2b7e264b0426" />

abcd
 
echo $?
 ## OUTPUT
 
<img width="769" height="185" alt="image" src="https://github.com/user-attachments/assets/cb81647b-d255-4d2c-88b8-a2f9d7dc50cb" />


 
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

<img width="840" height="186" alt="image" src="https://github.com/user-attachments/assets/a2dc8ff9-eec9-442d-abca-47ec47622ab9" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="804" height="45" alt="image" src="https://github.com/user-attachments/assets/56f48687-2eee-4316-b8f7-ef5e1d7308d6" />

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

<img width="824" height="47" alt="image" src="https://github.com/user-attachments/assets/6a9bb279-06b9-4a68-a266-bd0e89957490" />

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

<img width="820" height="82" alt="image" src="https://github.com/user-attachments/assets/bf7d8e1a-4612-4ff6-9ef7-c4608d7c7b04" />


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

<img width="792" height="62" alt="image" src="https://github.com/user-attachments/assets/db794b02-f34f-45da-8ffc-a3d014c960a6" />

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

<img width="820" height="82" alt="image" src="https://github.com/user-attachments/assets/461ce2f8-4177-4b00-a9c8-d58cb7c82722" />

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

<img width="823" height="44" alt="image" src="https://github.com/user-attachments/assets/c8c32ee6-bb9c-41e4-a7ae-30e3d6a5c22e" />


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

<img width="823" height="44" alt="image" src="https://github.com/user-attachments/assets/61742fef-fc4a-4604-aa2b-bd2f5304b6e8" />

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
 <img width="823" height="44" alt="image" src="https://github.com/user-attachments/assets/2c127d54-f896-4566-adc8-22c7514a79f7" />

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
 
 <img width="829" height="100" alt="image" src="https://github.com/user-attachments/assets/3b3ab5f4-44d0-4792-83d5-175c8c6191fb" />

 
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

 <img width="789" height="128" alt="image" src="https://github.com/user-attachments/assets/e71b5e74-6e3f-4b08-9f58-1620d6a79f5b" />

 
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

 <img width="784" height="80" alt="image" src="https://github.com/user-attachments/assets/588d1d97-2660-4919-a432-6efd5c3ae106" />

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

 <img width="787" height="152" alt="image" src="https://github.com/user-attachments/assets/3571848a-6024-4365-ac13-6f7a9129be14" />

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

<img width="816" height="113" alt="image" src="https://github.com/user-attachments/assets/624f109c-8789-4402-ad95-b99c7fabb8bd" />

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

<img width="833" height="236" alt="image" src="https://github.com/user-attachments/assets/63d2502a-b014-4661-b4c9-1b12be2e777c" />

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

<img width="837" height="113" alt="image" src="https://github.com/user-attachments/assets/8a5f9b68-72f9-4362-9046-8ae839fe95fd" />

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

 <img width="799" height="57" alt="image" src="https://github.com/user-attachments/assets/9968fb65-d9ea-4ef3-a560-550d3f12ed5d" />

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

<img width="808" height="57" alt="image" src="https://github.com/user-attachments/assets/77639605-f285-421d-bde0-6f1c266180d5" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="807" height="37" alt="image" src="https://github.com/user-attachments/assets/e44e6950-82f4-483a-96e0-3df62db87bdc" />



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

<img width="869" height="72" alt="image" src="https://github.com/user-attachments/assets/cff99f32-7212-4e7e-9c8e-ebe59672ad38" />

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

<img width="895" height="255" alt="image" src="https://github.com/user-attachments/assets/2377aa95-a4e2-44e6-8677-55acf4655d59" />

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
 
 <img width="869" height="72" alt="image" src="https://github.com/user-attachments/assets/8c01ae7d-966b-4d32-bf00-9826cd1c67ad" />

 
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

 <img width="839" height="72" alt="image" src="https://github.com/user-attachments/assets/3e6b2c98-09f6-41d4-ad90-8e494c512376" />

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

<img width="839" height="72" alt="image" src="https://github.com/user-attachments/assets/2876d071-bf99-4ff3-aaeb-5c31aca50800" />


# RESULT:
The Commands are executed successfully.

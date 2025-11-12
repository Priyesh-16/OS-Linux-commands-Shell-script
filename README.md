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

<img width="351" height="170" alt="Screenshot 2025-09-16 112743" src="https://github.com/user-attachments/assets/d400e5fb-9b3b-4a8b-b45a-03d6d5efd339" />


cat < file2
## OUTPUT

<img width="362" height="197" alt="Screenshot 2025-09-16 112752" src="https://github.com/user-attachments/assets/e04ea894-b9d7-4e79-b529-920810ce924c" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="385" height="96" alt="Screenshot 2025-09-16 112939" src="https://github.com/user-attachments/assets/7c3a04b1-596f-4061-a8ff-cfb253ce02c7" />


comm file1 file2
 ## OUTPUT

 <img width="395" height="347" alt="Screenshot 2025-09-16 113330" src="https://github.com/user-attachments/assets/8d26ff28-1e66-4b0e-b2d0-6264c908a6d3" />


 
diff file1 file2
## OUTPUT

<img width="405" height="266" alt="Screenshot 2025-09-16 113345" src="https://github.com/user-attachments/assets/9a6ba110-33a7-4e4e-98ae-33af4bcd4c4f" />



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

<img width="349" height="126" alt="Screenshot 2025-09-16 113745" src="https://github.com/user-attachments/assets/93b706e1-a3d5-47fa-af2c-ffe9b1063147" />





cut -d "|" -f 1 file22
## OUTPUT

<img width="349" height="157" alt="Screenshot 2025-09-16 113828" src="https://github.com/user-attachments/assets/aed5876a-7473-4b5a-a47c-c9823243768b" />




cut -d "|" -f 2 file22
## OUTPUT

<img width="342" height="145" alt="Screenshot 2025-09-16 113855" src="https://github.com/user-attachments/assets/907c10ac-c33e-4edd-be51-33d60ace36e5" />



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

<img width="337" height="69" alt="Screenshot 2025-09-16 114837" src="https://github.com/user-attachments/assets/214a083b-e369-4236-862c-0687d16f0e23" />


grep hello newfile 
## OUTPUT

<img width="337" height="69" alt="Screenshot 2025-09-16 114837" src="https://github.com/user-attachments/assets/27fb08b3-2749-4285-bb01-930c6c2bea1e" />



grep -v hello newfile 
## OUTPUT

<img width="343" height="90" alt="Screenshot 2025-09-16 114919" src="https://github.com/user-attachments/assets/5e63baec-eee5-4123-8705-95c8905d2cd2" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="346" height="90" alt="Screenshot 2025-09-16 114942" src="https://github.com/user-attachments/assets/1fa7e29b-f3c3-44e9-9875-01905d8c927a" />





cat newfile | grep -i -c "hello"
## OUTPUT

<img width="379" height="68" alt="Screenshot 2025-09-16 115018" src="https://github.com/user-attachments/assets/ebd74d3d-b8e2-4360-92c7-ae83472961d2" />





grep -R ubuntu /etc
## OUTPUT

<img width="782" height="259" alt="Screenshot 2025-09-16 115235" src="https://github.com/user-attachments/assets/2bc23a7b-1167-4829-a009-0d7cc9b322fb" />




grep -w -n world newfile   
## OUTPUT

<img width="376" height="100" alt="Screenshot 2025-09-16 115305" src="https://github.com/user-attachments/assets/971cb49b-fbf4-4395-9b45-7ae8a4b46d87" />



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

<img width="368" height="98" alt="Screenshot 2025-09-16 115509" src="https://github.com/user-attachments/assets/aad8d985-6d53-4edc-b388-d39e40ce36f9" />




egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="343" height="101" alt="Screenshot 2025-09-16 115535" src="https://github.com/user-attachments/assets/c76dde00-6dda-4400-8847-3e8f82a22617" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="387" height="95" alt="Screenshot 2025-09-16 115610" src="https://github.com/user-attachments/assets/e3117960-6c9d-4401-87ae-91f59d364098" />





egrep '(^hello)' newfile 
## OUTPUT

<img width="341" height="69" alt="Screenshot 2025-09-16 115633" src="https://github.com/user-attachments/assets/92a30c2a-168e-43a1-b1d5-cd3042a12fe8" />




egrep '(world$)' newfile 
## OUTPUT

<img width="343" height="96" alt="Screenshot 2025-09-17 103444" src="https://github.com/user-attachments/assets/96a9fd09-398e-4150-965e-b772e49dbf17" />




egrep '(World$)' newfile 
## OUTPUT

<img width="345" height="68" alt="Screenshot 2025-09-17 103520" src="https://github.com/user-attachments/assets/33516dcc-5c13-42b7-83dd-e20ed1c54d60" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="356" height="120" alt="Screenshot 2025-09-17 103541" src="https://github.com/user-attachments/assets/1c612826-9091-4b04-939b-79a6b8e48433" />




egrep '[1-9]' newfile 
## OUTPUT

<img width="342" height="74" alt="Screenshot 2025-09-17 103606" src="https://github.com/user-attachments/assets/7b39ff19-5f05-4849-ad60-5a007b3f4a96" />




egrep 'Linux.*world' newfile 
## OUTPUT

<img width="348" height="75" alt="Screenshot 2025-09-17 103642" src="https://github.com/user-attachments/assets/9098796e-c510-4b04-9754-7a89a5501803" />



egrep 'Linux.*World' newfile 
## OUTPUT

<img width="346" height="75" alt="Screenshot 2025-09-17 103750" src="https://github.com/user-attachments/assets/ed467e9a-abd3-44d1-95c3-1bb42ee6a2fa" />



egrep l{2} newfile
## OUTPUT

<img width="350" height="93" alt="Screenshot 2025-09-17 103812" src="https://github.com/user-attachments/assets/42b2413b-120c-4ad5-9baa-525330a17ac3" />




egrep 's{1,2}' newfile
## OUTPUT 

<img width="352" height="116" alt="Screenshot 2025-09-17 103833" src="https://github.com/user-attachments/assets/bb76dbf8-177b-4c51-9e6c-d7d7f33183d8" />



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

<img width="344" height="71" alt="Screenshot 2025-09-17 104112" src="https://github.com/user-attachments/assets/81a3ba12-0f1c-4539-927a-4e7689b5dc2b" />




sed -n -e '$p' file23
## OUTPUT

<img width="342" height="74" alt="Screenshot 2025-09-17 104137" src="https://github.com/user-attachments/assets/c8df6f12-6c7e-4f8b-8eaa-4910c586d76d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="346" height="268" alt="Screenshot 2025-09-17 104200" src="https://github.com/user-attachments/assets/70c34a8a-a0c0-49cd-9c85-8e81d7624d59" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="352" height="273" alt="Screenshot 2025-09-17 104228" src="https://github.com/user-attachments/assets/c2d0b472-194e-44af-a6db-62df96e298e7" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="367" height="271" alt="Screenshot 2025-09-17 104249" src="https://github.com/user-attachments/assets/0eb408c5-deac-45aa-aa83-4b96519076db" />





sed -n -e '1,5p' file23
## OUTPUT

<img width="352" height="180" alt="Screenshot 2025-09-17 104314" src="https://github.com/user-attachments/assets/62905d43-90cf-404f-8c93-523f953e0f66" />




sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="361" height="125" alt="Screenshot 2025-09-17 104335" src="https://github.com/user-attachments/assets/da66519e-5306-49a7-a811-c737b03cbefa" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="379" height="101" alt="Screenshot 2025-09-17 104354" src="https://github.com/user-attachments/assets/ed9afe6a-e871-4c8d-9ab3-c666a9dee8bc" />




seq 10 
## OUTPUT

<img width="346" height="305" alt="Screenshot 2025-09-17 104415" src="https://github.com/user-attachments/assets/bb7cff1d-1d20-4671-8635-377bae61f96a" />




seq 10 | sed -n '4,6p'
## OUTPUT

<img width="355" height="119" alt="Screenshot 2025-09-17 104438" src="https://github.com/user-attachments/assets/d37a14b1-f98b-4031-bc63-dd27f9b8ccbd" />




seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT

<img width="356" height="145" alt="Screenshot 2025-09-17 104500" src="https://github.com/user-attachments/assets/7f3f4c55-5ffb-4c9e-affe-abafd63f1d0f" />




seq 2 | sed '2i hello'
## OUTPUT

<img width="346" height="121" alt="Screenshot 2025-09-17 104517" src="https://github.com/user-attachments/assets/4ce37e18-abae-48c8-aa2c-da84ca3da313" />



seq 10 | sed '2,9c hello'
## OUTPUT

<img width="365" height="125" alt="Screenshot 2025-09-17 104536" src="https://github.com/user-attachments/assets/45afc5de-61be-440f-81f9-d1f8933c5a17" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="395" height="123" alt="Screenshot 2025-09-17 104602" src="https://github.com/user-attachments/assets/7876f139-b436-4785-a049-a3bbc74d289f" />




sed -n '2,4{s/$/*/;p}' file23

<img width="376" height="136" alt="Screenshot 2025-09-17 104628" src="https://github.com/user-attachments/assets/10c2cfa3-dd81-478a-a199-dcc879c0d252" />



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

<img width="351" height="164" alt="Screenshot 2025-09-17 104718" src="https://github.com/user-attachments/assets/d4e01905-d760-4101-833c-b0a5e5f0cd5b" />



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

<img width="344" height="167" alt="Screenshot 2025-09-17 104814" src="https://github.com/user-attachments/assets/95552027-dd6d-4cca-8954-805e401e7258" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="531" height="240" alt="image" src="https://github.com/user-attachments/assets/92791c98-bff9-48e9-92d5-04b53c15d267" />

cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
^d
 
cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
 
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="388" height="123" alt="image" src="https://github.com/user-attachments/assets/39ce4a7f-824a-4c76-98e5-b07305313cbb" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="498" height="121" alt="image" src="https://github.com/user-attachments/assets/385f0a08-2110-4cbe-ab3a-038a41594013" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="579" height="403" alt="image" src="https://github.com/user-attachments/assets/19e0686e-3e03-45ea-81fe-07eb80314a78" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="972" height="504" alt="image" src="https://github.com/user-attachments/assets/06bb859d-4adb-4e40-aca9-4c2e2a4aadeb" />


tar -xvf backup.tar
## OUTPUT
<img width="550" height="433" alt="image" src="https://github.com/user-attachments/assets/1126231e-7026-41e6-9a42-07e9dc8fc941" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="405" height="76" alt="image" src="https://github.com/user-attachments/assets/79ea6121-9599-446a-8eb8-afb043fbe6a2" />

gunzip backup.tar.gz
## OUTPUT
<img width="1632" height="128" alt="image" src="https://github.com/user-attachments/assets/38b174d6-a012-4bf4-bbcc-e01081e65eb2" />

 
# Shell Script

echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="453" height="224" alt="image" src="https://github.com/user-attachments/assets/87e3bf8f-7adc-4a6f-b36c-9c28ce39e931" />

 
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop


cat herecheck.txt
## OUTPUT
<img width="432" height="128" alt="image" src="https://github.com/user-attachments/assets/b1ec9192-1447-48c7-9db7-8fd3c08e009f" />


cat < scriptest.sh 
bash
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
 

cat scriptest.sh 
bash
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

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="797" height="437" alt="image" src="https://github.com/user-attachments/assets/68284ad2-386c-406a-93c9-43b4e6621575" />

 
ls file1
## OUTPUT
<img width="293" height="74" alt="image" src="https://github.com/user-attachments/assets/f4d19cb4-e71b-40a0-a490-4426efccde1a" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="272" height="77" alt="image" src="https://github.com/user-attachments/assets/e8a0fe64-a345-4ea9-a647-4d1c7bf1e616" />

echo $?
## OUTPUT 

 <img width="361" height="71" alt="image" src="https://github.com/user-attachments/assets/3c3f2fe8-cd92-4c69-9cbd-272eb63f29e7" />

abcd
 
echo $?
 ## OUTPUT
<img width="361" height="71" alt="image" src="https://github.com/user-attachments/assets/9d0d8ce8-cbdf-4fd6-afdf-213cf4d077dc" />


 
# mis-using string comparisons

cat < strcomp.sh 
bash
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


cat strcomp.sh 
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi

##OUTPUT

<img width="432" height="257" alt="image" src="https://github.com/user-attachments/assets/437d183c-2fb8-4fd6-99de-fbaf17291233" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="692" height="152" alt="image" src="https://github.com/user-attachments/assets/ddc41915-50d9-4fff-b873-419239d64e87" />

# check file ownership
cat < psswdperm.sh 
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d


cat psswdperm.sh 
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 
./psswdperm.sh
## OUTPUT

<img width="651" height="212" alt="image" src="https://github.com/user-attachments/assets/f4f1e6c2-0ab7-4d71-838d-43880ed5b9e9" />

# check if with file location
cat>ifnested.sh 
bash
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

cat ifnested.sh 

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


./ifnested.sh 
## OUTPUT

<img width="610" height="247" alt="image" src="https://github.com/user-attachments/assets/c7b432e8-bac2-42d9-ba4e-8bc736e1c8de" />


# using numeric test comparisons
cat > iftest.sh 
bash
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



cat iftest.sh 
bash
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


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

<img width="613" height="166" alt="image" src="https://github.com/user-attachments/assets/31226db2-855a-480a-95c3-f93a83a0f60a" />

# check if a file
cat > ifnested.sh 
bash
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


cat ifnested.sh 
bash
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


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

<img width="690" height="193" alt="image" src="https://github.com/user-attachments/assets/d350447f-51ec-4b2b-8017-edd373c88ae6" />

# looking for a possible value using elif
cat elifcheck.sh 
bash
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


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="702" height="152" alt="image" src="https://github.com/user-attachments/assets/4d3fd91f-20c2-4f3e-ba56-64cab2077be6" />


# testing compound comparisons
cat> ifcompound.sh 
bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="693" height="145" alt="image" src="https://github.com/user-attachments/assets/b189a1e0-00b3-44cc-a06a-9c246fa60b70" />

# using the case command
cat >casecheck.sh 
bash
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

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 ## Output
 <img width="357" height="117" alt="image" src="https://github.com/user-attachments/assets/f5d614cf-b50c-4b8f-a11c-c6ae90da3223" />

cat > whiletest
bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## Output
 <img width="366" height="339" alt="image" src="https://github.com/user-attachments/assets/1d18fe55-8db5-4426-9792-7fc7fae047d2" />

 
cat untiltest.sh 
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
 
$ chmod 755 untiltest.sh
 ## Output
 <img width="527" height="171" alt="image" src="https://github.com/user-attachments/assets/7d5b02d5-c36d-41e7-9012-75ccb9695131" />

 
 
cat forin1.sh 
bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 
 
$ chmod 755 forin1.sh
 ## Output
 <img width="658" height="242" alt="image" src="https://github.com/user-attachments/assets/657dc86e-adfd-470e-91dd-269432503327" />

 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done

$ chmod 755 forin2.sh
 
$ ./forin2.sh
## Output
 <img width="653" height="216" alt="image" src="https://github.com/user-attachments/assets/b31f806f-d83e-492e-a2b8-fbaecd460aea" />

cat forin3.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done

$ ./forin3.sh 
 ## Output
 <img width="584" height="246" alt="image" src="https://github.com/user-attachments/assets/14d71048-0ed5-4310-9953-929e0ea2ad17" />

cat forin1.sh 
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

$ chmod 755 forin1.sh

## OUTPUT

<img width="364" height="220" alt="image" src="https://github.com/user-attachments/assets/052e583f-b067-4cb0-91b0-3b59b8e640db" />


cat forinfile.sh 
bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done

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
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
`
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

<img width="235" height="173" alt="image" src="https://github.com/user-attachments/assets/59ae4d93-39ba-4836-9ee6-44f59cd1d24f" />

 
cat forctype1.sh 
bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="369" height="224" alt="image" src="https://github.com/user-attachments/assets/a27f8da6-626b-4809-a42b-a5d0765cd1b0" />
cat fornested1.sh 
bash
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

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="323" height="387" alt="image" src="https://github.com/user-attachments/assets/7477327d-53cc-44ca-a5ee-1d1e4d13ebdb" />

 
cat forbreak.sh 
bash
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

## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

 <img width="266" height="104" alt="image" src="https://github.com/user-attachments/assets/40347aeb-f838-4289-a5c6-290465640488" />


cat forbreak.sh 
bash
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


 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="331" height="178" alt="image" src="https://github.com/user-attachments/assets/69657555-406b-4006-baa0-f4bf9c5a97cf" />


cat exread.sh 
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="389" height="105" alt="image" src="https://github.com/user-attachments/assets/071266b5-5577-4c81-9910-49d035475d17" />


 cat exread1.sh
bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 

 
<img width="400" height="107" alt="image" src="https://github.com/user-attachments/assets/e82cedd7-d93b-4530-82b3-3fd10a20b4e8" />


cat funcex.sh
bash
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

## OUTPUT
 ./funcex.sh 

<img width="331" height="82" alt="image" src="https://github.com/user-attachments/assets/fd5162fb-81ea-4514-b27c-9024b5ae66c6" />

 
 ./funcex.sh 1 2

<img width="274" height="81" alt="image" src="https://github.com/user-attachments/assets/e4391bf5-4b31-44ab-aafd-0a13ff62dded" />

 
cat argshift.sh
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done

$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3

  <img width="335" height="122" alt="image" src="https://github.com/user-attachments/assets/df8dadad-8d19-4b4b-bfbf-97fb43062877" />
  
 cat argshift1.sh
bash
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

$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3

<img width="309" height="127" alt="image" src="https://github.com/user-attachments/assets/99167770-90a1-4a21-9acf-827c67e4ee9c" />


cat argshift.sh
bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x

## OUTPUT
 ./argshift.sh 1 2 3
 
<img width="509" height="421" alt="image" src="https://github.com/user-attachments/assets/1db13d86-39af-40e2-a9fe-8024cfa1856c" />
 
 
cat > nc.awk
bash
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
 
cat>data.dat
bash
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

awk -f nc.awk data.dat
## OUTPUT 
 <img width="411" height="366" alt="image" src="https://github.com/user-attachments/assets/715dbc51-2db3-4f41-a0d4-48ba59a0535d" />

cat > palindrome.sh
bash
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

## OUTPUT 
<img width="290" height="131" alt="image" src="https://github.com/user-attachments/assets/c87b04f6-2a8d-414f-a6a7-9e6e3f0c4660" />


# RESULT:
The Commands are executed successfully.

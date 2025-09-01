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
<img width="490" height="295" alt="Screenshot 2025-08-20 083406" src="https://github.com/user-attachments/assets/949e1afb-6588-4714-ae66-564d3d211f22" />



cat < file2
## OUTPUT
<img width="537" height="340" alt="Screenshot 2025-08-20 083427" src="https://github.com/user-attachments/assets/784c78cf-e29d-4883-85a4-e276e0107415" />



 
comm file1 file2
 ## OUTPUT
<img width="690" height="587" alt="Screenshot 2025-08-20 083634" src="https://github.com/user-attachments/assets/0a099cf0-c17a-4a00-86af-921415a71373" />

 
diff file1 file2
## OUTPUT
<img width="616" height="464" alt="Screenshot 2025-08-20 083642" src="https://github.com/user-attachments/assets/aa4e762d-4a73-4a58-b9b4-28ce2ab07baf" />


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
<img width="453" height="178" alt="Screenshot 2025-08-20 083944" src="https://github.com/user-attachments/assets/f11c489f-dd96-4c97-87d7-d938a6e38e48" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="512" height="210" alt="Screenshot 2025-08-20 084023" src="https://github.com/user-attachments/assets/70da1506-4a97-4fea-9c2b-977815ae1ba7" />



cut -d "|" -f 2 file22
## OUTPUT


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 

grep hello newfile 
## OUTPUT
<img width="434" height="117" alt="Screenshot 2025-08-20 084239" src="https://github.com/user-attachments/assets/6ec14366-8361-4965-a129-c3da2d54956e" />




grep -v hello newfile 
## OUTPUT
<img width="477" height="129" alt="Screenshot 2025-08-20 084243" src="https://github.com/user-attachments/assets/f9da91c3-0d1f-4fcd-bae9-9305a8358388" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="568" height="143" alt="Screenshot 2025-08-20 084248" src="https://github.com/user-attachments/assets/14958ff9-8171-4a29-bfe1-b1cd545cb7a5" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="630" height="109" alt="Screenshot 2025-08-20 084400" src="https://github.com/user-attachments/assets/796d278f-9868-407b-85ce-220d21debfe3" />



grep -R ubuntu /etc
## OUTPUT
<img width="698" height="591" alt="Screenshot 2025-08-20 084438" src="https://github.com/user-attachments/assets/8c55caea-4651-4582-bfa1-08cad9750acc" />



grep -w -n world newfile   
## OUTPUT
<img width="519" height="135" alt="Screenshot 2025-08-20 084617" src="https://github.com/user-attachments/assets/10ff0ab8-a94c-4f46-aaf8-5abb994de9d6" />


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
<img width="670" height="175" alt="Screenshot 2025-08-25 110154" src="https://github.com/user-attachments/assets/62cc8cb9-d894-4e48-b5e5-8b1614719d36" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="667" height="169" alt="Screenshot 2025-08-25 110345" src="https://github.com/user-attachments/assets/efc77579-0f9e-406c-bb91-a84944921458" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="645" height="169" alt="Screenshot 2025-08-25 181652" src="https://github.com/user-attachments/assets/1c726467-73bc-4e0d-97d4-d414be5c9223" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="594" height="128" alt="Screenshot 2025-08-25 181718" src="https://github.com/user-attachments/assets/be17ddce-5e8f-4c81-b34f-5ea0997d3a49" />



egrep '(world$)' newfile 
## OUTPUT
<img width="629" height="160" alt="Screenshot 2025-08-25 181756" src="https://github.com/user-attachments/assets/c2a54c8e-eab3-4a60-8d42-91de6dffc975" />



egrep '(World$)' newfile 
## OUTPUT
<img width="600" height="122" alt="Screenshot 2025-08-25 193832" src="https://github.com/user-attachments/assets/186a686b-781b-4720-989e-b5ea8b9b6f68" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="699" height="207" alt="Screenshot 2025-08-25 193955" src="https://github.com/user-attachments/assets/46ced5e6-e667-42ee-9305-d8126cc5905f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="527" height="134" alt="Screenshot 2025-08-25 194035" src="https://github.com/user-attachments/assets/4ffd86df-694b-47cc-bc9d-2c910393cc03" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="779" height="129" alt="Screenshot 2025-08-25 194041" src="https://github.com/user-attachments/assets/c672fc8e-46c7-4653-a62d-6501a0f1ddb3" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="743" height="139" alt="Screenshot 2025-08-25 194110" src="https://github.com/user-attachments/assets/00370b80-aff2-4d25-a69a-c88aea9140d7" />


egrep l{2} newfile
## OUTPUT
<img width="579" height="174" alt="Screenshot 2025-08-25 194553" src="https://github.com/user-attachments/assets/0ab414b0-0f75-4f78-ab64-ac03c8c50529" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="539" height="211" alt="Screenshot 2025-08-25 194612" src="https://github.com/user-attachments/assets/188edaea-aef1-4845-89be-83e731ae4a8b" />


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
<img width="650" height="135" alt="Screenshot 2025-08-25 194818" src="https://github.com/user-attachments/assets/f93fd462-94af-41c4-9ffb-3fbfd159a49f" />



sed -n -e '$p' file23
## OUTPUT
<img width="572" height="132" alt="Screenshot 2025-08-25 194855" src="https://github.com/user-attachments/assets/20b4c820-fcb3-4802-876f-9d213f75ae87" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="609" height="461" alt="Screenshot 2025-08-25 194947" src="https://github.com/user-attachments/assets/2046f844-fb20-4620-941f-2a1c10c033f8" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="616" height="462" alt="Screenshot 2025-08-25 195004" src="https://github.com/user-attachments/assets/122a81b2-67de-467a-8c2a-dd4c109ece11" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="659" height="466" alt="Screenshot 2025-08-25 195040" src="https://github.com/user-attachments/assets/a1b381da-452b-40f9-992d-65fd00f8b822" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="636" height="296" alt="Screenshot 2025-08-25 195328" src="https://github.com/user-attachments/assets/fe1f7554-2b88-4e16-9338-8b705ebe54df" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="683" height="212" alt="Screenshot 2025-08-25 195344" src="https://github.com/user-attachments/assets/f9267f80-f816-4473-9b4d-5fb7eec6aff6" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="704" height="175" alt="Screenshot 2025-08-25 195617" src="https://github.com/user-attachments/assets/d4030971-19bc-4731-9eca-fb53030d69ae" />



seq 10 
## OUTPUT
<img width="483" height="501" alt="Screenshot 2025-08-25 195631" src="https://github.com/user-attachments/assets/3720bc9c-25e3-46fb-bef4-2f396414b144" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="561" height="215" alt="Screenshot 2025-08-25 195646" src="https://github.com/user-attachments/assets/47dfcf52-4089-4901-b628-7d62802982b7" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="529" height="217" alt="Screenshot 2025-08-25 195659" src="https://github.com/user-attachments/assets/f4bb7e30-af72-4738-83db-add97da165c0" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="533" height="257" alt="Screenshot 2025-08-25 200204" src="https://github.com/user-attachments/assets/5f586768-e0ac-4a4a-9f36-fa3d6aa0bcab" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="586" height="220" alt="Screenshot 2025-08-25 200239" src="https://github.com/user-attachments/assets/a0f62638-0b4a-4853-953d-dd9775903e96" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="586" height="220" alt="Screenshot 2025-08-25 200239" src="https://github.com/user-attachments/assets/32074fab-ec50-4721-b5b9-f679767c9e19" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="666" height="226" alt="Screenshot 2025-08-25 200316" src="https://github.com/user-attachments/assets/e785e9dc-ef3c-4502-9a67-3290573a6e34" />


sed -n '2,4{s/$/*/;p}' file23
<img width="638" height="219" alt="Screenshot 2025-08-25 200331" src="https://github.com/user-attachments/assets/432964ac-007f-467e-80a5-e6b6e66eea5c" />


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
<img width="550" height="302" alt="Screenshot 2025-08-25 200416" src="https://github.com/user-attachments/assets/43d6b7c5-41b4-4274-aec9-c7c3e4ce9401" />


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
<img width="564" height="300" alt="Screenshot 2025-08-25 200459" src="https://github.com/user-attachments/assets/7e79fdc0-0ac5-4913-9d8f-43a1516801fd" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="752" height="465" alt="Screenshot 2025-08-25 200514" src="https://github.com/user-attachments/assets/d5f49a73-20d2-4ec6-95d2-70ee06094fd4" />

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
<img width="609" height="243" alt="Screenshot 2025-08-25 203534" src="https://github.com/user-attachments/assets/c250afe5-2a54-4da8-aaeb-3607ecde8924" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="832" height="260" alt="Screenshot 2025-08-25 203548" src="https://github.com/user-attachments/assets/aa9ad67f-c9ee-4799-9e60-f1f9d4e718a0" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="717" height="468" alt="Screenshot 2025-08-25 203609" src="https://github.com/user-attachments/assets/933986db-e02c-4611-87f7-2a6952b99b81" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="950" height="479" alt="Screenshot 2025-08-25 203647" src="https://github.com/user-attachments/assets/3aa43386-985c-48f1-9b23-c9958f478ba2" />


tar -xvf backup.tar
## OUTPUT
<img width="681" height="340" alt="Screenshot 2025-08-25 203704" src="https://github.com/user-attachments/assets/0f9080d9-6176-4443-8b15-ab0e8fd4bd00" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="718" height="134" alt="Screenshot 2025-08-25 203842" src="https://github.com/user-attachments/assets/f42207ef-dcc2-4bcb-9365-3b59b2a21a65" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="873" height="481" alt="Screenshot 2025-08-26 112200" src="https://github.com/user-attachments/assets/b455dad9-0e67-4a09-b285-5eb057bf43f2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="760" height="471" alt="Screenshot 2025-08-26 112247" src="https://github.com/user-attachments/assets/454c1844-5264-442c-8a00-48cee565dfdb" />


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
<img width="924" height="662" alt="Screenshot 2025-08-26 113447" src="https://github.com/user-attachments/assets/d0e16d73-5cc1-4fae-8dfb-7fd84ce57a7b" />

 
ls file1
## OUTPUT
<img width="503" height="113" alt="Screenshot 2025-08-26 113548" src="https://github.com/user-attachments/assets/3eda1b24-5583-48cb-9099-019d35433d29" />

echo $?
## OUTPUT 
<img width="447" height="115" alt="Screenshot 2025-08-26 113604" src="https://github.com/user-attachments/assets/c6972242-c4c1-4662-8a8f-d8b2d12f8567" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="499" height="113" alt="Screenshot 2025-08-26 113713" src="https://github.com/user-attachments/assets/f6de62f6-fe77-4fdf-a0be-151c4004ebf8" />

 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="923" height="241" alt="Screenshot 2025-08-26 114112" src="https://github.com/user-attachments/assets/24292b4d-d1e9-4ce0-b997-4b367f30125f" />


# check file ownership
cat > psswdperm.sh 
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

cat< psswdperm.sh 
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
<img width="885" height="345" alt="Screenshot 2025-08-26 114303" src="https://github.com/user-attachments/assets/29dcfedc-c44e-4ddb-a8aa-48b302b9ed33" />

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

<img width="955" height="365" alt="Screenshot 2025-08-26 133213" src="https://github.com/user-attachments/assets/8c6cdd27-63db-417c-8cc0-dd44368e68cd" />


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
<img width="961" height="433" alt="Screenshot 2025-08-26 133519" src="https://github.com/user-attachments/assets/64950a4e-c24b-4433-b9f8-e6b66e6f003e" />


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
<img width="537" height="114" alt="Screenshot 2025-08-31 181348" src="https://github.com/user-attachments/assets/12da0d94-95cf-4d8d-bb0a-492a00ab56d5" />

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
<img width="421" height="485" alt="Screenshot 2025-08-31 181853" src="https://github.com/user-attachments/assets/ab7e8da9-4f33-4cc9-97cc-8ed4a002ad0b" />

 
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
 
<img width="884" height="293" alt="Screenshot 2025-09-01 131533" src="https://github.com/user-attachments/assets/539da996-9243-4b17-813e-fecb3f56df55" />

 
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
 <img width="590" height="347" alt="Screenshot 2025-09-01 131651" src="https://github.com/user-attachments/assets/ce9e2d9a-9677-41cd-9e33-be2844e34631" />

 
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
<img width="596" height="208" alt="Screenshot 2025-09-01 131758" src="https://github.com/user-attachments/assets/7e6404a9-6c3e-44b9-8374-55294dfcea9d" />

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
./forin3.sh 
<img width="511" height="344" alt="Screenshot 2025-09-01 131850" src="https://github.com/user-attachments/assets/ccf1c570-b5a3-47a2-ba1a-5cc090a3989c" />



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
<img width="527" height="217" alt="Screenshot 2025-09-01 132239" src="https://github.com/user-attachments/assets/1be94229-4776-4860-a3e7-b8c1f82b3b87" />


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
<img width="588" height="297" alt="Screenshot 2025-09-01 132327" src="https://github.com/user-attachments/assets/16a4dced-2abb-461f-b415-6a1005aa3dd6" />

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
<img width="527" height="303" alt="Screenshot 2025-09-01 132448" src="https://github.com/user-attachments/assets/f757f4aa-c551-44cf-ac7c-a9ff0b8d9acf" />


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
<img width="498" height="602" alt="Screenshot 2025-09-01 132559" src="https://github.com/user-attachments/assets/5987326b-7fa7-41ac-9ec3-9032af1f973d" />

 
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

<img width="572" height="214" alt="Screenshot 2025-09-01 132749" src="https://github.com/user-attachments/assets/9a038bbb-e414-48d6-a449-2e4cb50437d5" />

 
 

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
<img width="818" height="178" alt="Screenshot 2025-09-01 132929" src="https://github.com/user-attachments/assets/562a20b4-f45f-48a6-911c-b801caa0da58" />


 
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

 <img width="493" height="126" alt="Screenshot 2025-09-01 133225" src="https://github.com/user-attachments/assets/ec9784b8-2efe-4608-874f-7632dea8d268" />



 
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
 <img width="520" height="215" alt="Screenshot 2025-09-01 133414" src="https://github.com/user-attachments/assets/27b2d9e7-d0a7-4005-a0e0-3bda6f74bbbd" />

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
<img width="519" height="215" alt="Screenshot 2025-09-01 133526" src="https://github.com/user-attachments/assets/49d0deae-fc30-4f5d-ade2-92d0b0b90984" />


 
 
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
 <img width="581" height="635" alt="Screenshot 2025-09-01 133751" src="https://github.com/user-attachments/assets/df527873-b292-4b9d-838a-3ffbd7940c27" />

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
<img width="689" height="216" alt="Screenshot 2025-09-01 133907" src="https://github.com/user-attachments/assets/34766ad2-ee8a-499f-aa88-7b30ca7f73bf" />


# RESULT:
The Commands are executed successfully.

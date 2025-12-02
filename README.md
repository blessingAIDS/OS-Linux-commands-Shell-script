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

<img width="359" height="181" alt="Screenshot 2025-10-24 085640" src="https://github.com/user-attachments/assets/a19e5095-3dda-491e-b5a1-1f149c59e8b6" />


cat < file2
## OUTPUT

<img width="403" height="204" alt="Screenshot 2025-10-24 085703" src="https://github.com/user-attachments/assets/6a1ae5a7-5166-4594-a037-db9a6b7c536a" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="455" height="95" alt="Screenshot 2025-10-24 085727" src="https://github.com/user-attachments/assets/c7dc18be-a172-462d-81ff-a8940f3a92a1" />



comm file1 file2
 ## OUTPUT

<img width="374" height="350" alt="Screenshot 2025-10-24 085858" src="https://github.com/user-attachments/assets/b4914273-d3bd-4242-af20-a0d559910353" />

 
diff file1 file2
## OUTPUT

<img width="327" height="271" alt="Screenshot 2025-10-24 085936" src="https://github.com/user-attachments/assets/04452ecb-5e8e-4121-900f-d6dde6ec1661" />


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

<img width="299" height="125" alt="Screenshot 2025-10-24 090302" src="https://github.com/user-attachments/assets/8c14c2b2-3a8d-40b0-b7ea-7ad5d09c6ca6" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="289" height="145" alt="Screenshot 2025-10-24 090328" src="https://github.com/user-attachments/assets/7a31fc74-2199-4b88-b20a-c892fd9b0691" />



cut -d "|" -f 2 file22
## OUTPUT


<img width="285" height="142" alt="Screenshot 2025-10-24 090359" src="https://github.com/user-attachments/assets/92d20e00-2ca7-44f1-a4ae-5e83a1f2d9e0" />


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

<img width="320" height="48" alt="Screenshot 2025-10-24 091841" src="https://github.com/user-attachments/assets/c3f33cc9-2533-4aad-9409-aae696be9b9c" />



grep hello newfile 
## OUTPUT

<img width="317" height="43" alt="Screenshot 2025-10-24 091938" src="https://github.com/user-attachments/assets/e5e2a800-9efa-4afb-9817-a9a3fbf12be0" />




grep -v hello newfile 
## OUTPUT

<img width="320" height="52" alt="Screenshot 2025-10-24 091949" src="https://github.com/user-attachments/assets/30624bf2-06f5-4d69-a577-f38c859d9b71" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="351" height="53" alt="Screenshot 2025-10-24 092026" src="https://github.com/user-attachments/assets/216c6dd7-9940-4384-abff-fcb88984ae05" />




cat newfile | grep -i -c "hello"
## OUTPUT


<img width="387" height="78" alt="Screenshot 2025-10-24 092100" src="https://github.com/user-attachments/assets/abd251a6-8bb2-4b0e-97b2-0f67b96f5814" />



grep -R ubuntu /etc
## OUTPUT
<img width="805" height="184" alt="Screenshot 2025-10-24 092140" src="https://github.com/user-attachments/assets/42db03e6-3ea1-4440-8c1d-7a5c50af48d3" />




grep -w -n world newfile   
## OUTPUT
<img width="333" height="51" alt="Screenshot 2025-10-24 092206" src="https://github.com/user-attachments/assets/4bc03928-cc89-4fc2-b755-86bb2e85579a" />



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

<img width="388" height="105" alt="Screenshot 2025-10-24 092525" src="https://github.com/user-attachments/assets/e19ba4d1-79bf-4080-9e9c-ac89000342a0" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="352" height="101" alt="Screenshot 2025-10-24 092549" src="https://github.com/user-attachments/assets/7dc14a92-2b89-4ab3-8513-1540397dd27b" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="395" height="98" alt="Screenshot 2025-10-24 092618" src="https://github.com/user-attachments/assets/f0ff8503-56ff-44d0-9f53-b972784e7577" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="354" height="79" alt="Screenshot 2025-10-24 092646" src="https://github.com/user-attachments/assets/174bde67-de76-4639-ba4a-6bbdbd398494" />



egrep '(world$)' newfile 
## OUTPUT

<img width="339" height="97" alt="Screenshot 2025-10-24 092714" src="https://github.com/user-attachments/assets/72f99369-feff-47f5-b152-639421f2fccb" />


egrep '(World$)' newfile 
## OUTPUT

<img width="339" height="97" alt="Screenshot 2025-10-24 092714" src="https://github.com/user-attachments/assets/0be61797-0fe5-4aa2-b7a2-829fb1c3b891" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="367" height="124" alt="Screenshot 2025-10-24 092742" src="https://github.com/user-attachments/assets/12caf5f7-4fe0-4f45-b2c3-17436806af50" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="303" height="73" alt="Screenshot 2025-10-24 092806" src="https://github.com/user-attachments/assets/6e6c887e-0b7a-490e-80e8-e11138ca446d" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="362" height="71" alt="Screenshot 2025-10-24 092834" src="https://github.com/user-attachments/assets/009182c1-16af-4874-a12e-1a3febbd4354" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="362" height="71" alt="Screenshot 2025-10-24 092834" src="https://github.com/user-attachments/assets/0ac9091d-68e9-49af-9f93-a09184c5954d" />



egrep l{2} newfile
## OUTPUT

<img width="283" height="90" alt="Screenshot 2025-10-24 092925" src="https://github.com/user-attachments/assets/d2912d9f-04c5-4128-a0ba-8be5a427710c" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="301" height="125" alt="Screenshot 2025-10-24 093002" src="https://github.com/user-attachments/assets/5f802dfa-50ca-4a36-a5ba-178329867e0f" />


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

<img width="311" height="76" alt="Screenshot 2025-10-24 093059" src="https://github.com/user-attachments/assets/37e7193f-79b9-482f-8f80-8181d66783f4" />


sed -n -e '$p' file23
## OUTPUT

<img width="311" height="76" alt="Screenshot 2025-10-24 093059" src="https://github.com/user-attachments/assets/beae74f2-0737-4213-af98-a7e6d4facda6" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="403" height="252" alt="Screenshot 2025-10-24 093315" src="https://github.com/user-attachments/assets/68017d26-1c78-45a8-b6c7-47a029f48112" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="359" height="250" alt="Screenshot 2025-10-24 093343" src="https://github.com/user-attachments/assets/ce5cafd4-3057-4a31-b275-3837ac223119" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT




sed -n -e '1,5p' file23
## OUTPUT
<img width="356" height="120" alt="Screenshot 2025-10-24 093502" src="https://github.com/user-attachments/assets/584a2ba5-b352-4ede-9c31-5c50b6e3060d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="440" height="95" alt="Screenshot 2025-10-24 093528" src="https://github.com/user-attachments/assets/b8c8ef3c-313a-4da9-91f5-c50391a293f5" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="440" height="95" alt="Screenshot 2025-10-24 093528" src="https://github.com/user-attachments/assets/96dffa11-71df-47fd-859a-38aeeec626d3" />




seq 10 
## OUTPUT

<img width="335" height="295" alt="Screenshot 2025-10-24 093552" src="https://github.com/user-attachments/assets/897aaf3f-e62f-4456-9471-56d4c0310145" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="309" height="117" alt="Screenshot 2025-10-24 093657" src="https://github.com/user-attachments/assets/e94c14e6-374d-4465-aa5c-0798bcf2ac19" />




seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="374" height="118" alt="Screenshot 2025-10-24 093756" src="https://github.com/user-attachments/assets/62a5989e-39f1-479d-ae42-671c10d4cca4" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="299" height="147" alt="Screenshot 2025-10-24 093834" src="https://github.com/user-attachments/assets/1ec2a766-2b5b-4d02-aaf7-6cf7d3a57bcf" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="299" height="121" alt="Screenshot 2025-10-24 094138" src="https://github.com/user-attachments/assets/664f6d92-ceae-44b1-838f-315b86323c0d" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="329" height="112" alt="Screenshot 2025-10-24 094201" src="https://github.com/user-attachments/assets/0977cf2b-201e-4d04-82d0-e6b8c6e05a6d" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="377" height="118" alt="Screenshot 2025-10-24 094228" src="https://github.com/user-attachments/assets/9a32f7fa-de46-4e6d-8534-11f4fbda12e3" />



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

<img width="552" height="177" alt="Screenshot 2025-10-24 094834" src="https://github.com/user-attachments/assets/c2da2612-5c67-420e-ab29-9cf6ba588bb2" />


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

<img width="649" height="176" alt="Screenshot 2025-10-24 094926" src="https://github.com/user-attachments/assets/c4ac9f8d-b2de-49b4-8c84-f49eb7b6413c" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="464" height="246" alt="Screenshot 2025-10-24 094954" src="https://github.com/user-attachments/assets/b2dafbb5-69ee-456b-bf6a-141b80a3a560" />


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

<img width="525" height="85" alt="Screenshot 2025-10-24 111005" src="https://github.com/user-attachments/assets/e15e1ca1-660a-4d7b-a216-a455ca17c196" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="538" height="120" alt="Screenshot 2025-10-24 111044" src="https://github.com/user-attachments/assets/b0eb9a50-5070-4470-bbde-4f9be8d0898d" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="509" height="277" alt="Screenshot 2025-10-24 111136" src="https://github.com/user-attachments/assets/4e0d63f0-1734-40d6-a1ab-9d75dd9afbc9" />


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="467" height="266" alt="Screenshot 2025-10-24 111256" src="https://github.com/user-attachments/assets/651713fd-1585-4378-8987-16889f133c4e" />


tar -xvf backup.tar
## OUTPUT
gzip backup.tar

![alt text](image.png)




ls .gz
gunzip backup.tar.gz
## OUTPUT
![alt text](image-1.png)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![alt text](image-2.png)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![alt text](image-3.png)


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
![alt text](image-4.png)



ls file1

echo $?
## OUTPUT
![alt text](image-5.png)




 
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
![alt text](image-6.png)


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
![alt text](<Screenshot 2025-12-03 010257.png>)


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
![alt text](<Screenshot 2025-12-03 010401.png>)



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
![alt text](<Screenshot 2025-12-03 010431.png>)


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
![alt text](<Screenshot 2025-12-03 010431-1.png>)



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
![alt text](<Screenshot 2025-12-03 010459-1.png>)


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
![alt text](<Screenshot 2025-12-03 010529.png>)

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

## OUTPUT
![alt text](<Screenshot 2025-12-03 010555.png>)

 
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
![alt text](<Screenshot 2025-12-03 010622.png>)
 
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
chmod 755 untiltest.sh

## OUTPUT
![alt text](<Screenshot 2025-12-03 010640.png>)

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
 chmod 755 forin1.sh

 ## OUTPUT
![alt text](<Screenshot 2025-12-03 010659.png>)
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
chmod 755 forin2.sh
 
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
![alt text](<Screenshot 2025-12-03 010747.png>)

 
cat forin3.sh 
```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
 ./forin3.sh 
 
## OUTPUT
![alt text](<Screenshot 2025-12-03 010810.png>)


cat forinfile.sh 
```
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```


 chmod 777 forinfile.sh



```
$ cat cities
Delhi
Mumbai
Chennai
```

## OUTPUT
![alt text](<Screenshot 2025-12-03 010848.png>)



cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
chmod 755 forctype.sh
./forctype.sh 

## OUTPUT
![alt text](<Screenshot 2025-12-03 010904.png>)



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
![alt text](<Screenshot 2025-12-03 010943.png>)


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
![alt text](<Screenshot 2025-12-03 011008.png>)

 
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
![alt text](<Screenshot 2025-12-03 011026.png>)

 
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
![alt text](<Screenshot 2025-12-03 011051.png>)

 
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

./funcex.sh 1 2

 ## output
 ![alt text](<Screenshot 2025-12-03 011114.png>)

 
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
![alt text](<Screenshot 2025-12-03 011133.png>)

 
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
$ chmod 777 argshift1.sh
$ ./argshift1.sh 1 2 3

## OUTPUT
![alt text](<Screenshot 2025-12-03 011150.png>)

cat argshift2.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
 ./argshift2.sh 1 2 3

 ## OUTPUT
![alt text](<Screenshot 2025-12-03 011217.png>)
![alt text](<Screenshot 2025-12-03 011230.png>)

 
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
![alt text](<Screenshot 2025-12-03 011253.png>)
![alt text](<Screenshot 2025-12-03 011304.png>)
![alt text](<Screenshot 2025-12-03 011320.png>)

 
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
![alt text](<Screenshot 2025-12-03 011343.png>)
![alt text](<Screenshot 2025-12-03 011405.png>)


# RESULT:
The Commands are executed successfully.

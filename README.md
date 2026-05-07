
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

<img width="420" height="121" alt="image" src="https://github.com/user-attachments/assets/55712b2e-9b4a-4aef-8de2-9050ecad9ab2" />


cat < file2
## OUTPUT

<img width="446" height="181" alt="image" src="https://github.com/user-attachments/assets/1c0ec1b6-7504-4c77-80b6-306b0ec85625" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="491" height="50" alt="image" src="https://github.com/user-attachments/assets/31f1c547-87c1-49e2-9e3f-75f43062bbb4" />

comm file1 file2
 ## OUTPUT
<img width="514" height="275" alt="image" src="https://github.com/user-attachments/assets/90dc0c40-9dc3-4e17-8786-0fad91b55f89" />

 
diff file1 file2
## OUTPUT

<img width="574" height="349" alt="image" src="https://github.com/user-attachments/assets/97817d93-2d4e-449e-a79b-a4f2853043d1" />


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

<img width="457" height="102" alt="image" src="https://github.com/user-attachments/assets/dadabac9-bc9d-4884-8c94-49d9e1c3590d" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="490" height="122" alt="image" src="https://github.com/user-attachments/assets/d24ba347-e640-4fc5-b2c8-fa01e1e563b2" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="516" height="132" alt="image" src="https://github.com/user-attachments/assets/9001e4ed-756a-4532-99f1-05ac88340288" />

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

<img width="520" height="70" alt="image" src="https://github.com/user-attachments/assets/9eb9fe35-ae69-464f-80f7-2c63fce8a799" />


grep hello newfile 
## OUTPUT


<img width="482" height="62" alt="image" src="https://github.com/user-attachments/assets/0a11dd6a-45a3-4286-b6d0-fbdd77abdb1d" />


grep -v hello newfile 
## OUTPUT

<img width="513" height="77" alt="image" src="https://github.com/user-attachments/assets/527bcce3-de33-42ee-936e-9fa81f275639" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="638" height="97" alt="image" src="https://github.com/user-attachments/assets/56f11294-cc7e-405a-9dd2-90a4dcd557d4" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="692" height="69" alt="image" src="https://github.com/user-attachments/assets/7fa60724-d5f4-42bf-af85-3d8c2bb1fe61" />



grep -R ubuntu /etc
## OUTPUT

<img width="745" height="238" alt="image" src="https://github.com/user-attachments/assets/6768e671-90b8-4dea-8171-d38de45a25c6" />


grep -w -n world newfile   
## OUTPUT

<img width="717" height="99" alt="image" src="https://github.com/user-attachments/assets/7289852c-ebbd-4165-b375-4feb2758ea60" />


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

<img width="726" height="96" alt="image" src="https://github.com/user-attachments/assets/6aec356f-3632-4f60-9198-d203552f9528" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="627" height="89" alt="image" src="https://github.com/user-attachments/assets/9130555c-0da7-45a2-8f92-ae10578e436e" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="698" height="88" alt="image" src="https://github.com/user-attachments/assets/525f4bce-a182-4751-9bd0-8d3d42592e1b" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="550" height="69" alt="image" src="https://github.com/user-attachments/assets/916c5898-bc07-4e7f-b437-025675efd185" />



egrep '(world$)' newfile 
## OUTPUT

<img width="581" height="60" alt="image" src="https://github.com/user-attachments/assets/08a999c7-15f1-427a-8b16-54affe4d2c41" />


egrep '(World$)' newfile 
## OUTPUT

<img width="608" height="66" alt="image" src="https://github.com/user-attachments/assets/c2969a4d-1e5e-46b3-b0dd-e72bfa641ebc" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="605" height="92" alt="image" src="https://github.com/user-attachments/assets/19954921-8442-472a-b4c8-0b7165da3be2" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="592" height="68" alt="image" src="https://github.com/user-attachments/assets/83d72f7e-7f7e-4ec8-a41c-748fb1315f43" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="644" height="69" alt="image" src="https://github.com/user-attachments/assets/79a6f589-3704-440e-8214-39a8ef071884" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="619" height="64" alt="image" src="https://github.com/user-attachments/assets/8ff44860-51f6-4508-8329-ea9196bf15fb" />


egrep l{2} newfile
## OUTPUT


<img width="727" height="98" alt="image" src="https://github.com/user-attachments/assets/142dc369-e9a5-40c2-baa0-6650593a27f4" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="732" height="128" alt="image" src="https://github.com/user-attachments/assets/99b65ea9-42e1-4e65-9b80-bbeb615ccc94" />

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
<img width="514" height="59" alt="image" src="https://github.com/user-attachments/assets/e8b77cc7-6373-480d-9dc0-3c9635d9c1b7" />



sed -n -e '$p' file23
## OUTPUT

<img width="536" height="64" alt="image" src="https://github.com/user-attachments/assets/5ad7843e-9cfa-4649-9891-bdfa66483218" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="592" height="263" alt="image" src="https://github.com/user-attachments/assets/bf87cadf-66e4-4f40-bd38-5e4a81009d62" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="595" height="272" alt="image" src="https://github.com/user-attachments/assets/48cfbe51-6f92-4350-aa77-f09fdea954a9" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="648" height="278" alt="image" src="https://github.com/user-attachments/assets/840734a4-15b7-4145-8def-ade5f30863c3" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="592" height="180" alt="image" src="https://github.com/user-attachments/assets/d63aaaa8-1a99-44b5-b18f-a0a1aa687268" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="581" height="119" alt="image" src="https://github.com/user-attachments/assets/93b75801-cc09-4c7a-8468-2ec4acc66ffc" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="636" height="86" alt="image" src="https://github.com/user-attachments/assets/ae6470f2-8268-4ab6-85e8-9f9742d04426" />


seq 10 
## OUTPUT
<img width="556" height="335" alt="image" src="https://github.com/user-attachments/assets/a365c5a0-82b7-4228-9270-b40e4a83fc3b" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="548" height="120" alt="image" src="https://github.com/user-attachments/assets/405fc704-d655-4d47-af2c-39c5d40f956c" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="554" height="119" alt="image" src="https://github.com/user-attachments/assets/b01810c6-6373-4f5a-9d90-15448176e2fa" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="561" height="119" alt="image" src="https://github.com/user-attachments/assets/94faeb18-7699-4df0-8ab4-fccad98a5730" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="562" height="144" alt="image" src="https://github.com/user-attachments/assets/b2538e75-ed7d-456e-bfa5-941a6b851774" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="570" height="119" alt="545144165-95e9cb97-22c0-45c0-8820-a230e7f59c8c" src="https://github.com/user-attachments/assets/1d8162ac-0bd5-4fec-bbfc-3fbe6a66236d" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="573" height="104" alt="545144343-d2d98be5-973c-4ec2-8ad2-c6b0b6d68840" src="https://github.com/user-attachments/assets/5f0816d9-197a-4fe3-9453-8386264ed501" />



sed -n '2,4{s/$/*/;p}' file23

<img width="609" height="122" alt="545144502-0c56dba9-be44-4e58-b04a-f1423593a749" src="https://github.com/user-attachments/assets/0a239bbd-d8dc-4708-b69a-95c025550805" />

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

<img width="406" height="189" alt="545145603-ed21100f-bbc6-4b9b-b66f-d699df00d4a5" src="https://github.com/user-attachments/assets/cebdb370-0b23-452b-bb67-4bebe7b38243" />

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

<img width="380" height="175" alt="545145828-0cffdb69-a350-49ca-8270-3c485d833d42" src="https://github.com/user-attachments/assets/8f300118-f752-4708-966a-d11c30030b7a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="694" height="258" alt="545146387-82f650e5-4399-418d-bb20-4f11827f4771" src="https://github.com/user-attachments/assets/42b55dae-1f5a-4c30-9c77-8f9404630527" />

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
<img width="634" height="114" alt="545146598-f74d7158-c084-42f8-b9ec-88728ed4ac26" src="https://github.com/user-attachments/assets/8fbd1568-50b2-4b80-9a8e-68ff344ae376" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="746" height="120" alt="545146771-5cf4c2fd-f0a5-4979-a4cf-53e2a7162039" src="https://github.com/user-attachments/assets/4a8199fa-571f-4bda-b669-94fca7dfabcb" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="367" height="89" alt="545146971-bc41b3ad-e10f-414b-b7bc-92afa5824782" src="https://github.com/user-attachments/assets/7bc5e076-a4f9-4550-ae43-2a9bfde80442" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="288" height="86" alt="545147259-00b537ca-e543-4a96-bf85-29311e02980a" src="https://github.com/user-attachments/assets/0d491e6c-c3e6-496c-b0b1-88231cae313d" />


tar -xvf backup.tar
## OUTPUT
<img width="766" height="147" alt="545147498-03083874-bade-49d9-a17d-19547af0bd2b" src="https://github.com/user-attachments/assets/85123654-6632-4094-a56b-b995cfd91b16" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="764" height="156" alt="545148181-1c88f035-f696-4021-b688-8a940bfeac4b" src="https://github.com/user-attachments/assets/181e21a8-84bc-4801-bc72-456c8531cb97" />

gunzip backup.tar.gz
## OUTPUT
<img width="767" height="222" alt="545147672-dfd4035a-494f-4ee7-aade-5c221bf38b86" src="https://github.com/user-attachments/assets/c27ec4be-0081-426e-a410-af33ff490424" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="750" height="313" alt="545148413-7c28c780-7a0b-4f0c-b799-df732933950d" src="https://github.com/user-attachments/assets/a7671281-7f3b-42d9-b657-d567a543ad9a" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="433" height="122" alt="545148643-0daafbe0-dd3d-4c14-a827-5d3985fc4dc0" src="https://github.com/user-attachments/assets/6e82a765-d158-4fe3-9a9e-151aa24fb11e" />

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
<img width="538" height="433" alt="545149295-2140d028-d583-4002-a5c4-7e3651bdc75b" src="https://github.com/user-attachments/assets/386b4035-2c9f-4a3f-aa20-c3ca45ba674b" />

 
ls file1
## OUTPUT
<img width="324" height="56" alt="545149418-465d24e0-2051-4163-bc98-9c9051619332" src="https://github.com/user-attachments/assets/f0ae62cf-32e3-4bec-b88c-45ea60313802" />

echo $?
## OUTPUT
<img width="316" height="64" alt="545149647-1cf42cd2-61cd-4ead-be5b-c12e10089544" src="https://github.com/user-attachments/assets/adeff344-58fb-409c-967a-c6c726936079" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="314" height="65" alt="545149758-7958006f-fa7b-400d-a6c1-5c982d12226a" src="https://github.com/user-attachments/assets/212277f3-7b4f-4331-bcdd-24bccf18c888" />

abcd
 
echo $?
 ## OUTPUT

<img width="652" height="299" alt="545149939-7918d027-6ae1-4a2e-9a0b-b5358c92a514" src="https://github.com/user-attachments/assets/6f5bd9cf-9e1a-4fbd-8c8e-3a964228d8fb" />

 
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

<img width="641" height="328" alt="545150168-10774268-d5c7-48f0-9edc-2e5197776f13" src="https://github.com/user-attachments/assets/cef0b3ec-f66c-474b-8b47-8b7bc871d335" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="781" height="316" alt="545150374-d4d8fbbf-cd64-4cc5-a84f-cc47c177da09" src="https://github.com/user-attachments/assets/2b6d872d-5649-4af4-a156-7ccf64019188" />


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
<img width="777" height="233" alt="545151148-74babbd4-573a-40d9-9c7d-58526df5ae08" src="https://github.com/user-attachments/assets/05adc3ca-c9a0-43a8-9656-9e51c24df05d" />

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
<img width="685" height="543" alt="545151395-28dc9b77-a6ca-4809-bf7c-3f19cb250493" src="https://github.com/user-attachments/assets/272b46a5-1028-4267-ac2d-cce356b4245c" />



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
<img width="729" height="648" alt="545151711-5e9d2afe-b172-4c95-9027-4c840e9d89e2" src="https://github.com/user-attachments/assets/45ca2fbe-87a1-4fe1-9f5a-9cdb8b0a8662" />

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
<img width="759" height="653" alt="545151980-02c5e1ae-cf11-4897-978b-b6c60989ac6c" src="https://github.com/user-attachments/assets/632445cd-9acf-4198-a596-163c61848e09" />

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
<img width="755" height="636" alt="545152257-b123a5fc-cc0d-49ab-82bf-1319de072d01" src="https://github.com/user-attachments/assets/1564a81f-8e26-4c9d-831f-49446eacf349" />


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
<img width="682" height="341" alt="545152496-d5251d0e-1e12-4045-ae05-21fb1c8b8e1e" src="https://github.com/user-attachments/assets/6bd3cc1f-0b20-4406-a870-e714eef86b3a" />

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
<img width="565" height="211" alt="545152793-9fb6afb5-b317-4f9f-aa8e-3e111c11166d" src="https://github.com/user-attachments/assets/d1bddfdb-6dd2-403c-a5e7-d99d7d012e97" />

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
<img width="525" height="267" alt="545153002-581f2d22-ff3c-409d-a088-c8e136e2846d" src="https://github.com/user-attachments/assets/e166883a-1be3-4c78-9c83-233a7d18737c" />


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
<img width="513" height="275" alt="545153180-7d3803f8-b96c-4827-a8ac-b08a148b42b8" src="https://github.com/user-attachments/assets/6fcf4d12-f1ae-483f-83f7-529328d79ef2" />

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
<img width="770" height="297" alt="545153395-25ba4cb4-cdd0-416d-8c17-22bffc26e7d0" src="https://github.com/user-attachments/assets/65d0218d-bcab-48bb-94fa-6e53efbbe758" />

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
<img width="769" height="286" alt="545153661-ac8f2555-f104-4537-83c2-2cc24f7bb960" src="https://github.com/user-attachments/assets/044a3b75-5072-404c-910d-657a1c63f48d" />

 
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
<img width="775" height="290" alt="545153906-e06e0388-c19d-453b-908a-37ecd2afeb99" src="https://github.com/user-attachments/assets/d293014c-b51d-47b1-b68f-29c946e9760a" />

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
 <img width="721" height="294" alt="545154087-87b5c3d5-abe8-43e3-8199-2f7ad3d5f96f" src="https://github.com/user-attachments/assets/099513a4-d6de-48b8-8dc5-4c483ab91f04" />

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
<img width="586" height="183" alt="545154266-24ebcfb4-7f43-4db8-a91d-0f4d133f6ae0" src="https://github.com/user-attachments/assets/422ea7b7-5af1-4245-8a44-e7a156843542" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="642" height="142" alt="545154445-f16d5720-2c94-4019-8ed8-0f0d3d161c88" src="https://github.com/user-attachments/assets/d5571d78-ab76-4061-9696-0153b52df6de" />


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
<img width="401" height="18" alt="545154849-3b14d772-c1a1-4a09-917d-6b6904cd181f" src="https://github.com/user-attachments/assets/dd605f21-37e0-4ac1-94ba-c93c77dd82b1" />

 
 ./funcex.sh 1 2
<img width="457" height="22" alt="545155035-9cc6b7f6-4b23-4d2e-bb6a-218d7ac39741" src="https://github.com/user-attachments/assets/5a85d8db-e126-4136-b706-49d9e62a94e4" />

 
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
<img width="226" height="57" alt="545155301-696cebbe-722f-4032-9c1d-90dcf6c6f5c1" src="https://github.com/user-attachments/assets/0650b6d3-019e-4fa6-9724-585d79bbf189" />

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
<img width="191" height="69" alt="545155499-bed3212e-6157-4d47-8699-b2996d79f714" src="https://github.com/user-attachments/assets/8eafc743-f1c8-4378-902e-28b25590c4a0" />

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
<img width="660" height="369" alt="545157195-0a178336-a3e4-447b-ad76-dfee7e6af668" src="https://github.com/user-attachments/assets/8e0127f8-9801-44bd-968c-a0380346e8cd" />

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
 <img width="457" height="245" alt="545157299-f8b4c03b-37cd-4b1a-88c4-47a1f0bf955e" src="https://github.com/user-attachments/assets/aad64841-ab71-48a4-b970-bb3ed1e0a325" />

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
<img width="682" height="371" alt="545155769-056eb38a-1c8a-4c4d-bdb9-47d5129cfa78" src="https://github.com/user-attachments/assets/eb32875f-845c-46a6-bb4a-3061786935d7" />


# RESULT:
The Commands are executed successfully.

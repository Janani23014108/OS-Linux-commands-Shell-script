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

![378188160-a57bbcc5-53a5-42ab-a95a-b1573d3a592a](https://github.com/user-attachments/assets/32b996cf-dd48-4ca2-b4b4-81592074735f)


cat < file2
## OUTPUT
![378188173-02b69943-eeab-4674-9521-3f6943ccaa51](https://github.com/user-attachments/assets/0cdb6c76-a513-402c-88c5-d5d46708a479)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![378188180-ccd7b31e-2a62-4603-8685-912f40627687](https://github.com/user-attachments/assets/0c9299fe-3049-4855-b790-9ea9df578b59)

comm file1 file2
 ## OUTPUT
![378188190-7d6c587d-a051-4734-b311-b3a07a4e87dc](https://github.com/user-attachments/assets/ea3a7f3f-6061-4975-b0fe-528a479aaec1)

 
diff file1 file2
## OUTPUT

![378188210-63107886-c989-42ee-9119-a7b18dc75e65](https://github.com/user-attachments/assets/b8833762-ff6b-4f91-b84e-359bb473a8e9)

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

![378188220-2e7e71b1-91c6-44bf-8718-4e767322356f](https://github.com/user-attachments/assets/9407a2ae-b2b7-4ce3-a5c9-7ca09346a74e)



cut -d "|" -f 1 file22
## OUTPUT

![378188248-edc0e1f0-fca0-4e4a-ae52-8bb370c8131d](https://github.com/user-attachments/assets/c551c917-dde9-45d2-a4d6-8111b7953425)


cut -d "|" -f 2 file22
## OUTPUT

![378188266-4990326f-1a51-45a3-bca5-f50e77ecb5ea](https://github.com/user-attachments/assets/2df1d101-6c2c-401b-8102-91e3fa597f90)

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
![378188277-33015d7a-bd9a-4400-9a39-edce4b2582ff](https://github.com/user-attachments/assets/6d51736d-f110-4786-9816-db30767f9884)



grep hello newfile 
## OUTPUT

![378188284-082911e4-5f8e-423a-9877-412307ceb1c4](https://github.com/user-attachments/assets/0fa9a6e3-915d-42be-8d56-f10d9f461462)



grep -v hello newfile 
## OUTPUT
![378188295-cb8eefc3-5d28-4657-93d8-a83a472a7d65](https://github.com/user-attachments/assets/35c0c984-febb-42fa-b398-e8185a9589ff)



cat newfile | grep -i "hello"
## OUTPUT

![378188304-5147f8c9-347b-46d9-a4f2-a47911ca90fa](https://github.com/user-attachments/assets/93a2550a-252b-46e3-8ded-8abdb892f9c4)



cat newfile | grep -i -c "hello"
## OUTPUT

![378188323-94f49554-1ad1-4420-bfab-2c58cec56818](https://github.com/user-attachments/assets/139dbfd0-06cf-4b0f-ad84-d9baedb6a780)



grep -R ubuntu /etc
## OUTPUT

![378188350-fe63d40e-6773-412d-acb4-6d0120468dc0](https://github.com/user-attachments/assets/8936ffc9-fa91-470f-9a78-adb2d748911e)


grep -w -n world newfile   
## OUTPUT
![378188373-1c7c6bda-6636-43c5-95d8-b8f828628482](https://github.com/user-attachments/assets/a5566bca-9604-44e9-8505-133082098137)


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

![378188385-a9e483ec-0c41-405e-bb29-3fed12c4cac0](https://github.com/user-attachments/assets/4fb81d31-87a1-4861-adae-dec05b73e016)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![378188388-9a616b71-ac26-4cbf-bcd6-0b4319cfab7a](https://github.com/user-attachments/assets/b36d7430-b49a-4f91-9fee-e8c58ba3546d)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![378188395-daeaeed8-42e7-464f-8f8d-ff5ca98040ef](https://github.com/user-attachments/assets/da399080-7c42-44a9-89c7-893cd67dac88)



egrep '(^hello)' newfile 
## OUTPUT

![378188398-3dc810c7-e48f-4660-936b-5b91050644b5](https://github.com/user-attachments/assets/e0ebc836-86f5-43e9-b960-37c6b73cacc8)


egrep '(world$)' newfile 
## OUTPUT

![378188405-ff733263-c707-4aa3-9f32-b6d0fc611ed3](https://github.com/user-attachments/assets/0938db52-d384-48eb-94a5-70d11259528a)


egrep '(World$)' newfile 
## OUTPUT
![378188415-b3285124-3e11-4af7-a98e-0bd6b5126165](https://github.com/user-attachments/assets/52a20e60-f306-4028-8089-9a6d58aa04a4)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![378188419-9e85dc5b-f974-4938-bab1-395680090d98](https://github.com/user-attachments/assets/ceed10d3-43f5-4039-9d89-c81dda3ed06a)


egrep '[1-9]' newfile 
## OUTPUT

![378188426-e6dcbee0-c809-4028-a6c5-76ba596cd93d](https://github.com/user-attachments/assets/731dcd9a-1a3c-484f-90e0-ddd95a536193)


egrep 'Linux.*world' newfile 
## OUTPUT
![378188431-06261923-c788-411c-a36e-39e42f34e336](https://github.com/user-attachments/assets/fb491189-aa66-4ed1-aa5a-99107cc9ae5e)


egrep 'Linux.*World' newfile 
## OUTPUT

![378188454-c842bb59-b1ba-41f5-9fd5-72ba27a5aa83](https://github.com/user-attachments/assets/71cb7f24-3325-4a39-b0b0-ce53d53ded46)

egrep l{2} newfile
## OUTPUT

![378188464-08642e5e-08be-4ec7-bcba-20aef8d8b68f](https://github.com/user-attachments/assets/d2609284-cb45-4e73-9eca-9885feaa28b4)


egrep 's{1,2}' newfile
## OUTPUT 
![378188469-95c6e208-d704-47cb-b692-fd264bf95e8d](https://github.com/user-attachments/assets/f936ada5-fc61-46c1-ae94-f915949eed78)


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
![378188478-bc13707f-b20e-49a0-854b-c33ebb122b86](https://github.com/user-attachments/assets/c46a0ea6-f40e-453c-a372-af4336e4be6f)



sed -n -e '$p' file23
## OUTPUT

![378188483-794fcb6c-d6c6-48be-b4e9-4affa4f45e47](https://github.com/user-attachments/assets/a5fc6c47-05d8-4e7a-bba0-c11685de2432)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![378188491-e96317a6-b36e-4282-9c6f-b83916b53cba](https://github.com/user-attachments/assets/e7d617b0-a32b-44b5-ba39-122c26f59e08)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![378188508-cdf4d9b1-afb6-4550-ab38-8cac3fb01b36](https://github.com/user-attachments/assets/b2d750c3-5296-40ea-b307-f5aac670faba)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![378188513-96ac7379-326e-4c25-90d4-0eb59d108d64](https://github.com/user-attachments/assets/54b9705f-74aa-4d34-8393-22fb0af7a2c5)


sed -n -e '1,5p' file23
## OUTPUT

![378188521-afdaceb4-87a5-4933-9d94-058353dbeef9](https://github.com/user-attachments/assets/fb1c936b-6aa4-4ef6-84e9-d1d5ba219783)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![378188544-607070e1-3801-4b6f-bdb3-ad6d81cad476](https://github.com/user-attachments/assets/c2d1869f-3792-4bde-8407-303417831877)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![378188556-c9af429f-1574-4c0c-9a9e-b7358fa70639](https://github.com/user-attachments/assets/d83246c0-3e0e-4f4f-9434-f3ec1cba4477)

seq 10 
## OUTPUT

![378188563-0e0fb4c3-6479-4e3d-b480-e6c83690a6eb](https://github.com/user-attachments/assets/997b538e-b6ec-4add-89c5-d2cca1b1346e)


seq 10 | sed -n '4,6p'
## OUTPUT

![378188586-fc325015-cfe6-4c7e-818e-f189f8cd56fa](https://github.com/user-attachments/assets/7bf85676-d101-47d5-babc-5cd301b5672f)


seq 10 | sed -n '2,~4p'
## OUTPUT
![378188591-fd7c6cf4-bf93-42ff-aa1f-576494b3ea53](https://github.com/user-attachments/assets/fce9ebc2-043f-4a8c-93fb-baccf2955eca)



seq 3 | sed '2a hello'
## OUTPUT

![378188612-fbeb2d4d-47e5-4712-a516-7e866e1814ec](https://github.com/user-attachments/assets/5af39b08-d93c-4f82-8864-4214caa52a9e)


seq 2 | sed '2i hello'
## OUTPUT
![378188626-80b2dcb1-bd3a-42d5-b9a9-b5df5c3a117a](https://github.com/user-attachments/assets/d0ab0c0f-2330-4cfc-a83c-a04ee5c56e39)


seq 10 | sed '2,9c hello'
## OUTPUT

![378188632-ff05324d-4713-430d-ba45-946964447179](https://github.com/user-attachments/assets/d45471e1-4445-4de7-b904-9d046921f4e7)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![378188639-76cfefb1-bf43-44e8-a750-485dcd825d4d](https://github.com/user-attachments/assets/579b85bf-26be-4b5c-9aca-f8186c844a12)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![378188666-d8b8550f-e827-4e2e-bd12-8ee4b35be4de](https://github.com/user-attachments/assets/c43aa97e-9dfd-4761-a92e-0f8701ef022d)


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
![378188676-eac2e945-6653-4422-8582-87228bd34483](https://github.com/user-attachments/assets/0577bfb2-dbad-4e00-b2b9-3201997d66b1)


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

![378188688-8641b525-8737-440f-9b7d-7d27c42e7603](https://github.com/user-attachments/assets/95488f8c-79d9-4fe8-95d3-271af0702fc3)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![378188702-40153662-b888-4ce2-a62d-f9d19b0dae28](https://github.com/user-attachments/assets/34f876e8-305b-4fb4-821a-6f791201b384)

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

![378188711-ef013a03-8cc5-4cd5-aa78-aac36db878f3](https://github.com/user-attachments/assets/c69d2591-0b51-442d-8606-88fb2fefe3bf)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![378188722-f5a138e7-9913-4f26-af94-9b62fe69b708](https://github.com/user-attachments/assets/452eee35-4a99-4967-9fe0-206a4cd6a344)



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![378188737-6a798d35-dbbf-43ab-8e47-717a5cc1783e](https://github.com/user-attachments/assets/dc3ae1e7-b33d-4357-ad8a-9ccb2dcf9016)


tar -xvf backup.tar
## OUTPUT
![378188755-c3f2985b-a499-47d4-aa92-9af2848d924f](https://github.com/user-attachments/assets/a0f05014-5a3a-4aab-ae78-ac4169d9c597)

gzip backup.tar

ls .gz
## OUTPUT
 ![378188811-154cfaae-e69f-4f20-b85c-e807e36e1868](https://github.com/user-attachments/assets/5cf3ac10-5aca-402c-8d5d-05a48b98034e)

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

 ![378188831-36eb897f-db6e-4896-adf4-d4fe5ce96429](https://github.com/user-attachments/assets/b4f090df-99b8-4fa7-ba01-3b98c30f13f6)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![378188850-ec03ed36-ba6d-4eff-af34-3c104a978bae](https://github.com/user-attachments/assets/c12f5612-73f7-4810-8a77-49f85ab89414)


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
![378188858-fa266f9d-a128-4197-9317-62fe0cb653e4](https://github.com/user-attachments/assets/4e4b16d9-98d6-404c-ae5f-796dd933ba43)

 
ls file1
## OUTPUT
![378188869-1a1c8f31-0522-40e0-9fd8-8727ba3012e1](https://github.com/user-attachments/assets/58620549-e863-489e-932d-8f167a4ab8d7)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![378188899-f2e61dc6-24fc-4e48-a9da-0e4aabc0087f](https://github.com/user-attachments/assets/49dfe9a1-5a19-4196-9620-e5f16c544762)

abcd
 
echo $?
 ## OUTPUT


 ![378188906-14942117-1054-4436-8c30-6c505da1a7a0](https://github.com/user-attachments/assets/7f8491b7-7f5d-4a6f-93c9-ddd24dec18d2)

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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![378188916-b0aaa81a-ebbf-4989-a91c-949f0b9534ed](https://github.com/user-attachments/assets/b05e1978-7fa3-42ba-807e-49e795e90465)


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
![378188929-f0ac1f47-6542-4c7d-83a2-d8c467214dde](https://github.com/user-attachments/assets/ac7a1bfb-e5c2-4231-b87c-4809b1866e76)


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

![378188943-c1f68c70-eafa-4a88-93f3-86b459568244](https://github.com/user-attachments/assets/89039f37-2e07-46b6-9cd1-f89b72f26246)


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
![378188970-661713cf-bdb2-47e7-93cf-28ed5ce978b1](https://github.com/user-attachments/assets/93a66daf-14df-482f-9047-0e67de3d754b)

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
![378188987-e48c55c5-5fef-4e18-9e86-4223a0b44ce0](https://github.com/user-attachments/assets/35572eec-518a-4a18-9d56-fe7f64c6e02d)

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
![378188993-c1bc5615-f861-4a04-b908-60235a747e18](https://github.com/user-attachments/assets/871197dd-c898-44c1-9c50-7617ffdd30b5)


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
![378188987-e48c55c5-5fef-4e18-9e86-4223a0b44ce0](https://github.com/user-attachments/assets/56f16d72-9390-46ae-8953-e358b8d91c51)

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
 ![378189189-96112688-b88e-459a-bab6-ce5278339ea3](https://github.com/user-attachments/assets/b805c0b6-4cbb-49c3-a19b-04b4bb3189a5)

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
 
 ![378189210-4ecfed5c-e79e-409c-95e4-16d0d7de830a](https://github.com/user-attachments/assets/6219989c-522f-46ce-b592-35c6e7d8b81f)

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
 
 ## OUTPUT
 
 ![378189236-6033c2d8-dab8-4512-99cb-83f736af747a](https://github.com/user-attachments/assets/31475292-c1d1-4322-bd61-ad00bacbfa00)

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
 ## OUTPUT
 ![378189328-e96cac5b-2d74-4c9a-a2ca-7844f3ba75e7](https://github.com/user-attachments/assets/481ce299-dbd8-4569-a78d-b47b0498cde0)

 
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
 ## OUTPUT
![378189354-945b036e-e5a5-4aa2-8029-244297a98c3d](https://github.com/user-attachments/assets/f88de1a8-b3ef-40fa-aeaa-e05076ab6711)

 
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
![378189354-945b036e-e5a5-4aa2-8029-244297a98c3d](https://github.com/user-attachments/assets/169218e1-c978-4437-aeb7-ba25b0dc967b)

 
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
 ![378189423-193873b1-71b5-40cb-bc0c-02f5a65ff5ef](https://github.com/user-attachments/assets/d0979510-4290-48fe-b4a2-cc428c3445e1)

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
![378189457-1305c3c5-e96f-427a-8eb1-75a6267bb28b](https://github.com/user-attachments/assets/e6d78713-5996-4bb3-b178-f77f1b04df48)


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

## OUTPUT

![378189479-cb9dfa4f-5896-4ceb-911f-f5649f400ac4](https://github.com/user-attachments/assets/b5fde905-b478-44c1-8ed4-8617a8081bf3)


$ chmod 777 forinfile.sh
$ cat cities

## OUTPUT
![378329951-041142f6-65ee-46b2-a0cc-aaa2a735aa54](https://github.com/user-attachments/assets/4b3ee7eb-6a9f-4c39-8342-0f1771d39349)


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
![378330005-b705e55e-51ee-4400-9a02-2990bd78fd3a](https://github.com/user-attachments/assets/dee64f6f-e71a-47c6-9ae9-bea3ec7235e7)

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
![378330067-3a4510cc-92ef-455e-947c-57b60b3e1923](https://github.com/user-attachments/assets/39efe7eb-2324-4e86-9f90-d86ca3da987e)

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

 ![378330136-dd32ae9d-03f7-45b5-a13e-337f807f5ea9](https://github.com/user-attachments/assets/48fd1621-795c-48e9-8893-920dde41a012)

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
![378330267-e9720aca-556d-4af1-bfc4-63f5189e2965](https://github.com/user-attachments/assets/aa5abd45-1c5c-493b-85f8-71fcb88a1544)

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
 ![378330327-0ac87190-a1bf-4034-a266-d151c166db2c](https://github.com/user-attachments/assets/f7b03af2-07b7-447a-84e7-7b50f41bff9e)

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

![378330371-18af2b0e-4cfc-4aaf-bb97-126c789628e8](https://github.com/user-attachments/assets/ac76fc53-8498-46e2-9c75-af3354828f5e)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![378330404-4652bcf4-de5e-46f6-8f53-988fece8117e](https://github.com/user-attachments/assets/e1486db4-b591-40e5-9657-79d9d7c583eb)


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

 ![378330471-27f8f964-0f4b-471f-bbe2-a5df7e74277f](https://github.com/user-attachments/assets/1b83f102-877f-4d5e-9490-0e66a9a25ae2)

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
 ![378330689-b9f522ff-18dc-4915-b784-88c593bf116f](https://github.com/user-attachments/assets/51a06be6-95cf-40f3-87a4-e246f7b862a0)

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
 ![378330775-56f185d3-c4c9-45ed-a12d-23e53efc91a7](https://github.com/user-attachments/assets/be8abb1b-ec46-41b7-977e-a397051d1c28)

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
 
 ![378330845-b140fe9a-9a9f-4ae9-b6fc-60c4f09514bc](https://github.com/user-attachments/assets/fab36b51-2bde-4ca1-814f-cb266265b0b4)

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
 ![378330991-69bed850-7e60-459b-911d-3089821e7a20](https://github.com/user-attachments/assets/8820addc-f5c9-462e-8f24-b5bd5d03edf2)

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

![378331043-dfe2b770-6374-4445-a87b-70551156f294](https://github.com/user-attachments/assets/a252127b-6284-4c6c-aa1f-0299d076b3f2)

# RESULT:
The Commands are executed successfully.

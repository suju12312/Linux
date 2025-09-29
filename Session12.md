## user managament

root has a unlimited power
user has a limite dpower

useradd popl2
adduser pop1234

User 
1. add accound useradd
2. deleteuser userdel
3. userhelper
4. usermod 
5. users

users 
root root :op

useradd

GUI --- CMD ----- FILE
USERADD(STORING INFO IN A FILE)

usseradd krish123 (stored infile)
7 to 8 have enry of the user

/etc/passwd
vim /etc/passwd
/etc/shadow
/etc/group
/etc/shadow
/home/dir

create delete user ----> /etc/passwd--->does user exist or not

passwd has 7 fields seperated by colon
login name : password: uid: giod: comments : homedirectory: shell

root:x:0:0:root:/bin/bash
useradd jack
passwd jack
vim /etc/passwd
id root
id jack (not exisat because when login from command prompt they always go to /etc/passwd)
dont try with root account because root login notwork andif login again then not work because they rdit the info

whoami
id root

2nd field is password 
x --> link---> /etc/shadow
secuirty reason (passwd file eadable to eveyone)
so passwd store in /etc/shadow 

if remove x then unlink ith password

uid = userid 
username ---> login ---> os (uid)
vimal ( unsestand user with id  have yuinque id)
powered is confirmed by id not name
root = uid = 0 (any user has id o has unlmitewd power
)

1000/74/80 -- third field ---third id (unique id)
username --- login ---- os -- uid

vimal working with company with 1000 uid \
he koe user passwd means vimal passwd not root passwd
so he cant useradd command cant open /etv/shadow
so what he can do is vim /etc/passwd
vimal:x:0 

vim virus.sh

sed -i 's/vimal:x:1000/vima:x:0'  /etc/passwd

bash virus.sh

vimal 
[root@loalhost ~]#

 
GRoup ID: /ETC/GROUP PERMISSIONS (upcoming sessions)

coments GECOS --- STORE SOME EXTRA INFO ABOUT USER (FULL NAME) IF NOT NAME THEN TAKE FROM LOGINNAME

[root@loalhost ~]#VIM  /ETC/PASSWD
vimal:x:1000:1000:Vimal Daga: (vimal daga is full name)
adv is when login from gui then full name will come

[root@loalhost ~]#finger (this have capablity to do all info ) vimal daga,lw,9372264203

comments/gecos/finger
man passwd (red manual of the file)


passwd -- to change passwd -- cmd name
/rtc/passwd --- file name but both have diff uses

man 5 password

pwconv(8)

who

idle:do not do anything

pinky (name full name of user)

users

man users
man who
who -q
man w
w user
w
login ---- o.s -----landed on one of directory

pwd op:/root
home directory is first because it gives feel of safety , organized /home/vomal 
cat > mybank
ls
pwd
ueradd yash
pwd
/home/yash
cd /hme/vimal (permission denied)
root has priviledges

/ ---/home --- vimal --yash ------sujal

/home/dir -create home useradd done ythis 

[root@loalhost home]# useradd sarah
passwd sarag
pwd 
/home/sarah (useradd this directory) (home:directory)\

vim /etc/passwd
sarah:x:1024:1024:sarah:;/home/sarah:/bin/bash
sarah:x:1024:1024:sarah:::/bin/bash
login woith sarahh
pwd
op: /

mkdir /homer/monkey

useradd ttuser1
cat /var/log/secure (kuch nhi chnage hota ahi th yeha sabtack kar saktre hai)

monkey::1024:1024:sarah::/home/monkey123:/bin/bash (cant traqck by log)

/bin/bash (next class)

whenever login --- after login -- in cmd (behind scene bash shell is running) 
asgfh
/bin/sh
bwhen we write command behind scene shell is there t run that

if dont want too shell give : /sbin/nologin (after login auomatically u logout)




 







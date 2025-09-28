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

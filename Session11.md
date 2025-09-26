# secuirt relate to user management


h.b ---- > os (we wnt to say identty)(username or account name)

#date
cmd ---> ----> progrsm ---->file -->stored in hard disk ---- process (after load on ram)

o.s say to executr a program only allowed when u say identity

identity? is every user has differernt power  such as sujal user root account

priviledges (power) 
cat /etc/shadow (only rott account can see)

root account disabled for login
cmd:
useradd sujal
 suppose i want to run tewo command 
 yum useradd but not from root so how?
 useradd lwusr
 passwd lwusr
lwuser ----> give extra power so that this cxan run command those root can run only we have to provide list of command is known as priviledge escalation.
sudo through wicvh we give extra power 
vim /etc/sudoers

sujal  ALL=(ALL) ALL
sujal  ALL=(ALL) /usr/bin/yum
sujal  ALL=(ALL) NOPASSWD:  ALL

username          cmd and pgm name
:wq!

yum install httpd (not run) 
because we give power via sudo 
so sudo yum install httpd
which yum op: /usr/bin/yum

but we have to give passwdv of user

/usr/sbin/useradd

never write all

 VIMAL ---> SUDO ---> BECOME --- ROOT (SUDO == BECOME)
id
uid = userid 1000
sudio id (change vimal id rot) as uid=0
sudo -l
cd /etc/sudoers.d/
vim /etc/su

vim /etc/sudoers

last account create make as sudo users(wheel)
vim /etc/group

wheel -- any user belong to this grp have all power 
sudo -i
ALL=(ALL)  IP ADDR:(ONLY VIA SSH)
sudoedit 
sudo

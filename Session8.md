Servers ----> web (http)
-------->mail (smtp)
----------> DB (mysql)
----------> Remote login (ssh)


Remte login services

Syste m A ---> login (GIVE USER AND PASWORD) ---> AUTHENTICATED
LOGIN  ---> LOCAL
------> REMOTE LOGIN

a -----------N/W-------> LOGIN b
i can use b from a therr program , cmd , resource etc


(remote login server)----
                        |
                        |
rsh protocol telnet protocol ssh protocol

s -> secure way to connect
s-> shell
- ssh server

confihure any server
1: install a software

# yum install openssh-server
2: configure the fle
# vim /etc/ssh/sshd_config
3: service/daemon
systemctl start sshd

configure client:
1) win OS: do you have any clint software? ssh or putty(software)
2) connect to server (by knowing ip address)
ssh -l root 192.168.1.2

[root@localhost ~]# free
[root@localhost ~]# lscpu
[root@localhost ~]# exit
[root@localhost ~]# systemctl stop sshd
[root@localhost ~]# systemctl start sshd
[root@localhost ~]# netstat -tnlp
[root@localhost ~]# 

putty 
hostname 192168.1.2 22 ssh
hostname root@192168.1.2 22 ssh
do saved in save session

moble: ssh app

command line is known as shell

vim /etc/ssh/sshd_config

Port 1234 (unused only do netstat command and check once)

systemctl restart sshd
getenforce
setenforce 0
semanage port -l (tell us which port is allowed ) by Selinux

getnenforce

systemctl restard sshd

\
windoe nd:
ssh -l root 192.168.1.2
ssh -l root 192.168.1.2 -p 1234

User  --> root vimal 


useradd harry
passwd harry
id harry
root (unlimited power)

su - harry
whoami
su - tom (limited power)
always keep root account disabled

PermutRootLogin prohibit-password
ps aux | grep sshd

PasswordaAythentication no
Banner /etc/mybanner
vim /etc/mybanner
sdmskdsmksmkdmmkmcmdc

ssh -l root 192.168.1.2 date; cal
git bash considered ; as terminate 
so dare will run 
after that semicolon the command treat as wndow comamand

ssh -l root 192.168.1.2 'date; cal'

login ----> Auth (user/pass) Password Authentication
passworless authentication (user  key)
key is like daa one big file
CLINET(CUSTOMER) ----------------------> SERVER(BANK)
BANK HAS LOCKER (UNDER DATA) HAVE GIVE BANK KEY AND CUSTOMER KEY THEN LOCKER OPEN
BANK GUY = PUBLIC KEY
CUSOMER = PRIVATE KEY
IP , USER , PRIVATE KEY AND SERVER PUBLIC KEY (MATCH THEN AUTHENTICATION DONE)
CLIENT MAKE PUBLIC AND PRIVAE KEY (PUBLIC KEY GIVE TO SERVER)

ssh client(private and public key) ---------> connect ----> ssh server (account suppose vimal attche dpublic to that)
if client login to vmal then it authorized fastly because of attachment

useradd jack
passwd jack

ssh jack@192.168.1.2
ssh-keygen.exe
.ssh/id_rsa (private key)
.ssh/id_rsa.pub (public key)

enable public key based authetication
at client side:
#ssh-keygen
ssh-copy-id jack@192.168.1.2 (public key)

at server side
disabled passwordautheticaton no
pubkeyauthenticaton yes

systemctlrestart sshd
su - jack
ls
ls -a
mkdir .linux13 (hidden)
cd .ssh/
ls
cat autorized_keys
cd ./ssh
vim authorized_keys
cp /hpme/jack/.ssh/authorized_keys .
cat autorized_keys
ssh -l root@192.168.1.2

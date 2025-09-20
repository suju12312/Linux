## sesssion 6

Server 

Anything that served someone is known as srver

A ---------------------------> B
  data -----  ---- ---- ---->> send data minimum requirement is: 1) netowrk 2) ip addrerss 

first data come to address before reached or send
program is one who send data and receive data

cncept : one buildong there is no human being so our responsibility to take datainboxkown as packaet and intop of that we have to write addrerss known as packet header 

every server has a unique number known as port number 
web server : 80
mail server : 25
ssh : 22
dns : 53

https: 443


http://ip:port/page ---> schema of url

rpm -q httpd
cd /var/www/html
cat lw.html
pwd
sytemctl start httpd

systemctl enable httpd (means when reboot system  automaticallt behnd the scnee it will start)

systemctl stop firewalld

netstat -tnlp  
not all program hads port no but who  do some work with network thn it will has port no

ss -tn -l -p

configuration (every server come with setting file)
eg : for apahe it show in /etc/httpd
cd /etc/httpd
ls
cd conf
ls
vim httpd.conf
Listen 80 (by default)
Listen 81 (can change)

server process in ram and cnf change in hard disk so we have to restart thr file

systemctl restart httpd

one server can have multiple port no

0 -65535 (2^16)

port = 2 bytes

Listen 1234

(it is correct but show error becaus eof security Selinux )
http = 80 8080 81

getenforce

setenforce 0
getenforce
OP: Permissive


systemctl restart httpd

netstat -tn -l -p

then 1234 will be run


setenforce 1
getenforce

now 1234 will nor run

cd /var/www/html/

ls
vimal.hyml


vim /etc/httpd/conf/httpd.conf

op: DocumentRoot "/var/www/html"

if we want change can do like /var/www/sujal

but not try to xchange in main conf file

sECONDRY FILE IN apache as conf.d/ (do change iin this)


cd conf.d/
vim vimal.conf
Listen 81
DocumentRoot "/var/www/vimal
systemctl restart httpd
curl (client command from website)


mkdir /var/www/vimal

ls 
cat > lw.html

pwd 
/var/www/html

cat > lw.html
hihi\cat lw.html
hiii

cat >> lw.html
bye


cat lw.html
hhi
bue


cd /var/www/html


always give priority to secondry file



systemctl restart httpd


indexx.html (homepage) 

it will open because it is index page 

services === daemon

DirectgryIndex lw.html index.html

1  ---> package
2----> configuration file
3----> daemon

ip c---> public and private


network ofnetwork is internet


jaipur -----> internet (public id ) ----->  singapre

private --> wifi  (lan) == private


public ip --- not work ----> private no connection 

how i kow wheter ip is private or not?

private ip is free   range is there 
public p is paids (montly bill )



ngrok software (gives public id )

 
tar -xvzf
ls 
ngrok
ls
./ngrok http 80
authtoken 

./authtken

scp ngrok-v3-stable-linux-amd64.tgz root@192.168.1.2:/root


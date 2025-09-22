Web server ---> 
1) install server
2) configure server
3) start services

advanced conf today



Networking ---->  need network card where we apply ip address

 network card ---> vrtual card ---> ip
 ifconfig 

 enp0s3 ---> 1.2 (ip address)


 ifconfig enp0s3:1 (createnew ntw card)
 ifconfig enp0s3:1 11.2.32.2(createnew ntw card)


ping 12.1.1.1

one os ---> rhgel 9
(we can install one software)

systemctl statusd httpd

ss -tnlp

from one server we can host one website

but just in one os one software can be host multiple website together

ifconfig
mkdir /var/www/lw
cd /var/www/lw

cat > index.html
ls
cat index.html
ls

mkdir /var/www/ibm
cd /var/www/ibm

ls

cat > index.html
ls


mkdir /var/www/india
catr > index.htm
ls
cat index.html


cd /etc/httpd/conf.d

cat vimal.conf
rm vimal.conf
ls
pwd
vim myweb.conf
<virtualHost 192.168.1.2:80>
DocumentRoot /var/www/lw
</vrtualHost>
<virtualHost 11.1.2.3:80>
DocumentRoot /var/www/india
</vrtualHost>
<virtualHost 10.1.2.3:80>
DocumentRoot /var/www/ibm
</vrtualHost>


client 

http://11.1.2.3:80/ndex.html

vim mywb.conf
systemctl status httpd
systemctl rerstart httpd
netstat -tnlp

curl http://11.1.2.3/index.html


shortcut 

esc
yy - copy
p - paste
u - undo

shell c----> alt + .

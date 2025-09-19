 To interact wit os cli / gui / webui


 to get cli three difeerent way 
 1) local login (physiclly available) (localhost)
 2) remote login
 3) webui
 
 A -------> B
     LOGIN    (REWMOTE LOGIN)

CAN CONNECT FROM A TO B  BY NETWORKS


SUPPOSE A (WINDOWS)
B --- > LNUX VM

PROTOCOL ---. IF WE WANT TO DO SOMETHING FOR REQUIREMT FROM ONE COM TO ANOTHJER COMP THROUGH NETWORK 

FOR CONNECTION WE NEED SSH

A --------------> B
  PROTOCOL:SSH

  - - - - - (PACKET)


SSH -L ROOT 192.168.0.1

Linux Server:
what is server?|
whoever serve us is server
who taking services called client

client -------- server
there are many server as mail , seach etc

Web server

web page created now want to create all over thr world can seen taht page

clinet ---- chrome

web page copied on one computer known as web server


os : vm
copy webpage
--> start a program

----> to serve the page is duty (hosting webpage)

Setup any server:

step 1: Installl vlc software
step 2: configure the vlc player according to your requirements
step 3: star program

step 1 : instal softwre for web server
step 2: CONFIGURE WEB SERVER ACC TO REQIREMENT
step 3: start the program


web server : httpd (sftware name)

rhel 9.2 (os) 192.168.1.2 (apache web server)

client == windows
n/w  (protocol == http)

#yum install httpd

rpm -q httpd

#web page - copy

dta --- file -- folder/directry
 cd /var/www/html

 pwd
 gedit lw.html
 welcome to lww

 systemctl start httpd


http:\\192.168.0.1/lw.html


client need wewb client software  --- chrome


firewall --- security


systemctl stop firewalld 

:w -- save
:q --- quit
:wq -- save and quit

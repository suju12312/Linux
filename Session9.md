Networking
container --> docker kubernetes openshift
cloud 
Linux

TWO COMPUTER 

A --------------------------n.w-----> B
n/w --> connectvity  --> wifi / wired

physical medium

List down A ---> b and b--->a  possible a can connect to b but b dont to a

1. physical medium
2. os --> boot up
3. NIC (NETWORK INTERFACE CONTROLLER) / LAN/N CARD (netwrork acess)
4. IP address
5. Same n/w different n/w
6. source computer -> request -> a (routing table ) --> destination rnage
7. a ---> switch ---> b (route tble a dont know then switch caqn be come in place)
 a ----- router ---b 
8. NAT
how many available verson of ip address available?
---> 16 different ip adress in the market


same n/w ---> switch/hub/jack wire
different nw--> router

IPv4 
                          0-255
----- . ----- . ------ . -----

192.168.1.10

192.168.1 ---> n/w

192.168.1.10 ------>   switch ---->  192.168.1.12  same network

192.168.1.10 -----> router ------>      192.168.2.5 different network


A               switch              b
192.168.1.5                    192.168.2.10
depond on us if want connect or not by network name 
if consider 3 192.168.1 as then network name is different 
if consider two then 192.168 then it will connet by switcher

class A  126
class B 164 - CONSIDERED TWO OCTATE
class C 192  THREE OCATATE IS CONSIDERD AS NETWORK NAME
class D 239


WE CAN DECIDE WHAT WILL BE OUR NETWORK NAME  
suppose 2 will be considered (tell os)

netmask  255.255.255.0


simple if 255.255.255.0 then three octate will be considered


192.168.1.---  (-- = hOSTIP)

256  --> 2^8 = 1 BYTE
UPTO US WHICH NETWORK RANGE WE WANT


192.168.1.2
255.255.0.0
------------
192 .16.8.0.0 (NETWORK NAME)
-------------

TOTAL HOST WE ALLOCATE IS 65536 MEANS CAN CONNECT WITH OTHER WITH SWITCH 2^16

linux o.s
192.168.1.2
255.255.255.0

[root@localhost ~]# ifconfig enp0s3 192.123.1.4 netmask 255.255.255.0 --1
[root@localhost ~]# route -n  
[root@localhost ~]# ip route add 10.1.2.3/255.255.25.0 dev enp0s3  --2
[root@localhost ~]# ping 10.1.2.1
[root@localhost ~]# ping 11.1.2.3

10.1.2.3 netmask 255.255.255.0

router ---> 
vimal  98292912511 
   

Same sim Airtel (can connect to airtel and do all work)
rahul  9829125123

but have different sim then 
internally go to airtel and from there it will send to jio (measn airtel know were is jio company is known as routing) so device name is in between is router

192.168.1.5 /24   --- > router ------ >       11.1.2.3/24
255.255.255.0 or 24 (route length)
255.0.0.0 0r 8
255.255.0.0 0r 16

connect wore to one port of router and from router conec with b

what router do 
a send packet to router
router chrck were to go if b then send to b

if we dont know whjere to go ut then we cannot reach to router (gate means gateway)


cmd

ifconfig
ping 8.8.8.8 
whereis gatwa and shoud i have routing table from source?
route del -net 00..0.0 dev enp0s3
ping 8.8.8.8
route add -net 0.0.0.0 dev enp0s3
route -n
route add -net 0.0.0.0 gw 192.168.1.254 dev enp0s3

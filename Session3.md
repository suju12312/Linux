## session 3 notes

GUI ----> Behind scene some proggram is run which also known as cmd

screenshot --->  prt screen button 
gnome-screenshot

which gnome-scrrenshot
/usr/bin/gnome-screenshot

gnome-screenshot always stored by default in directory nameed as pictures
But if want to store in diffeent place make new directory 
ls
blue color --> directory
mkdir lworld
ls
document downloads lworld

gnome-screenshot 
cd lworld/
pwd  ---> /root/lwphoto (absolute path)
man gnome-screenshot
gnome-screenshot -f /root/lworld/s1.png
eog s1.png (open his file because needed double click to open image so eog cmd is there)
gnome-screenshot -h
gnome-screenshot -d=2  (delay in seconds) (hangup its unil 30 sec done )
firefox & (run command in backgground in running mode)

Task ---> fnd command behind ctrl +  c  and + z and resume process?
ctrl +s (invisible )
ctrl + q (showing what u have written in unhided )

program (file)
data ---> file ----> directory   99 percent of file create by software just we have to install it
rpm -q -a (list down all software in os)
rpm -q -l eog (-l --> long list)
software name is firefox and cmd name is forefox
tasmk: firefox cmd type karne mai google chalu hojaye
2nd: change icons 
3rd: software disconected but how can be installed that on other laptop




package management -----> rpm

rpm -q -i fireofox ( give information of all software )

rpm -e firefox
df (where dvid connected )
cd /run/media/root/HEL-9-2-0-BaseOS-x86_64
ls
cd AppStream/
ls
cd Packages/
ls
(lot opf packages available eg firefox)
touch vimal.txt
ls
ls vimal.tcxt
if locterd give file name if not give cannot acees message

so do 
ls firefox
ls firefox-102.9.0-3.el9_1.x8
rpm firefox-""
rpm -i -v -h firefox


to solve dependemncies problem
---> yum
configure yum at /etc/yum.repos.d
cd /etc/yum.repos.d
ls
redhatr.repo
gedit mydvd.repo
[DVD1]
/run/media/root..""/Appstream = baseurl = file://
[DVD2]
/run/...""/BaseOS
gpgcheck=0
yum install htppd
yum remove httpd
 task : how to install vlc player
 



folder (basic) 

Data to be storede permanent it sotred in hard disk (permaanent sotre known as persistent) 
Without directory we can create any file
if we want to create drectory then also one directory is needed so where to stop known as root
root --> /
agar hum kahi bhoi login kare tho vho ek directory masi hi ogeed hota hai

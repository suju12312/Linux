## Linux + docker


Developers ---- program --- programming language --- program write in file ----hard disk(storage)    
first load in ram device (ram/memory)
when program runs it is known as process



all process club together and become operating sdystem running

ps -aux (how many pprocess at time)
os start --- boot up  
1st process in rhel9 is systemd(big program)
 
pid 1
cpu 0.8
mem 0.2
vsz (virtual space)  
rss (real space)

firefox &(run in background)

if we know process d we can terminate the prograsm
kill 2694
pgrep firefix (2694)
man kill
kill -l
pgrep firefox
kill
kill -9 3184 
kill -19 3547 |(lock the firefox proces)
ps -aux | grep firefox
flag = sl RINNING STATE -9
flag = tl stopped state -19
kill -18 3547
3547 === directory /folder (program fro  thast lauch process means somewherein ram get space and store all data code files which create directory or folder)

cd /proc/ (contain all directory in ram)
ls
cd 3547
pwd op:/proc/4241
free -m
pwd
ls
programming language = memory overflow = oom_adj , oom_score, oom_scoreadj 
net working = net
stack memory = stack
schedulling = sched , schedstat,sessionid

vim status
root
process  -- for every,process create root intenally link with / drive
[root@localhost 4241]# ls pl
cd /
pwd op: /
cd -

## docker

program ----- process (folder in ram) --- inside called root linke diwth / drive ----(which is entire storage)--- 

process ---- root (folder) ----- different / (hard disk)---- which is image 

container is the process
start with bash shell


su - 
docker images ( give / as image)
docker run  -it centos:7
ps -aux | grep bash
docker run -dit --name os1 centos:7
docker ps
ps -aux | grep bash
cd /proc/1142896
pwd
cd root/
docker attach os1
docker attach os1
kill -9 114296
docker ps -a
docker ps
kill -l



container == os / process
process run from program (bash)
program --- runtime (container runtime) runc ---- container(for docker)

docker ----- run ---- containerd (container engine know how to run container)
ps -aux | grep docker
docker is a program which based oon daemon
podman == doemonles
docker is run on root most of the time not in user




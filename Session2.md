## sesssion 2


## Day 01

windows --- > oracle virtual box -----> rhel 9 o.s ---> 
Linux is centre of everything  ---> use of os is to run a program
Hb (user)  --------> program --------> o.s 
program is also known as command
To execute program we need operating system
             H.B (USER)
              |  |  |
              |  |  |   (INTERACTION)
                O.S
              |  |  |   (THREE METHOD)
             GUI CLI WEBURL

if we want power as unlimited then use root account (power means priviledge)
GUI ---> CLICK BY MOUSE ----->  Icon (inside program is runniing)
CLI ---> Terminal ---> command (prompting) --> type foefox (without using mouse) it will open his gui
GUI < CMD
SIGNAL PASS --> CLI (CTRL + C) TO Terminate UP THE COMMAND (Termination)
Stopped (Pause) ----> CLI (Ctrl+Z) tO PAUSE THE COMMAND 
ping www.google.com

Program ----> store in storage (hard disk)----> when execute ---> load in Ram (main memeory) -----> (PROCESS) -----> RUN PROCESS BY CPU 
- when we do ctrl + c process will removed 
- but when we do ctrl + z it did not remove in ram but pause there .
- to check ram ---> free / free -m (give output in megabytes (mb)).
- jobs ( to see paused program)
- fg

Terminal ----> CLI (Process) == Shell <-------cmd <------- user(H.b)
Shell ----> (1) Bash (2) Cshell (3) Shshell (4) Fish
Whenever we are using gui every gui run a program == cmd if we know that command we can run that program by cli also.
Program is crreated by developers
We ca see source code then use command which (name) eg which firefox
op: /usr/bin/firefiox

folder in linux is known as directory .
cmd: gedit /user/biin/firefox (find source code of firefox)
task: 5 commands of gui from rhel 9 (like firefox eg)
whoami ---> root
useradd tom (new acount is created)
passwd tom (set ur password)
Linux is Multi-user O.S (SCREEN (Virtual TERMINAL(vt) ) -----> LOGIN ----> MULTI-USER O.S)
shortcut : left ctrl +alt + f? 1 to 6 ( to open vt)
f2 --> give gui
f3 to f6 ---> give cli
tty ---> which terminal no it give
task : how can we increase the terminal vt in rehel9?
Gui --> 1 can use only at one (if one want to login or create with more user then how can be?)
cmd : chvt 4 (switching in terminal)
Any gui open thing commad if u write then it will not run in black terminal except in f2 because thats gui
Gui ---> gnome CLI ---> BASH SHELL
We can send mail , tweet and more stuff by cli (how ? task)
cmd: history (whatever u have wrie all will show with no
if we want to swtich t command thensee in histoey that no (!2) )
MANUAL (CMD : MAN ) EG: MAN DATE
date +%m
date +%M
date +%r
task : certain command in linux that figure the way find command thatr showing date timer in real time. (how to check running date or time in linux terminal)




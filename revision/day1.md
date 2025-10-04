###
With only a few notable exceptions, most popular Linux 
distributions are either Red Hat based (Red Hat Enterprise Linux, Fedora, CentOS, and so on) or Debian based (Ubuntu, Linux Mint, KNOPPIX, and so forth).

### Cockpit administration web UI: 
Since Linux was created, people have tried to develop  simple graphical or browser-based interfaces for managing Linux systems. I believe that Cockpit is the best web UI ever created for managing most basic Linux features. Throughout this book, I have replaced most older system-config* tool descriptions with those focusing on Cockpit. With Cockpit, you can now add users, manage storage, monitor activities, and do many other administrative tasks through a single interface.
### Lead into cloud technologies:
 After introducing cloud technologies in the previous edition, I’ve expanded on that coverage here. This coverage includes setting up your own Linux host for running virtual machines and running Linux in a cloud environment, such as Amazon Web Services. Linux is at the heart of most technological advances in cloud computing today. That means you need a solid understanding of Linux to work effectively in tomorrow’s data centers. I help you learn Linux basics in the front of this book. Then in the last few chapters, I demonstrate how you can try out Linux systems as hypervisors, cloud controllers, and virtual machines as well as manage virtual networks and networked storage.
### Ansible:
 Automating tasks for managing systems is becoming more and more essential in modern data centers. Using Ansible, you can create playbooks that define the state of a Linux system. This includes things like setting which packages are installed, which services are running, and how features are configured. A playbook can configure one system or a thousand systems, be combined to form a set of system services, and be run again to return a system to a defined state. In this edition, I introduce you to Ansible, help you create your first Ansible playbook, and show you how to run ad-hoc Ansible commands.
### Containers: 
Packaging and running applications in containers is becoming the preferred method for deploying, managing, and updating small, scalable software services and features. I describe how to pull containers to your system, run them, stop them, and even build your own container images using podman and docker commands.
### Kubernetes and OpenShift:
 While containers are nice on their own, to be able to deploy, manage, and upgrade containers in a large enterprise, you need an orchestration platform. The Kubernetes project provides that platform. For a commercial, supported Kubernetes platform, you can use a product such as OpenShift.


 ### 
 Is paragraph ka simple Hinglish meaning ye hai — aaj ke time par Linux ne operating system ke world mein jeet li hai.

Linux ek open-source system hai, matlab koi bhi iske code ko dekh, use aur improve kar sakta hai. Is culture of sharing aur innovation ke wajah se Linux bohot fast improve hota rehta hai, jabki Windows jaise proprietary systems itni speed se compete nahi kar paate.

Microsoft jiska purana CEO Steve Ballmer ne Linux ko “cancer” kaha tha, ab khud ke Azure cloud par Windows se zyada Linux use karta hai. Google apne search servers aur Android phones ke liye Linux use karta hai, aur Chrome OS bhi Linux par based hai. Facebook bhi apni website LAMP stack par banata hai — Linux, Apache, MySQL, aur PHP — sab open-source tools hain.

Facebook apna code bhi public karti hai, jisse duniya bhar ke developers usme improvements karte hain, bugs fix karte hain, aur tezi se growth hoti hai.

Stock exchanges jaise New York, Chicago, aur Tokyo Stock Exchange bhi Linux par run karte hain — kyunki ye fast, secure, aur reliable hai.

Simple shabdon mein — Linux ne world ka trust jeet liya hai kyunki ye free, secure, flexible, aur sabke contribution se continuously improve hota rehta hai.

aaj kal cloud computing
 ek bohot popular concept hai, lekin iske peeche ka real base Linux aur open-source technologies hi hain.

Cloud ka matlab hai internet par servers aur software use karna, bina apne physical computer ke. Aaj jitne bhi bade cloud systems bante hain — chahe private ho ya public — unka foundation Linux aur open-source tools par hi hota hai.

Cloud banane ke liye jo parts chahiye jaise hypervisors
, cloud controllers
, network storage
, virtual networking
, aur authentication
 — ye sab free aur open-source form mein available hain. Matlab koi bhi inhe use karke apna khud ka cloud system bana sakta hai.


 ### Understanding What Linux Is

Linux is a computer operating system. An operating system consists of the software that manages your computer and lets you run applications on it.

### Detecting and preparing hardware:
 When the Linux system boots up (when you turn on your computer), it looks at the components on your computer (CPU, hard drive, network cards, and so on) and loads the software (drivers and modules) needed to access those particular hardware devices.

### Managing processes: 
The operating system must keep track of multiple processes 
running at the same time and decide which have access to the CPU and when. The system also must offer ways of starting, stopping, and changing the status of processes.
### Managing memory: 
RAM and swap space (extended memory) must be allocated to applications as they need memory. The operating system decides how requests for memory are handled.
### Providing user interfaces:
An operating system must provide ways of accessing the 
system. The first Linux systems were accessed from a command-line interpreter called a shell. Today, graphical desktop interfaces are commonly available as well.
### Controlling filesystems: 
Filesystem structures are built into the operating system (or 
loaded as modules). The operating system controls ownership and access to the files and directories (folders) that the filesystems contain.
### Providing user access and authentication: 
Creating user accounts and allowing boundaries to be set between users is a basic feature of Linux. Separate user and group accounts enable users to control their own files and processes.
### Offering administrative utilities: 
In Linux, hundreds (perhaps thousands) of com mands and graphical windows are available to do such things as add users, manage disks, monitor the network, install software, and generally secure and manage your computer. Web UI tools, such as Cockpit, have lowered the bar for doing complex administrative tasks
### Starting up services:
 To use printers, handle log messages, and provide a variety of system and network services, processes called daemon processes run in the background, waiting for requests to come in. Many types of services run in Linux. Linux provides different ways of starting and stopping these services. In other words, while Linux includes web browsers to view web pages, it can also be the com puter that serves up web pages to others. Popular server features include web, mail, database, printer, file, DNS, and DHCP servers. 
 ### Programming tools:
  A wide variety of programming utilities for creating applications and libraries for implementing specialty interfaces are available with Linux.

s paragraph ka simple Hinglish meaning ye hai — Linux ko aise configure kiya ja sakta hai ki wo advanced computing tasks ko handle kar sake, jaise clustering, virtualization, cloud computing, real-time processing aur specialized storage.

Clustering﻿
 — Linux multiple computers ko ek single system ki tarah kaam karne ke liye combine kar sakta hai. Agar ek system fail bhi ho jaye, service doosre system se continue rehti hai bina interruption ke.

Virtualization﻿
 — Linux ek host system ki tarah kaam karke uske upar alag-alag operating systems (jaise Linux, Windows, BSD) chala sakta hai, jaise sab apne-apne separate computers ho. Iske liye KVM﻿
 aur Xen﻿ jaise tools use hote hain.

Cloud computing﻿
 — Large-scale virtualization manage karne ke liye Linux platforms use kiye jaate hain jaise OpenStack﻿, Red Hat Virtualization﻿
, aur oVirt﻿. Ye multiple servers, virtual machines, networks aur users ko ek saath manage karte hain. Kubernetes﻿ containerized applications ko bada-bada data centers mein handle karta hai.

Real-time computing﻿
 Linux ko real-time systems ke liye configure kiya ja sakta hai, jahan kuch processes ko high priority aur immediate response milta hai.

Specialized storage﻿
 — Data sirf hard disk par nahi, balki advanced storage systems jaise iSCSI﻿, Fibre Channel﻿, aur Infiniband﻿ par bhi store kiya ja sakta hai. Complete open-source storage solutions jaise Ceph﻿ aur GlusterFS﻿ bhi available hain.

### Understanding How Linux Differs from Other Operating Systems

Is paragraph ka simple Hinglish meaning ye hai — agar aap Linux ke naye user ho, to ho sakta hai ke aapne pehle Windows﻿ ya MacOS﻿
use kiya ho. Ye dono proprietary operating systems﻿ hain, matlab inka source code aap nahi dekh sakte, change nahi kar sakte, aur apna version nahi bana sakte.

Aap operating system ke original code nahi dekh paate, isliye agar kuch problem ho to usse apne hisaab se fix nahi kar sakte. Aap bugs ya security problems khud check nahi kar sakte.
Agar company chahe to aapko unke system ke programming interfaces ka access bhi nahi milta, isliye apna software aasan se connect karna mushkil ho jata hai. Kayi log soch sakte hain, “Mujhe kya farq padta hai? Main to developer nahi hoon.” Par open-source software (jaise Linux) ke wajah se hi aaj Internet﻿
, Google﻿
, Android phones﻿
, aur TiVo﻿
jaise devices sambhav hue hain. Free software ne computing cost kam ki aur innovation bada di.

Chahe aap khud Linux ka use ek multi-billion-dollar company banane ke liye na karna chahe, phir bhi duniya bhar me un companies ko skilled log chahiye jo Linux systems chala sakein.

Aur agar aap ye soch rahe ho ke itna powerful aur flexible system free kaise hai, to iska jawab Linux ke history me chhupa hai. Agle parts me bataya gaya hai kaise Free Software Movement﻿
ne Linux ka raasta banaya.
# Virtualization 

Virtualization is the process of separating the software from the hardware.


## What is a virtual server?

A virtual server means that a server does not exist in a physical form. The server itself is just a file. You can take it and run it on another hardware, and it should run and work without any problem. 

Before virtualization, a server used to be equipped with specific operating system. 

If you want another server, it used to be that you would have to buy the server, running an operating system and then running the software.

## Virtualisation 

In virtualization, you have the physical node and hypervisor (virtualization layer). The hypervisor is the interface between the hardware and operating system. Instead of having just one os coupled with the physical node, you have the hypervisor that provides the interface with the physical node, and then you run the os on the hypervisor directly. For example, if you have a network/graphic card, and you need to change it, nothing will be affected. This os has nothing to do with the physical node, it goes through the hypervisor. All will go through the hypervisor.

If you bought a new machine, you install the hypervisor. The os and the app in this case act like a file. e.g. like Kali Linus 

## Type 1 and Type 2 

We have several types of hypervisors. We have type 1 and type 2.

Type 1: you have the hardware and directly on the hardware, you have the hypervisor. You don't have an operating system between the hardware and the hypervisor. It eliminates all the middle layer between the hardware and the hypervisor. Then the hypervisor will run the virtual machines. You don't have a host os. You have the hardware, the hypervisor and the guest os directly.

In type 1, the hypervisor itself you can control everything. You have less components to secure than type 2 hypervisor. 



Type 2: You have the hardware, os (the os in this case is windows), and the hypervisor (in this case is virtualbox or a vmware). In this case, our os is the host os because it is hosting the hypervisor, and the other virtual machines. 

In type 2, you have the hypervisor working on the host os and the guest os. 

What's in common between the two types is that the operating systems don't share anything between eachother. 

Which is better?

Perfomance - Type 1 is better 

The more layers you add, the more security we need. 

## What are the benefits of virtualization?
- reduces the cost. In the past for example, if we wanted to run multiple servers, we needed separated servers. 
- downtime - if in the past there was a problem with a server, you would have to install and run a new server and that could take a long time. With virtualisation, if the server is down then you just start another server with a hypervisor, move the file and then you are up and running
- scalability - you need aanother server? it is easy. You just need the virtual machine file and hypervisor

 
How can we save money if we are using the same hardware?

We will be using virtualbox 

We will work with Linux

Learnt how to download Ubunto 

Learnt how to create a virtual machine from an iso image from linux

## What is Linux?

It is an operating system.

## What is the main attributes of Linux?
It is an open source. It started as a multiuser and multitasking operating system. 

From the design of Linux, it was built on these three things:

-open source
-multiuser
multitasking operating system

Its free available for download and use 

Linux is the leading os on servers. 

## What are the differences between Windows and Linux?

- Windows is user interface based and linux is command based
- In linux, you can go through the source code line by line and check what's going on. Security people can check everything. Microsoft and windows in not the case - it is closed source. When you test something with a closed source, you are testing it from the outside. You are not really testing or editing the code to know if there is a problem or not. In linux, you can go thorough the code, change it, compile it and have your own version of Linux. 

Linux has an architecture for its operating system which is fixed.

## The linux architecture consists of:
- The application
- Shell
- Kernel
- Hardware
  
#What is the Kernel?
The Kernel is the core interface between the hardware and the processors. 

## What is the shell?
Interface between the users and the applications and the kernal

In Linux, we have many shells:
- SH
- Bash 
- Dash (Debian Shell)
- TCSH 
- KSH 
- ZSH 

Many of these share certain commands but will also differ

## In Kali Linux, we use ZSH.
## In Ubunto, we use SH or bash 

It is possible to download and install another shell

ZSH and bash are very similar 

## What is the application here?
Whether the user is seeing a graphical interface or command line interface. It will be interpreted to commands at the end. Everything will go through the same pipeline, through the shell, then the kernel then the hardware

## Linux Distributions

Linux Distributions is a software collection that's built on Kernel. So any distribution you have, it will go back to the same Kernel. The software collection around the Kernel are different from distribution to another distribution (some distributions will focus on things that other distributions do not have). For example, Kali Linus has everything that focuses and is related to cyber security. You will find other distributions that might focus on for example, audio and video or desktop applications.

## The main 3 distributions of Linux:

- Debian Linux
- Fedora 
- Arc Linux 

Ubunto and Kali is a derivative from Debian. Most distributions are a derivative from Debian. 

Fedora has the main two derivatives  

Arc Linux - used for advanced users. Not covered in this course

Today, we will install Ubunto and Kali Linux for Cyber Security.

## File System:
The files in or from the storage devices (e.g hardisk, USB etc)
Linux supports an EXT 4 and EXT 3, BTRFS, XFS file system 
Ext 4 is the basic one - can support large volumes of data (designed for huge amounts of data)
The file system is what controls how to write on the storage medium 

The storage on your computer starts with root
Whether you have multiple hardisks or one drive - it will all be under one the root 

Linux runs under the concept that everything is a file. This means that it could be edited, read and write on the file. e.g process informatioon - if you want to check the memory on the computer, you can read it the information from this file.

It unifies all types of communications in this case.

We will be installing Ubunto next





slmgr /xpr 

checks whether windows version is genuine or not  - whether its the origional

netplwiz 
- gives you the user account and if u want to disable accounts - and forces the user to enter the passwords
  
- diagrams



 
## Recap on Kali Linux:

When we started using the virtualisation, we created a hypervisor (which acts as a hardware and the software runs on it) which essentially virtualises the hardware. But in reality, there is a virtual machine inside the real machine and the downside to this is that it is slow (as it trying to mimick the hardware- it behaves as a computer).

One of the biggest issues application developers are faced with is that variation between the development and production environment. In the past, the developers will write the code and then send the code to the production team to run the server but it doesn't run on the production teams computer. This happens because the development environment is different from the production environment (for example, there may be a variation in the version of the sofware). 

Therefore, a new adaptation of virtualisation was created where virtualisation was used to create the same environment that will run on both the devlopment and production team. So, when the code is written, it would be written in an environment similar to the enviroment that will be in production.

Vagrant was then proposed for a more automated solution,

## Vagrant 

Vagrant is a tool for building and managing the virtual machine environment in a single workflow. You would give this to every person which will then be run on their machine. Vagrant is not a virtual machine or a hypervisor. 

When the whole development team uses vagrant to create a code, you would give the same code/file to the production team. 

It needs a hypervisor running on the same machine in order to manage it

In this case, you would have a vagrant file that has the configurations related to the project and when you want to start working on the project, it will start the vagrant file and the vagrant file will create an environment as a virtual machine and it will link the folder to the folder in the virtual machine. The code is wrriten on the computer but the testing and all the running happens inside the virtual machine.

## Docker  

Docker is the idea of containers 

A container is a standard unit of software in which application code is packages along with its libraries and dependencies. 



When do we use container and when do we use VM?

You can use the container in development, development and testing.
For example, if you want to test a code and you don't want to install the libraries on your machine directly, you can start a container, test it and then destroy it. It doesn't change anything on your computer because everythign was installed in the container and then you destroyed it.

Also, for example, if you have a different servers like a web-server, a data base server and a log server. You will have 3 virtual machines running on your computer. That would make your computer very slow. In a container, they don't do that, they use as much as they need and you can put a cap on their resources. You can control everything. 

In Docker, you can run a container engine and use part of the os from there - it runs separately in each container but comes from the same operating system. You are basically running the librarieis that you specified through the container engine and you don't have the full operating system running.

A vm has the complete os inside the machine. Containers are hosted on a single physical server with a host which is shared among them. 

In VM, the guest os does not share anything with the host os but in containers, they share the os with the host. 


What are the benefits of containers?
- easy to run since we don't download the whole os
- quick since it shares the same os
- isolated from the other processors and we can control what part of the host os we can access
- you don't have conflict between the libraries 
  - different versions of python are not conflicted


Disadvantages of containers
- Usually containers are limited to the resources they can access in the os
- security incidents 2018 60% suffered a security breach related to containers 
- any misconfiguration/problem will allow the malware to escape from the container to the host os 


Docker is an open platform for developing, shipping and running containers. 

Using docker we can seperate the application from the infrastructure. It is written in a language called GO. It is free to use. 


## Cloud computing

is an on demand delivery of any computing service services (e.g. could be a server or a software ) over the internet.

It is any resource for example, servers, applications, infrastrucure  

benefits
- scalable  is much easier when you are renting because you are not paying for the server and most of these services are running on pay as you go. So, if you are using the service, you pay and if you are not then you don't pay. 
- cost- eliminates the capital expense of buying hardware and software and setting up and running on-site data centres
- reliability - there is data backup and disaster recovery so it makes it easier for business's not to lose their work
- Also for example, if you are running a service and its disrupted (you have users from different regions) - you can rent the servers in the same areas instead of having the servers in one area. So any problems in the connection or infrastructure between two countries or continents - they will not lose the connection because they are working in their region 

risks of cloud computing 
- you are not the only one who has access to the data or manages the data
- security - if there a misconfiguartion found by a hacker then might cause a data leak

  
cloud deployment types:
- public cloud is owned and operated by a third party e.g AWS, Microsoft Azure etc - you rent access to the resources
- private cloud is the resources used by a single business or organisation. Some organisations prefer to have their own cloud
- hybrid cloud whihc combines the public cloud and private cloud. You have some resources in public cloud and some on private cloud and you have some applications that work in between them.
- 

## Difference between cloud computing and virtualisation


we would not be able to have cloud computing in its current form without virtualisation as technology. Cloud computing is not a technology but is a way of delivering sharing and renting services

main three cloud providers and what are the services provided by each one of them:
- AWS Amazon Web Services - leader in public cloud computing and is a major player in AI, database, machine learning and serverless deployments. 
  
- Microsoft Azure - offers a hybrid cloud model
  it might be more convenient to choose this as your cloud service provider if you are already deploying windows and other microsoft software in your comapny because of its compatibility 
  
- Google Cloud
compatible with Android, OS X, windows and iOS which makes it useful on the desktop, tablet and even on the smartphone. Google cloud has made file sharing and working remotely with internet connection very easy.
  










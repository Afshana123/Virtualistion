# Potential Questions

## What is Vitualization?

Virtualization is the process of separating the software from the hardware.

Virtualisation does not exist in a physical form, allows you to create OS's/ storage devices that are traditionally bound to hardware.

There are two types of virtualization:

Type 1: you have the hardware and directly on the hardware, you have the hypervisor. You don't have an operating system between the hardware and the hypervisor. It eliminates all the middle layer between the hardware and the hypervisor. Then the hypervisor will run the virtual machines. You don't have a host os. You have the hardware, the hypervisor and the guest os directly.

In type 1, the hypervisor itself you can control everything. You have less components to secure than type 2 hypervisor. 



Type 2: You have the hardware, os (the os in this case is windows), and the hypervisor (in this case is virtualbox or a vmware). In this case, our os is the host os because it is hosting the hypervisor, and the other virtual machines. 

In type 2, you have the hypervisor working on the host os and the guest os. 

## What is Vagrant?

Vagrant is a tool for building and managing the virtual machine environment in a single workflow. You would give this to every person which will then be run on their machine. Vagrant is not a virtual machine or a hypervisor. 

When the whole development team uses vagrant to create a code, you would give the same code/file to the production team. 

It needs a hypervisor running on the same machine in order to manage it

In this case, you would have a vagrant file that has the configurations related to the project and when you want to start working on the project, it will start the vagrant file and the vagrant file will create an environment as a virtual machine and it will link the folder to the folder in the virtual machine. The code is written on the computer but the testing and all the running happens inside the virtual machine.

## Difference between VM and Vagrant 

A virtual machine is where you can run any operating system on your machine and freely switch between different operating system. So on Virtual Box you can run pretty much any OS and if you installed multiple os on virtualbox, you can switch between using the different os's. It's a virtual environment that functions like a virtual computer. 

Vagrant is a tool for building and distributing development environments. It's main objective is to simplify the software configuration management of virtualization to increase development productivity. 

For example: On Kali Linux, we installed the whole os and ran the whole operating system every time.


## Docker/What is a container?
Docker is the idea of containers 

A container is a standard unit of software in which application code is packages along with its libraries and dependencies.

Docker is an open platform for developing, shipping and running containers. 

Using docker we can separate the application from the infrastructure. It is written in a language called GO. It is free to use. 

## When do we use container and when do we use VM?

You can use the container in development, development and testing.
For example, if you want to test a code, and you don't want to install the libraries on your machine directly, you can start a container, test it and then destroy it. It doesn't change anything on your computer because everything was installed in the container, and then you destroyed it.

Also, for example, if you have a different servers like a web-server, a database server and a log server. You will have 3 virtual machines running on your computer. That would make your computer very slow. In a container, they don't do that, they use as much as they need, and you can put a cap on their resources. You can control everything. 

In Docker, you can run a container engine and use part of the os from there - it runs separately in each container but comes from the same operating system. You are basically running the libraries that you specified through the container engine, and you don't have the full operating system running.

A vm has the complete os inside the machine. Containers are hosted on a single physical server with a host which is shared among them. 

In VM, the guest os does not share anything with the host os but in containers, they share the os with the host. 

## When do you use vagrant or docker? 

If you want to manage machines, you should use Vagrant. And if you want to build and run applications environments, you should use Docker.

Vagrant is a tool for managing virtual machines. Docker is a tool for building and deploying applications by packaging them into lightweight containers. A container can hold pretty much any software component along with its dependencies (executables, libraries, configuration files, etc.), and execute it in a guaranteed and repeatable runtime environment. This makes it very easy to build your app once and deploy it anywhere - on your laptop for testing, then on different servers for live deployment, etc.

Vagrant was designed to manage virtual machines. Docker was designed to manage an application runtime. 

## What is cloud computing?

It is an on demand delivery of any computing service services (e.g. could be a server or a software ) over the internet which is called 'the cloud' in order to offer faster innovation, flexible resources and economies of scale. Typically, you only pay for cloud services you use, helping you lower your operating costs, run your infrastructure more efficiently and scale as your business needs change.

## What is the benefits of cloud compuuting?

- scalable  is much easier when you are renting because you are not paying for the server and most of these services are running on pay as you go. So, if you are using the service, you pay and if you are not then you don't pay. 
- cost- eliminates the capital expense of buying hardware and software and setting up and running on-site data centres
- reliability - there is data backup and disaster recovery so it makes it easier for business's not to lose their work
- Also for example, if you are running a service and its disrupted (you have users from different regions) - you can rent the servers in the same areas instead of having the servers in one area. So any problems in the connection or infrastructure between two countries or continents - they will not lose the connection because they are working in their region 

## Difference between cloud computing and virtualisation?

basically we would not be able to have cloud computing in its current form without virtualisation as technology. Cloud computing is not a technology but is a way of delivering sharing and renting services

virtualization is a technology that allows you to create multiple simulated environments or dedicated resources from a single, physical hardware system, and clouds are IT environments that abstract, pool, and share scalable resources across a network. 

Virtualization is a technology, where cloud is an environment.

## File System - Windows file system

A Windows file system is a system for storing and retrieving data from a storage medium. It basically organises the data on the storage medium. 

Storage medium e.g hardrive, SSD Card

The file system that will organise the data on the storage medium.

In windows, each os has its own standards:

- NTFS (New Technology file system)
    - the one we are using right now-
    - on this file system, you can have for example, different users. You can also implement privileges to make the system secure.
    - It is case-insensitive, so it does not recognise capital letters or small letters. However, it can be configured to be case-sensitive. 
    
- FAT (File Allocation Table) 12/16/32 - which had no security (UBS's are working on FAT 16/32)
- EXFAT(Extended File Allocation Table) - not very secure also

The number is addressing the storage medium e.g FAT 32 cannot address storage more than 32GB 
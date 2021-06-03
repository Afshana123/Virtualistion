## Windows 

To enforce a password policy on Windows:

Edit Group Policy > Computer Configuration > Windows Setting > Security Setting >Account Policies > Password policies

In settings, go to sign-in options
You can add Windows Hello PIN in order to secure your machine

You can also enable and disable remote desktop:
Type in remote desktop on start menu

Recommendation for windows:
Use multiple accounts

Usually you have a guest account on your windows which you can disable:
Go on start menu > control panel > user accounts > add or remove user accounts

The guest account has no security. 

Turn on the Windows firewall
Control Panel > System and Security > Windows Defender Firewall > Turn Windows Defender Firewall on or off > Turn on both and click notify me 

Encrypting your data:

Encrypt your data on all of your devices 
There is a tool for this in Windows Business Edition
This is called bitlocker ( using 128 bit encryption and 256)
On file explorer, right-click on the file you would like to encript, and then you enter a password. It will ask you if you would like to enable the recovery keys. You can print or save them on another device. Make sure you do not lose the password as you will not be able to recover any of your data. 

## Virtualization 

Virtualization is the process of separating the software from the hardware.

A virtual server means that a server does not exist in a physical form. The server itself is just a file. You can take it and run it on another hardware, and it should run and work without any problem. 

Before virtualization, a server used to be equipped with specific operating system. 

If you want another server, it used to be that you would have to buy the server, running an operating system and then running the software.

In virtualization, you have the physical node and hypervisor (virtualization liar). The hypervisor is the interface between the hardware and operating system. Instead of having just one os coupled with the physical node, you have the hypervisor that provides the interface with the physical node, and then you run the os on the hypervisor directly. For example, if you have a network/graphic card, and you need to change it, nothing will be affected. This os has nothing to do with the physical node, it goes through the hypervisor. All will go through the hypervisor.

If you bought a new machine, you install the hypervisor. The os and the app in this case act like a file. e.g. like Kali Linus 

We have several types of hypervisors. We have type 1 and type 2.

Type 1: you have the hardware and directly on the hardware, you have the hypervisor. You don't have an operating system between the hardware and the hypervisor. It eliminates all the middle layer between the hardware and the hypervisor. Then the hypervisor will run the virtual machines. You don't have a host os. You have the hardware, the hypervisor and the guest os directly.

Type 2: You have the hardware, os (the os in this case is windows), and the hypervisor (in this case is virtualbox or a vmware). In this case, our os is the host os because it is hosting the hypervisor, and the other virtual machines. 

Which is better?

Perfomance - Type 1 is better 

The more layers you add, the more security we need. 
24 mins






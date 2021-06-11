# Windows

Windows essentially started without security.

Windows API - when you have an app, you will need to communicate with the windows os. Windows provides what you call a windows API. For example, if you want to write on the harddrive, or communicate with the driver, or communicate with the hardware - it should go through the windows API. This way windows is protecting its Kernal from any non authorised access. 

If a virus or malware manages to work in the Kernal, then you no longer have control anymore.

In windows, we have two system architectures:

- 32 bits - Two power 32 - which means we can have a memory up to 4GB
- 64 bits - newer one - two power 64

the numbers are the number of bits used to address the memory

file explorer > this pc > properties > about 

os and CPU should be 32 or 64 

## Windows File System
A Windows file system is a system for storing and retrieving data from a storage medium. It basically organises the data on the storage medium. 

Storage medium e.g hardrive, SSD Card

The file system that will organise the data on the storage medium.

In windows, each os has its own standards:

- NTFS (New Technology file system)
    - the one we are using right now-
    - on this file system, you can have for example, different users. You can also implement privilidges to make the system secure.
    - It is case-insensitive so it does not recognise capital letters or small letters. However, it can be configured to be case sensitive. 
    
- FAT (File Allocation Table) 12/16/32 - which had no security (UBS's are working on FAT 16/32)
- EXFAT(Extended File Allocation Table) - not very secure also

The number is addressing the storage medium e.g FAT 32 cannot address storage more than 32GB 

## Users and Groups 
When doing security checks, check for users because a hacker can make an account and hack or use another user's password. You can do this by going on file explorer > Account > Users > Computer Management > local users and groups > users (exists by default) > groups (also exists by default) > double click on users in groups 

It is very important to check whether the user should be administrator or not. 

## What is a shared folder?
This is a folder that can be accessed through the network which means you share the folder on the computer and based on some settings and configuration, someone who is not on your computer can also access it. 

It is not the same thing as sharing a folder that is on the same computer. 

In this type of case, you should share the folder but set permissions for security

**To browse the shared folder on your machine:**

File Explorer > network > write: \\localhost (if you shared anything, you will find it here otherwise it will be empty)

Note: Whenever we refer to local host, this is referring to your computer. 

**To set up a shared folder:**

click on the folder you want to share > right click > go on 'give access to' > select and share with specific people 

you can stop the sharing by removing access in the same place

## Windows Registry 

A database for all the configurations of windows operating system 

If a malware/virus infiltrates in the boot in windows registry then it becomes infected 

**To open the registry:**

Search registry editor on start menu > export registry 

file > export > save registry file 

If something happens then at least you have a backup

## Remote Desktop 

You can also enable and disable remote desktop:
Type in remote desktop on start menu 

If enabled, anyone who has access to your username and password can connect to your computer directly from the internet

rdp - remote desktop protocol is the most dominant attack. 63% of ransomware attacks use rdp so it is very important to not have remote desktop enabled unless you are using it

Enforce a password policy on Windows:

Edit Group Policy > Computer Configuration > Windows Setting > Security Setting >Account Policies > Password policies

In settings, go to sign-in options
You can add Windows Hello PIN in order to secure your machine

- Keep your windows and applications updated all the time because most of the time, there are bugs in the software.
- Use a firewall in order to limit the access to the IP address
- Limit to working hours
- Use encryption
- If you don't need it, stop it 

## Loggings 

Logging is the process of collecting and storing data regarding the events that occurs on your computer or on the software. The main security is from logging 

So if you lose network, you will have a log to find out what is going on

start menu > type event viewer > you can check all the logs here 

## Recommendation for windows:
Use multiple accounts

Usually you have a guest account on your windows which you can disable:
Go on start menu > control panel > user accounts > add or remove user accounts

The guest account has no security. 

Turn on the Windows firewall
Control Panel > System and Security > Windows Defender Firewall > Turn Windows Defender Firewall on or off > Turn on both and click notify me 

## Encrypting your data:

Encrypt your data on all of your devices 
There is a tool for this in Windows Business Edition
This is called bitlocker ( using 128 bit encryption and 256)
On file explorer, right-click on the file you would like to encript, and then you enter a password. It will ask you if you would like to enable the recovery keys. You can print or save them on another device. Make sure you do not lose the password as you will not be able to recover any of your data. 

## Environment Variables


## Powershell 
This is windows version of command shell.

To open powershell:
search 'powershell' in windows 

Powershell can be launched as an admin or user mode 
- The user mode access is limited
- Admin gives access to all functionalities



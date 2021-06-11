# Kali Linux Commands 

Use Terminal Emulator or Ctrl+Alt+t to open the Kali Linux Shell

`pwd` – stands for 'print working directory' – it will print the directory you are in right now

**To create a new directory:**
`mkdir` - this means make directory 

`ls` – will show you all the directories and the files in the current path. However, you do not get any hidden files 

`ls -a` - shows all the hidden files and well as the command above.

The hidden files always start with a dot. So, if you would like to hide something, start it with a dot.

**Linux file systems are case sensitive**

Each folder in Linux has two subfolders at least. One which is '.' and the other being '..'

`ls .` - when you want to see the files in the current folder

`ls ..` - it will refer to the parent of the current directory 

`~` - refers to the home directory

`ls -l` - prints all the directories, and the files in a list. Each line is either a file or a directory

`ls -la` - prints all files including hidden files in a list

`type ls` - to find out the type of command it is. In this case, ls is an alias

`type type` - will show that type is a shell built in

Why is it important to know the origin of the command?
For example, if your computer was hacked, a command can harm your computer or come disguised as a command

`man ls` - `man` will provide help or a manual. It will give all the information regarding that command. E.g `man ls` will give you all the commands regarding `ls` command 

**Make a directory called testdir:**

`mkdir testdir`

**Browse the above directory:**

`ls testdir/` - if you do not start with a slash then the system will go and search in the current directory which is the same as `./testdir` as the dot at the beginning in this instance means current directory.

We have two paths in Linux: 

- Absolute Path
  - If you start the path with a slash then it is an absolute path. e.g `ls /home/kali/testdir` starts from the beginning of the hierarchy.
- Relative Path
    
**To create a file:**

e.g `touch testdir/testfile.txt` - touch will create the file without putting any content in it

`cat` - to create a content directly to the file e.g for the example above you would write `testdir/testfile.txt` to create a testfile.txt - it will read the content in the file 

`echo` - to add or append content inside the file e.g `echo Welcome to Kali > testdir/testfile.txt` - you need to add the > sign in order to redirect the message to the test file 

If you use echo with the only one > sign then it will just keep rewriting/replacing the content on the file 

If you want to append to a file, you can use two > signs e.g. `echo Welcome to Kali 1 >> testdir/testfile.txt` will add now this message, and the message above to the test file.

`cp` - used to copy one file to another e.g. `cp testdir/testfile.txt testdir/testfile1.txt`

However, you cannot use the above command to copy folders because when you copy directories, you should pass the `-r` option which means recursive. It should copy everything inside the directory recursively. e.g `cp testdir testdir2 -r`. 

`mv` - to move one file to another e.g `mv testdir2 testdir3`. 

`rm` - to remove a directory. However, you need to pass `-r` for directories like above as there are other items in that directory e.g `rm -r testdir3`

`cd` - changes to the current directory e.g `cd testdir`. You can do `pwd` to check where you are

`cd ..` - goes up to the parent directory 

`history` - will give you the history of all the commands that you have used so far. This is quite useful when you want to check again which commands worked and which didn't work.

`tree` - will print the current directory and all the subdirectories as a tree. This is an external command (it is not in the official distribution). It will show you how many directories and files there are too.

`date` - to check the date

`df` - to check what the free space in the file system is

`df -h` - will give you human-readable numbers 

`top` - will give the current processors running on your machine. Press Ctrl+c to stop it 

If you want to store your history:

`history >` and then redirect the history e.g `history > my_history.log`. If you do `cat my_history.log`, it will show what's inside the file. 

`ps` - gives you data about the processors

`free - will display the current situation of the memory

`cat /proc/meminfo` - read the memory information file (linux dealt with this as a file)

`cat /proc/cpuinfo` - reads the cpu info of the machine

## To edit files
We have `vi` and `nano` - vi is complicated (for professional use), nano is easy

`nano` - e.g `nano testdir/testfile` - it will open what's inside that file and you can edit it then press Ctrl+X and then Y to save.

## To run a script
To start a new file example:
 `nano testdir/script.sh` 
Inside the file write:
```commandline
NAME="Cyber-Course"

echo $NAME
```
Save file and exit out of the file. To run the script:
`. testdir/script.sh` - the dot makes it an executable script otherwise it will not run as the permission will be denied (it can't execute the command) OR you can write `zsh testdir/script.sh` 

## Extensions

Examples of extensions:
- .txt
- .sh 
- .log 

How does linux interpret these extensions?
We are only using extensions on Linux for two reasons:
- To make things clear for us
- The system itself can use the right application to open the file (linus will know what to open it with). 

## To change the permissions of a file:

`chmod 700` – user can read, ride and execute but the group does not have access e.g `chmod 700 testdir/scrips.sh` so now there won't be a permission denied. 

## User Management
Linux is a multi-user os which means that multiple users can log into the system either locally or remotely and perform a task at the same time.

It is possible to create multiple user accounts where each has its own set of permission privileges, files and directories.

The main account that exists in Linux is the root account. `pwd` gives you the root of the file system but to change to the root account ` sudo mkdir /root/test01`. Any command that starts with sudo will execute it as a root account. It will then ask you for the password. 


The root account can literally do anything. If someone has the root account on their Linux machine then that means the account can be used to do anything. There is no limitation and no protection against any type of commands. It has all the privileges and can execute anything. 

To get a list of users on your machine:
`cat /etc/passwd` - will display all the accounts on your linux machine 

To change the ownership of a file:
`chown` - `sudo chown kali /root/test01` - to change the owner from root to kali

## To add, update and remove packages from Linux

You need a root account for these:

To update the packages:
`sudo apt update` - `apt` is a package management used for Linux (advanced package tool) 

To upgrade the packages:
`sudo apt upgrade`

To install a package:
`sudo apt install` then the package that you want e.g `sudo apt install tree`

To remove a package:
`sudo apt remove` - e.g `sudo apt remove tree` then write `tree` to check to see if it exists(it should not exist if removed)

## Checking Logs

To check the log for everything:
`sudo cat /var/log/auth.log` - this will give you an authorisation log

`sudo more /var/log/auth.log` - reads the file page by page (you can hit enter to move onto the next page)

`sudo less /var/log/auth.log` - works in a similar way to `more`

`sudo tail /var/log/auth.log` - to read the end of the page


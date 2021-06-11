ec2  - 

instances in aws

images AMI's - Amazon machine image - the os that your going to run on ec2 

network and security - let aws create by default the security group but when you make your own, you can define and create the protocols a security group

created the instance and then created the ip address

everytime you start a new instance, you will not have a new ip address all the time - elastic 

network interface - 

when we start automating the process, we need to define the value of each variable in network interfaces 

auto scaling - when it hits for example 90%, it will start another server in order to balance the load between the two servers

aws s3 (symbol storage service) - storage service from amazon 

if you want to check an instance, make sure you terminate any instances after finishing the instance or if you don't need it anymore 

save ssh key in the folder in .ssh


```commandline
─(kali㉿kali)-[~]
└─$ ls .ssh
cyber-abegum-key.pem  known_hosts
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ ls -a .ssh
.  ..  cyber-abegum-key.pem  known_hosts
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ ls -l .ssh
total 8
-rw-r--r-- 1 kali kali 1674 Jun  4 11:14 cyber-abegum-key.pem
-rw-r--r-- 1 kali kali 1106 May  5 12:47 known_hosts
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ chmod 400 .shh/cyber-abegum-key.pem
chmod: cannot access '.shh/cyber-abegum-key.pem': No such file or directory
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ chmod 400 .ssh/cyber-abegum-key.pem                                                                                                                                                                                                  1 ⨯
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ ls -l .ssh
total 8
-r-------- 1 kali kali 1674 Jun  4 11:14 cyber-abegum-key.pem
-rw-r--r-- 1 kali kali 1106 May  5 12:47 known_hosts
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ ssh -i "cyber-abegum-key.pem" ec2-user@ec2-52-19-20-163.eu-west-1.compute.amazonaws.com        
Warning: Identity file cyber-abegum-key.pem not accessible: No such file or directory.
The authenticity of host 'ec2-52-19-20-163.eu-west-1.compute.amazonaws.com (52.19.20.163)' can't be established.
ECDSA key fingerprint is SHA256:bax8Qk8WHSPtX2A6lFu1k2rGk+aNyfWfC+a5eFYyQ1M.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'ec2-52-19-20-163.eu-west-1.compute.amazonaws.com,52.19.20.163' (ECDSA) to the list of known hosts.
ec2-user@ec2-52-19-20-163.eu-west-1.compute.amazonaws.com: Permission denied (publickey,gssapi-keyex,gssapi-with-mic).
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ ssh-add .ssh/cyber-abegum-key.pem                                                                                                                                                                                                  255 ⨯
Identity added: .ssh/cyber-abegum-key.pem (.ssh/cyber-abegum-key.pem)
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~]
└─$ ssh -i "cyber-abegum-key.pem" ec2-user@ec2-52-19-20-163.eu-west-1.compute.amazonaws.com
Warning: Identity file cyber-abegum-key.pem not accessible: No such file or directory.

       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/
6 package(s) needed for security, out of 17 available
Run "sudo yum update" to apply all updates.
[ec2-user@ip-172-31-41-195 ~]$ uname -a
Linux ip-172-31-41-195.eu-west-1.compute.internal 4.14.231-173.361.amzn2.x86_64 #1 SMP Mon Apr 26 20:57:08 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux
[ec2-user@ip-172-31-41-195 ~]$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.41.195  netmask 255.255.240.0  broadcast 172.31.47.255
        inet6 fe80::9e:c2ff:fe1a:b9bf  prefixlen 64  scopeid 0x20<link>
        ether 02:9e:c2:1a:b9:bf  txqueuelen 1000  (Ethernet)
        RX packets 42159  bytes 60789871 (57.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 19609  bytes 1138853 (1.0 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 8  bytes 648 (648.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 8  bytes 648 (648.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[ec2-user@ip-172-31-41-195 ~]$ exit 
logout
Connection to ec2-52-19-20-163.eu-west-1.compute.amazonaws.com closed.

```
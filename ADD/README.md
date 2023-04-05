### ADD

add is same as copy. it is usefull to copy files from local to container
but it has 2 extra capabilities.

1. Add can download the file from the internet to the container
2. Add can untar/Unzip the file directly into the container

--[ec2-user@ip-172-31-26-33 ADD]$ docker build -t add:v1 .
[ec2-user@ip-172-31-26-33 ADD]$ docker run -it add:v1
[root@eb2da48a0f80 /]# cd /tmp/
[root@eb2da48a0f80 tmp]# ls -l
-rw------- 1 root root 223011 Jan 1 1970 AirelRibeiro
[root@eb2da48a0f80 tmp]# exit

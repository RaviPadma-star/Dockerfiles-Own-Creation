###

Docker containers are ephemeral, when you remove containerby default it will delete the data

-----Docker Volumes------
cd /var/lib/docker/volume
##to set up docker volume
-- docker volume create <name of volume>

## how can we see a created volume

-- docker volume ls

## to insepect we it created

-- docker volume inspect nginx

[ec2-user@ip-172-31-26-33 ~]$ docker volume create nginx
nginx
[ec2-user@ip-172-31-26-33 ~]$ docker volume ls
DRIVER VOLUME NAME
local nginx
[ec2-user@ip-172-31-26-33 ~]$ docker volume inspect nginx
[
{
"CreatedAt": "2023-04-05T10:08:37Z",
"Driver": "local",
"Labels": {},
"Mountpoint": "/var/lib/docker/volumes/nginx/\_data",
"Name": "nginx",
"Options": {},
"Scope": "local"
}

### let say now we created volume, then how to attach this to container

-p hostport:containerport
-v hostpath:containerpath
-- docker run -d -v nginx:/usr/share/nginx/html -p 80:80 nginx

next go to root user --> sudo su
then go to -> cd /var/lib/docker/volumes/nginx/\_data

for all above we can use as we create a folder
-- mkdir testvolume
[ec2-user@ip-172-31-26-33 ~]$ docker run -d -v /home/ec2-user/test-volume:/usr/share/nginx/html -p 8083:80 nginx

sdsds

####

### FROM

from should be the first instruction of Dockerfile

- the file name should be Dockerfile

### How to build image from dockerfile

# syntax is # -t means is tagging, . is mandotory for syntax it denotes the current directory

```
docker build -t[docker-hub-URL]/[your-username]/[image-name]:version .
```

### Go to ec2 server then install git , clone repo

    # sudo yum install git
    # git clone https://github.com/RaviPadma-star/Dockerfiles-Own-Creation.git

    #Result in server

```
[ec2-user@ip-172-31-26-33 ~]$ ls

Dockerfiles-Own-Creation
[ec2-user@ip-172-31-26-33 ~]$ cd Dockerfiles-Own-Creation
[ec2-user@ip-172-31-26-33 Dockerfiles-Own-Creation]$ ls
FROM README.md
[ec2-user@ip-172-31-26-33 Dockerfiles-Own-Creation]$ cd FROM
[ec2-user@ip-172-31-26-33 FROM]$ ls -l
total 8
-rw-rw-r-- 1 ec2-user ec2-user 14 Mar 11 13:23 Dockerfile
-rw-rw-r-- 1 ec2-user ec2-user 99 Mar 11 13:23 README.MD
[ec2-user@ip-172-31-26-33 FROM]$ docker build -t docker.io/padmaravi/from:v1 .
Sending build context to Docker daemon 3.072kB
Step 1/1 : FROM almalinux
---> d3ffa43c2567
Successfully built d3ffa43c2567
Successfully tagged padmaravi/from:v1

```

### how to push a image to Docker hub

```
docker push -t[docker-hub-URL]/[your-username]/[image-name]:version

# Results in server

[ec2-user@ip-172-31-26-33 FROM]$ docker push padmaravi/from:v1
The push refers to repository [docker.io/padmaravi/from]
624a98f02f85: Preparing
denied: requested access to the resource is denied
[ec2-user@ip-172-31-26-33 FROM]$

**it access is denied because we need to login in server first cmd
        -- docker login

        # Results:
        Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: padmaravi
Password:
WARNING! Your password will be stored unencrypted in /home/ec2-user/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[ec2-user@ip-172-31-26-33 FROM]$ docker push padmaravi/from:v1
The push refers to repository [docker.io/padmaravi/from]
624a98f02f85: Mounted from library/almalinux
v1: digest: sha256:77e77cff9b2483dacc07feed7f5a23fb63445064769735314b1537f232dfe2ce size: 529
[ec2-user@ip-172-31-26-33 FROM]$



```

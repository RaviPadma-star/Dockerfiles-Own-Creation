### Run vs CMD \* important question in interview.

Run -
Run command will run at the time of image creation

CMD - >
command will ececute at the time of running container.
[ec2-user@ip-172-31-26-33 CMD]$ docker run -d padmaravi/myproject1
[ec2-user@ip-172-31-26-33 CMD]$ docker ps -a -q --> it give all running containers

    --to delete all container at a time use-- docker rm -f `docker ps -a -q`

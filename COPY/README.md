###

Copy instruction is usefull to copy the files from local to Image container
-- if i dont want a index page of webiste of ngnix
to remove that we can go to inside od=f container with
docker exec -it <imageid> bash
-- then go to cd usr/share/nginx/html

then go to cmd terminal -> git pull
[ec2-user@ip-172-31-26-33 COPY]$ docker build -t copy:copyrepo .

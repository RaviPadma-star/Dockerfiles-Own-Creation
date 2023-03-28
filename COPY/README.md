###

Copy instruction is usefull to copy the files from local to Image container
-- if i dont want a index page of webiste of ngnix
to remove that we can go to inside od=f container with
docker exec -it <imageid> bash
-- then go to cd usr/share/nginx/html

then go to cmd terminal -> git pull
[ec2-user@ip-172-31-26-33 COPY]$ docker build -t copy:copyrepo .

if we run docker run -d -p 8082:80 reponame;
then if we see the --docker ps -a
it shows the status will be exited so for that reason we need to give atleast one CMD for CMD ["nginx", "-g", "daemon off;"] so it will run
e2d3ff6a420f copy:copyrepo "nginx -g 'daemon of…" 5 seconds ago Up 4 seconds 0.0.0.0:8082->80/tcp, :::8082->80/tcp zen_satoshi

-- then we need to push the docker push copy:copyrepo
we will get access denied, becaus e we are not giving any user name for that
REPOSITORY TAG IMAGE ID CREATED SIZE
copy copyrepo f401cc21e68e 7 minutes ago 303MB

---> docker tag <repo:tagname> [usrname]/[repo:tagname] --->then enter

---> docker images
so it will create as
padmaravi/copy copyrepo f401cc21e68e 7 minutes ago 303MB

after pushing we need to run this instance where we want in any local

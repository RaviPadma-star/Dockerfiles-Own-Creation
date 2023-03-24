### LABEL

label instruction is used to give some metadata information
label we can consider as key value pair

-- for label omwards we are using local -> [ec2-user@ip-172-31-26-33 LABEL]$ docker build -t local .

-- next-> docker images
local latest 124a9f4b9662 2 minutes ago 190MB
-- docker inspect 124a9f4b9662
-- why we are using label means its filter out the servers if we have lot of many in server
-- docker images --filter "label=AUTHOR=Ravi"
[ec2-user@ip-172-31-26-33 LABEL]$ docker images --filter "label=AUTHOR=Ravi"
REPOSITORY TAG IMAGE ID CREATED SIZE
local latest 124a9f4b9662 6 minutes ago 190MB

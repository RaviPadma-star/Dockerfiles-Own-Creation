# Arg is used to supply the varaible while creation of image

- arg is the only instruction is used to use before FROM. arg declared before cant be accessed after FROM.

[ec2-user@ip-172-31-26-33 ARG]$ docker build -t arg:v1 .
invalid reference format
[ec2-user@ip-172-31-26-33 ARG]$ docker build -t arg:v1 --build-arg VERSION=8 .
[ec2-user@ip-172-31-26-33 ARG]$ docker build -t arg:v1 --build-arg VERSION=9 .

### using ENV and ARG for best results

## create one variable and assign the value to arg

then we acces or values both in images and container

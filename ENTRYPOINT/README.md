### Entrypoint is used to run the container just like CMD, but there are few difference

1. we cant overide the entrypoint, but we can overide in CMD
2. we cant override the entrypoint, if we to do so it append to the entry point
3. CMD will give the argument to entry point if we not mention in epression
   [ec2-user@ip-172-31-26-33 ENTRYPOINT]$ docker run entrypoint:v1
   PING google.com (142.251.16.101) 56(84) bytes of data.
   64 bytes from bl-in-f101.1e100.net (142.251.16.101): icmp_seq=1 ttl=49 time=1.46 ms
   [ec2-user@ip-172-31-26-33 ENTRYPOINT]$ docker run entrypoint:v1 ping -c3 facebook.com
   64 bytes from edge-star-mini-shv-01-iad3.facebook.com (31.13.66.35): icmp_seq=1 ttl=45 time=0.628 ms
   [ec2-user@ip-172-31-26-33 ENTRYPOINT]$ docker ps -a
   CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES
   3822f2053568 entrypoint:v1 "ping -c3 facebook.c…" 11 seconds ago Exited (0) 8 seconds ago thirsty_leavitt
   17e55b26f8bf entrypoint:v1 "ping -c5 google.com" About a minute ago Exited (0) About a minute ago loving_elion

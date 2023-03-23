FROM almalinux
RUN yum install nginx -y
CMD ["nginx", "-g", "daemon off;"]

#CMD ["sleep", "20"] there should be only one CMD instrucution for one docker file, if we give multiple it takes the last as reference 
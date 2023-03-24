FROM centos:8
RUN yum install ngnix -y
RUN rm -rf cd usr/share/nginx/html/index.html
COPY website /usr/share/nginx/html/
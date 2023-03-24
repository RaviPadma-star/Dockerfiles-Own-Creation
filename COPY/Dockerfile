FROM almalinux
RUN yum install nginx -y
RUN rm -rf cd usr/share/nginx/html/index.html
COPY website /usr/share/nginx/html/
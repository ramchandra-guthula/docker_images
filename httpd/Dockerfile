FROM centos:latest
MAINTAINER ramchandra
LABEL httpd_varsion=2.xx
ARG package=httpd
ARG file_name=index.html
RUN yum -y install $package
COPY $file_name /var/www/html/index.html
EXPOSE 80
CMD ["/usr/sbin/httpd","-D","FOREGROUND"]

FROM centos:latest

RUN yum update -y

RUN yum install wget unzip -y

WORKDIR /home/

ARG tomcat_version=8.5.66
ARG deployment_file=hello-1.0.war

#installing Java8

RUN wget -c --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.tar.gz && \
                 tar -zxvf jdk-8u131-linux-x64.tar.gz && \
                 rm -rf jdk-8u131-linux-x64.tar.gz



#setting JAVA env varibales
ENV JAVA_HOME=/home/jdk1.8.0_131
ENV PATH=$JAVA_HOME/bin:$PATH


RUN wget https://mirrors.estointernet.in/apache/tomcat/tomcat-8/v$tomcat_version/bin/apache-tomcat-$tomcat_version.tar.gz &&\
                                        tar -zxvf apache-tomcat-$tomcat_version.tar.gz && \
                                        rm -rf apache-tomcat-$tomcat_version.tar.gz


#ADD apache-tomcat-8.5.57.tar.gz /home/

#Adding deployment war file
COPY $deployment_file /home/apache-tomcat-$tomcat_version/webapps


RUN chmod +x /home/apache-tomcat-$tomcat_version/bin/catalina.sh

EXPOSE 8080

ENTRYPOINT ["/home/apache-tomcat-8.5.66/bin/catalina.sh", "run"]

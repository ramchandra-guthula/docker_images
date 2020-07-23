## Tomcat docker image

Please place apache-tomcat-8.5.57.tar.gz file and hello-1.0.war file before build the image

** build image with below command**
```
docker build -t <imagename> .
```
**Create container with below command**

```
docker run -itd -p 8080:8080 <image name> & 
```

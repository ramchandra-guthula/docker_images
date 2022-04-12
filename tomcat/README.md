## Tomcat docker image
Sample tomcat image to get practice on working tomcat image and understand how to create tomcat image using docker file

here we are downloading tomcat from the tomcat official website, url get's changed most of the times needs to update to the right once in case image build fails 

**build image with below command**
```
docker build -t <image name> .
```
**Create container with below command**

```
docker run -itd -p 8080:8080 <image name> 
```

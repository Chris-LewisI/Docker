# Docker
Practice and mini projects using Docker.

## To build docker container:
```
  $ docker build -t hello-world .  
```
-t --> names the container  
. --> points to current directory  

## To run docker containers:
```
  $ docker run -p -v /Users/../Docker/Hello-World/src/:/var/www/html/ 80:80 hello-world  
```
-v mounts a local directory to the container so that you can update your local files and see change in the container  
-p 80:80 --> forwards request from the local port 80 to the container's port 80  
EXPOSE 80 parameter in Dockerfile allows the image to handle it with Apache  
project runs on "localhost"  

###### Tips:  
Try to have one process per container because the duration of the container's run is dependant on the completion of the process.  

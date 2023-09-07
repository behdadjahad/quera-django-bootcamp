# lecture 3 (12:30 - 14:00)

## network


+ portainer
+ kitematic

## docker file 


we use `.dockignore` to specify the files that we don't want to have them in docker image.



these are the most used keywords in docker file.

``` Dockerfile
from # this command sets the base image

run # execute any commands in new layer on top of 

cmd # provide defaults for an executing container


expose # informs docker that the container listens on

add # copies new files or dir to containers

copy # copies new files to directories

entrypoint # configures a container that will 

volume #

user # 

workdir #

arg #

onbuild

stopsignal

label

healthCheck

shell

```

now lest use it in a real dockerfile
``` Dockerfile
FROM ubuntu:22.04

RUN apt update -y
RUN apt install -y nginx
RUN apt install -y vim net-tools iputils-ping

```
now lets build docker image

there is a problem the container will dies so fast

``` console 
$ docker build -t nginx:sm1
$ docker run -d --name w1 -p 80:80 nginx:sm
$ docker ps -a
```

lets make it better 

``` Dockerfile
FROM ubuntu:22.04

RUN apt update -y
RUN apt install -y nginx
RUN apt install -y vim net-tools iputils-ping

CMD ["nginx", "-g", "daemon off;"]

```
# docker-quickstart
This a quickstart for how to make a simple php apache environment of docker image

## - Download docker
[Docker Download](https://www.docker.com/get-started)  
Install docker and then run it
## Create basic files
```
mkdir docker
cd docker

mkdir src
cd src

#create hello world php file
echo "<?php echo 'hello, world!';" > index.php

#create Dockerfile
cd ..
vim Dockerfile
```
- In vim terminal:
```
FROM php:7.2-apache
COPY src/ /var/www/html
EXPOSE 80
```
- Then ESC and :wq  
## Run Docker image
- RUN cmd in current docker directory
```
docker build -t hello-world-php .
docker run -p 80:80 hello-world-php
```
- Then we can access localhost and see "hello,world!"

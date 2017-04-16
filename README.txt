# image downloads 
docker pull [OPTIONS] NAME[:TAG|@DIGEST]
ex] docker pull ubuntu

# look up all containers
docker ps -a


# look up images 
ex] docker images

# delete docker image

ex] docker images # get image ID
ex] docker rmi ${TENSORFLOW_IMAGE_ID}

docker rmi [OPTIONS] IMAGE [IMAGE...]


# make container docker [OPTIONS]  -i interactive   -t tty   -d detach  -name  naming
docker run -i -t --name hello ubuntu /bin/bash

# run container
docker restart name(namming or containerID)


# look up docker container logs
ex] docker logs [OPTIONS] CONTAINER     -f, --tail


# Attach Docker container 
ex] docker attach [CONTAINER]

# Stop Container
docker stop [OPTIONS] CONTAINER [CONTAINER...]

# docker ps # get container ID
# docker stop ${TENSORFLOW_CONTAINER_ID}
# docker ps -a # show all containers


# Build Dockerfile
mkdir example
cd example

docker build --tag hello:0.1 .

# Run Our Nginx Image
			   [MAKE CONTAINER NAME]  	   [Image NAME & Tag]
docker run --name hello-nginx -d -p 80:80  hello:0.1


#!/bin/bash
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)

# Hot Tip
# 도커를 컨테이너를 끄지 않고 , 나가는 방법?!
Ctrl + P  , Ctrl + Q 를 차례대로 누르고 나가면? 컨테이너가 종료되지 않는다!

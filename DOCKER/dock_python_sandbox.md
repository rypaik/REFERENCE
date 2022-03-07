Python Sandbox

```python
# Python Sandbox
```

Shell Sandbox

```shell
######### DOCKER PREP
# 1. Create Directory BASH
mkdir 
# 2. Make a docker file BASH
touch Dockerfile


######### DOCKER BUILD
## BUILDING DOCKER IMAGES CLI
# https://docs.docker.com/engine/reference/commandline/build/
docker build --name <name of image> .
docker build --name <name> -p <ports> -rm

docker build -t <imagetag> .

# builidng with DOCKERFILE
docker build -t python_docker_base -f Dockerfile . --no-cache



######### DOCKER START/STOP
## RUNNING DOCKER IMAGES
# https://blog.codeship.com/the-basics-of-the-docker-run-command/
docker run --name <name> <images> 
# Run a web App
docker run --rm prakhar1989/static-site
# https://blog.codeship.com/the-basics-of-the-docker-run-command/
docker run -ti -name <name> <images> 
docker run -ti -name <name> <image>   ** preferred

# STOP
docker stop <image>

```shell
# build docker file and all dependencies
# from inside location of docker file


docker run -p <port:port Map> <imageid>
docker run -it <imageid> sh # runs shell command at runtime


docker exec -it <imageid> sh  #runs shell command from inside that image
```

######### DOCKERHUB

# pulling image from Docker Hub

docker pull [OPTIONS] NAME[:TAG|@DIGEST]
docker pull

######### DOCKER IMAGE/CONTAINER MANAGEMENT

## LIST

# lists images

docker images

# list running containers

docker ps -a
docker ps --format $FORMAT

## REMOVE

# remove and image

docker rmi <image>

# deletes a container

docker rm <container>

# deletes all containers

docker rm $(docker ps -a -q -f status=exited)

######### DOCKER COMMANDS

# running bash inside Container

docker exec -it CONTAINER_ID bash
docker exec -it CONTAINER_ID sh

# commiting changes made in running container to image  - USE OG IMAGE and update to that IMAGE

# https://www.techrepublic.com/article/how-to-commit-changes-to-a-docker-image/

docker commit CONTAINER_ID IMAGE_NAME

# Save one or more images to a tar archive (streamed to STDOUT by default)

https://docs.docker.com/engine/reference/commandline/image_save/
docker image save [OPTIONS] IMAGE [IMAGE...]
docker commit -c 'CMD["redis-server"]' <id of image>

######### DOCKER COMMANDS

# images are the core library

# containers are the running instances of images

# commiting changes made in running container to image  - USE OG IMAGE and update to that IMAGE

docker commit CONTAINER_ID IMAGE_NAME

# running bash inside Container

# https://docs.docker.com/engine/reference/commandline/container_exec/

docker exec -it CONTAINER_ID bash
docker exec -it CONTAINER_ID sh

#saving Changes to a new image

# https://docs.docker.com/engine/reference/commandline/commit/

# https://www.techrepublic.com/article/how-to-commit-changes-to-a-docker-image/

docker commit

docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]

docker commit 
docker commit c3f279d17e0a  svendowideit/testimage:version3
docker commit <container> <image_repository>

# DOCKER CONTAINER EXPORT

https://docs.docker.com/engine/reference/commandline/container_export/

# DOCKER IMAGES EXPORT

https://docs.docker.com/engine/reference/commandline/export/

# DOCKER CP TO CONTAINER

https://docs.docker.com/engine/reference/commandline/cp/
docker cp '<filepath>' container:<target directory>

# getting docker container ip

https://stackoverflow.com/questions/17157721/how-to-get-a-docker-containers-ip-address-from-the-host

docker inspect <container ID>
docker inspect <container id> | grep "IPAddress"

[How to SSH into a Running Docker Container and Run Commands](https://phoenixnap.com/kb/how-to-ssh-into-docker-container)

sudo docker inspect -f "{{ .NetworSettings.IPAddress }}" container_name

# RUNNING LOCAL SCRIPT IN CONTAINER

https://stackoverflow.com/questions/34182530/how-do-i-run-a-python-script-with-tensorflow-running-in-a-docker-on-windows
docker run -v /path/to/your/script:/path/to/script

####### DOCKER LINKS
#cheatsheet
https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes

```
Docker Workflow

```shell
# build docker file and all dependencies
# from inside location of docker file

docker build -t <imagetag> .

docker run -p <port:port Map> <imageid>
docker run -it <imageid> sh # runs shell command at runtime


docker exec -it <imageid> sh  #runs shell command from inside that image
```

Modules

https://towardsdatascience.com/learn-python-modules-and-packages-in-5-minutes-bbdfbf16484e

https://betterprogramming.pub/write-better-python-scripts-ce58c1ebf690

https://medium.com/free-code-camp/awesome-python-modules-you-probably-arent-using-but-should-be-ec926da27439

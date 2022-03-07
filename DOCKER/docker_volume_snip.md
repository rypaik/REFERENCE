# Docker Volumes and Bind Mounts



## Code
--mount type=bind
```
docker run -d \
  -it \
  --name devtest \
  --mount type=bind,source="$(pwd)"/target,target=/app \
  nginx:latest

```


## Links
[Docker Bind Mounts Documentation](https://docs.docker.com/storage/bind-mounts/)
[Introduction to Docker Bind Mounts and Volumes](https://4sysops.com/archives/introduction-to-docker-bind-mounts-and-volumes/)
[docker bind mounts vs volumes](https://serverfault.com/questions/996785/docker-volumes-vs-mount-binds-what-are-the-use-cases)
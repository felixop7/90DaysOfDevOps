# Day 18: Docker for DevOps Engineers 🎉

## Daily Log

**Date:** July 5, 2024

Today marks the completion of our intensive Docker hands-on series! We have covered a wide range of Docker concepts, commands, and best practices, and I hope you have found these lessons as valuable and exciting as I have. Now, it’s time to consolidate everything we’ve learned into a comprehensive Docker cheat-sheet.

## Key Concepts

### Docker Cheat-Sheet

This cheat-sheet includes commands for both Docker and Docker-Compose, along with brief explanations of their usage. It serves as a handy reference guide for future projects and a contribution to the DevOps community.

### Docker Commands

#### Run a New Container

- Start a new container from an image:
  ```bash
  docker run IMAGE
  docker run nginx
  ```
- Assign it a name:
  ```bash
  docker run --name CONTAINER IMAGE
  docker run --name web nginx
  ```
- Map a port:
  ```bash
  docker run -p HOSTPORT:CONTAINERPORT IMAGE
  docker run -p 8080:80 nginx
  ```
- Map all ports:
  ```bash
  docker run -P IMAGE
  docker run -P nginx
  ```
- Start container in background:
  ```bash
  docker run -d IMAGE
  docker run -d nginx
  ```
- Assign it a hostname:
  ```bash
  docker run --hostname HOSTNAME IMAGE
  docker run --hostname srv nginx
  ```
- Add a DNS entry:
  ```bash
  docker run --add-host HOSTNAME:IP IMAGE
  ```
- Map a local directory into the container:
  ```bash
  docker run -v HOSTDIR:TARGETDIR IMAGE
  docker run -v ~/usr/share/nginx/html nginx
  ```
- Change the entrypoint:
  ```bash
  docker run -it --entrypoint EXECUTABLE IMAGE
  docker run -it --entrypoint bash nginx
  ```

#### Manage Containers

- Show a list of running containers:
  ```bash
  docker ps
  ```
- Show all containers:
  ```bash
  docker ps -a
  ```
- Delete a container:
  ```bash
  docker rm CONTAINER
  docker rm web
  ```
- Delete a running container:
  ```bash
  docker rm -f CONTAINER
  docker rm -f web
  ```
- Delete stopped containers:
  ```bash
  docker container prune
  ```
- Stop a running container:
  ```bash
  docker stop CONTAINER
  docker stop web
  ```
- Start a stopped container:
  ```bash
  docker start CONTAINER
  docker start web
  ```
- Copy a file from a container to the host:
  ```bash
  docker cp CONTAINER:SOURCE TARGET
  docker cp web:/index.html index.html
  ```
- Copy a file from the host to a container:
  ```bash
  docker cp TARGET CONTAINER:SOURCE
  docker cp index.html web:/index.html
  ```
- Start a shell inside a running container:
  ```bash
  docker exec -it CONTAINER EXECUTABLE
  docker exec -it web bash
  ```
- Rename a container:
  ```bash
  docker rename OLD_NAME NEW_NAME
  docker rename 096 web
  ```
- Create an image out of a container:
  ```bash
  docker commit CONTAINER
  docker commit web
  ```

#### Manage Images

- Download an image:
  ```bash
  docker pull IMAGE[:TAG]
  docker pull nginx
  ```
- Upload an image to a repository:
  ```bash
  docker push IMAGE
  docker push myimage:1.0
  ```
- Delete an image:
  ```bash
  docker rmi IMAGE
  ```
- Show a list of all images:
  ```bash
  docker images
  ```
- Delete dangling images:
  ```bash
  docker image prune
  ```
- Delete all unused images:
  ```bash
  docker image prune -a
  ```
- Build an image from a Dockerfile:
  ```bash
  docker build DIRECTORY
  docker build .
  ```
- Tag an image:
  ```bash
  docker tag IMAGE NEWIMAGE
  docker tag ubuntu ubuntu:18.04
  ```
- Build and tag an image from a Dockerfile:
  ```bash
  docker build -t IMAGE .
  docker build -t myimage .
  ```
- Save an image to a tar file:
  ```bash
  docker save IMAGE > FILE
  docker save nginx > nginx.tar
  ```
- Load an image from a tar file:
  ```bash
  docker load -i TARFILE
  docker load -i nginx.tar
  ```

#### Info & Stats

- Show the logs of a container:
  ```bash
  docker logs CONTAINER
  docker logs web
  ```
- Show stats of running containers:
  ```bash
  docker stats
  ```
- Show processes of a container:
  ```bash
  docker top CONTAINER
  docker top web
  ```
- Show installed docker version:
  ```bash
  docker version
  ```
- Get detailed info about an object:
  ```bash
  docker inspect NAME
  docker inspect nginx
  ```
- Show all modified files in container:
  ```bash
  docker diff CONTAINER
  docker diff web
  ```
- Show mapped ports of a container:
  ```bash
  docker port CONTAINER
  docker port web
  ```

## Reflection

Completing this Docker series has been an enriching experience. The hands-on tasks have solidified my understanding of Docker and Docker-Compose, preparing me to utilize these tools effectively in real-world projects. I am excited to apply these skills in upcoming projects and continue learning new commands and best practices from various resources.

## References

- [Docker Official Documentation](https://docs.docker.com/)
- [Docker-Compose Documentation](https://docs.docker.com/compose/)
- [Docker Cheat Sheet](https://cdn.hashnode.com/res/hashnode/image/upload/v1670863735841/r6xdXpsap.png?auto=compress,format&format=webp)

---

**Happy Learning! 🚀**

Roshan Sahani

# Day 14: Docker for DevOps Engineers 🐳

## Daily Log

**Date:** July 2, 2024

Today's focus was on getting hands-on experience with Docker, an essential tool for DevOps engineers. Docker allows you to package applications into containers, making it easier to build, test, and deploy applications across different environments.

## Key Concepts

### Docker

Docker is a software platform that packages applications and their dependencies into standardized units called containers. Containers include everything the software needs to run, ensuring consistency across different environments.

## Tasks

### 1. Use the `docker run` command to start a new container and interact with it through the command line.

#### Example:

```bash
docker run hello-world
```

This command runs a simple "Hello World" container to verify that Docker is installed and running correctly.

### 2. Use the `docker inspect` command to view detailed information about a container or image.

#### Example:

```bash
docker inspect hello-world
```

This command provides detailed information about the "hello-world" image, including its configuration and metadata.

### 3. Use the `docker port` command to list the port mappings for a container.

#### Example:

```bash
docker port <container_id>
```

Replace `<container_id>` with the actual container ID to view the port mappings for that container.

### 4. Use the `docker stats` command to view resource usage statistics for one or more containers.

#### Example:

```bash
docker stats
```

This command displays real-time resource usage statistics for all running containers.

### 5. Use the `docker top` command to view the processes running inside a container.

#### Example:

```bash
docker top <container_id>
```

Replace `<container_id>` with the actual container ID to view the processes running inside that container.

### 6. Use the `docker save` command to save an image to a tar archive.

#### Example:

```bash
docker save -o hello-world.tar hello-world
```

This command saves the "hello-world" image to a tar archive file named `hello-world.tar`.

### 7. Use the `docker load` command to load an image from a tar archive.

#### Example:

```bash
docker load -i hello-world.tar
```

This command loads the "hello-world" image from the `hello-world.tar` archive file.

These tasks involve simple operations that can be used to manage images and containers effectively.

## Reflection

Today's tasks provided a practical introduction to Docker commands essential for managing containers and images. Understanding these commands is crucial for deploying and scaling applications efficiently in a DevOps environment. Docker's ability to package applications into containers ensures consistency and reliability across different environments.

---

### References:

- [Docker Official Documentation](https://docs.docker.com/)
- [Docker Commands Cheat Sheet](https://www.docker.com/sites/default/files/d8/2019-09/docker-cheat-sheet.pdf)
- [TutorialsPoint: Docker](https://www.tutorialspoint.com/docker/index.htm)
- [Install Docker on AWS EC2](https://medium.com/@mehmetodabashi/how-to-install-docker-on-ec2-and-create-a-container-75ca88e342d2)
- [Introduction to Containers](https://www.youtube.com/watch?v=7JZP345yVjw)
- [Docker Tutorial on AWS EC2 as DevOps Engineer](https://www.youtube.com/watch?v=Tevxhn6Odc8)

---

**Happy Learning! 🚀**

Roshan Sahani

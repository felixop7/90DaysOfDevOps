# Day 16: Docker for DevOps Engineers 🚀

## Daily Log

**Date:** July 4, 2024

Today, we explored more advanced Docker concepts, focusing on Docker Compose and working with Docker images and containers. This provided a deeper understanding of managing multi-container applications and interacting with Docker containers using various commands.

## Key Concepts

### Docker Compose

Docker Compose is a tool that simplifies the management of multi-container Docker applications. It allows you to define and configure your application’s services in a YAML file. With a single command, you can start or stop all the services defined in the file. For more information, you can visit [this tutorial](https://tecadmin.net/tutorial/docker/docker-compose/).

### YAML

YAML (YAML Ain’t Markup Language) is a human-readable data serialization language often used for writing configuration files. It is easy to read and understand, making it popular for configuration management. For more information, you can read [this article](https://www.redhat.com/en/topics/automation/what-is-yaml).

## Tasks

### Task 1: Learn how to use the docker-compose.yml file

We learned how to set up the environment, configure services, link different containers, and use environment variables in the `docker-compose.yml` file.

#### Sample docker-compose.yml file:

```yaml
version: "3.3"
services:
  web:
    image: nginx:latest
    ports:
      - "80:80"
  db:
    image: mysql
    ports:
      - "3306:3306"
    environment:
      - "MYSQL_ROOT_PASSWORD=test@123"
```

### Task 2: Pull a pre-existing Docker image and run it on the local machine

#### Steps:

1. **Pull a Docker image:**

   ```bash
   docker pull nginx:latest
   ```

2. **Run the container as a non-root user:**

   ```bash
   sudo usermod -a -G docker $USER
   sudo reboot
   ```

3. **Run the container:**

   ```bash
   docker run -d -p 80:80 --name my-nginx nginx:latest
   ```

4. **Inspect the container's running processes and exposed ports:**

   ```bash
   docker inspect my-nginx
   ```

5. **View the container's log output:**

   ```bash
   docker logs my-nginx
   ```

6. **Stop and start the container:**

   ```bash
   docker stop my-nginx
   docker start my-nginx
   ```

7. **Remove the container when done:**

   ```bash
   docker rm -f my-nginx
   ```

### How to run Docker commands without sudo?

Make sure Docker is installed and the system is updated. Then, run:

```bash
sudo usermod -a -G docker $USER
sudo reboot
```

## Reflection

Today's tasks provided practical insights into using Docker Compose for managing multi-container applications and interacting with Docker containers using various commands. These skills are essential for efficient container management and deployment in real-world DevOps scenarios.

---

### References:

- [Docker Compose Tutorial](https://tecadmin.net/tutorial/docker/docker-compose/)
- [What is YAML?](https://www.redhat.com/en/topics/automation/what-is-yaml)
- [Docker Official Documentation](https://docs.docker.com/)
- [Docker Tutorial on AWS EC2 as DevOps Engineer](https://www.youtube.com/watch?v=Tevxhn6Odc8)

---

**Happy Learning! 🚀**

Roshan Sahani

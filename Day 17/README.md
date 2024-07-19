# Day 17: Docker for DevOps Engineers 🚀

## Daily Log

**Date:** July 5, 2024

Today, we explored advanced Docker concepts, focusing on Docker Volumes and Docker Networks. These concepts are crucial for managing data persistence and inter-container communication in Docker-based applications.

## Key Concepts

### Docker Volumes

Docker Volumes provide a way to store data outside of the container’s writable layer. They are useful for persisting data that should not be tied to the container's lifecycle. This allows for data persistence even when containers are deleted. You can learn more about Docker Volumes [here](https://docs.docker.com/storage/volumes/).

### Docker Network

Docker Network enables communication between containers and between containers and the host machine. It allows you to create isolated networks where containers can interact securely. More details about Docker Network can be found [here](https://docs.docker.com/network/).

## Tasks

### Task 1: Create a Multi-Container Docker-Compose File

We created a multi-container Docker-Compose file to manage an application and its database.

#### Hints:

- Use the `docker-compose up -d` command to start the application in detached mode.
- Use the `docker-compose scale` command to adjust the number of replicas for a service.
- Use the `docker-compose ps` command to view the status of all containers.
- Use the `docker-compose logs` command to view logs for a specific service.
- Use the `docker-compose down` command to stop and remove all containers, networks, and volumes.

#### Sample docker-compose.yml file:

```yaml
version: "3.3"
services:
  web:
    image: varsha0108/local_django:latest
    deploy:
      replicas: 2
    ports:
      - "8001-8005:8001"
    volumes:
      - my_django_volume:/app
  db:
    image: mysql
    ports:
      - "3306:3306"
    environment:
      - "MYSQL_ROOT_PASSWORD=test@123"
volumes:
  my_django_volume:
    external: true
```

### Commands to manage the multi-container application:

- Start the application in detached mode:

  ```bash
  docker-compose up -d
  ```

- View the status of all containers:

  ```bash
  docker-compose ps
  ```

- View logs for a specific service:

  ```bash
  docker-compose logs web
  ```

- Stop and remove all containers, networks, and volumes:

  ```bash
  docker-compose down
  ```

### Task 2: Using Docker Volumes and Named Volumes

#### Steps:

1. **Create and Run Containers with Shared Volume:**

   ```bash
   docker run -d --name container1 --mount source=my_volume,target=/app busybox
   docker run -d --name container2 --mount source=my_volume,target=/app busybox
   ```

2. **Verify Data Consistency:**

   ```bash
   docker exec container1 sh -c "echo 'Hello from container1' > /app/data.txt"
   docker exec container2 cat /app/data.txt
   ```

3. **List and Remove Volumes:**

   ```bash
   docker volume ls
   docker volume rm my_volume
   ```

## Reflection

Today's tasks provided valuable insights into managing data persistence and inter-container communication using Docker Volumes and Docker Networks. These skills are essential for building robust and scalable Docker-based applications.

---

### References:

- [Docker Volumes Documentation](https://docs.docker.com/storage/volumes/)
- [Docker Network Documentation](https://docs.docker.com/network/)
- [Docker Official Documentation](https://docs.docker.com/)

---

**Happy Learning! 🚀**

Roshan Sahani

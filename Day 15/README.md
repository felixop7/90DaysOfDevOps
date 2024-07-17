# Day 15: Docker Project for DevOps Engineers 🚀

## Daily Log

**Date:** July 3, 2024

Today was an exciting day as we delved into a practical DevOps project using Docker. The goal was to create, build, run, and push a Docker container for a simple web application. This hands-on project provided a comprehensive understanding of how Dockerfiles work and how to manage Docker images and containers.

## Key Concepts

### Dockerfile

A Dockerfile is a script that contains a series of instructions on how to build a Docker image. It specifies the base image, commands to run, files to copy, and the entry point of the application. For more about Dockerfiles, you can visit [this blog](https://blogs.rishikeshops.in/dockerfile-docker-compose-swarm-and-volumes).

## Tasks

### 1. Create a Dockerfile for a simple web application

#### Example Dockerfile for a Node.js application:

```Dockerfile
# Use the official Node.js image as the base image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port the app runs on
EXPOSE 8080

# Define the command to run the app
CMD ["node", "app.js"]
```

### 2. Build the image using the Dockerfile and run the container

#### Commands:

```bash
# Build the Docker image
docker build -t my-node-app .

# Run the Docker container
docker run -p 8080:8080 my-node-app
```

### 3. Verify that the application is working as expected by accessing it in a web browser

Open your web browser and go to `http://localhost:8080` to see if the application is running correctly.

### 4. Push the image to a public or private repository (e.g., Docker Hub)

#### Commands:

```bash
# Log in to Docker Hub
docker login

# Tag the image for Docker Hub
docker tag my-node-app felixop7/my-node-app

# Push the image to Docker Hub
docker push felixop7/my-node-app
```

## Reflection

Today's project was an excellent opportunity to apply Docker concepts to a real-world scenario. Creating a Dockerfile, building an image, running a container, and pushing the image to Docker Hub are fundamental skills for any DevOps engineer. These tasks demonstrated the power of Docker in packaging and deploying applications consistently across different environments.

---

### References:

- [Docker Official Documentation](https://docs.docker.com/)
- [Blog on Dockerfile, Docker Compose, Swarm, and Volumes](https://blogs.rishikeshops.in/dockerfile-docker-compose-swarm-and-volumes)
- [Docker Hub](https://hub.docker.com/)
- [Docker Tutorial on AWS EC2 as DevOps Engineer](https://www.youtube.com/watch?v=Tevxhn6Odc8)

---

**Happy Learning! 🚀**

Roshan Sahani

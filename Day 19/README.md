# Day 19: Getting Started with Jenkins 😃

## Daily Log

**Date:** July 7, 2024

Today, we will delve into Jenkins, an essential tool for implementing continuous integration and continuous delivery (CI/CD) pipelines. Jenkins is widely used in DevOps to automate the build, test, and deploy phases of software development.

## What is Jenkins?

Jenkins is an open-source automation server written in Java. It facilitates continuous integration and continuous delivery by automating the process of building, testing, and deploying software. Jenkins uses plugins to integrate various stages of the DevOps lifecycle, such as Git for source control, Maven for building projects, and Amazon EC2 for cloud deployments.

### Key Features:

- **Open-source**: Free to use and widely supported by a large community.
- **Automation**: Automates repetitive tasks in the software development process.
- **Plugins**: Extensive library of plugins to integrate with numerous tools and platforms.
- **Easy Setup**: Simple to install and configure on any operating system that supports Java.

### Why Use Jenkins?

In modern software development, automation is crucial for increasing efficiency and reducing manual errors. Jenkins allows developers to focus on writing code while it handles the repetitive tasks of building, testing, and deploying applications. This leads to faster development cycles, higher quality software, and more reliable releases.

## Tasks

### Task 1: What I Understood About Jenkins

Jenkins is an indispensable tool in the DevOps arsenal, designed to automate the entire CI/CD process. It simplifies the workflow by integrating with various tools through plugins, allowing seamless automation from code commit to deployment. Jenkins reduces manual intervention, ensuring that software builds are consistent and reliable. Its flexibility and extensibility make it suitable for projects of any size and complexity.

### Task 2: Create a Freestyle Pipeline to Print "Hello World!!"

**Steps to Create a Freestyle Project in Jenkins:**

1. **Open Jenkins Dashboard**: Access your Jenkins instance via the web interface.
2. **Create a New Job**: Click on "New Item" on the left-hand side menu.
3. **Name Your Project**: Enter a name for your project (e.g., "HelloWorldPipeline") and select "Freestyle project".
4. **Configure the Project**: In the project configuration page, navigate to the "Build" section.
5. **Add Build Step**: Click on "Add build step" and select "Execute shell" (or "Execute Windows batch command" for Windows).
6. **Enter the Command**: In the command box, enter the following:
   ```bash
   echo "Hello World!!"
   ```
7. **Save the Project**: Click "Save" to store your configuration.
8. **Build the Project**: Click "Build Now" on the project page.
9. **View Build Output**: Once the build is complete, click on the build number and then "Console Output" to see the "Hello World!!" message.

You have now created a simple Jenkins pipeline that prints "Hello World!!".

## References

- [GeeksforGeeks: What is Jenkins?](https://www.geeksforgeeks.org/what-is-jenkins/)

---

**Happy Learning! 🚀**

Roshan Sahani

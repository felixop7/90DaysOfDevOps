# Day 7: Package Managers and Systemctl/Systemd 🐧

## Daily Log

**Date:** June 25, 2024

Today, I delved into the world of package managers and explored the functionality of systemctl and systemd in Linux. Understanding package managers and system service management is crucial for effective system administration and DevOps practices.

## Key Concepts

### Package Managers

In the Linux ecosystem, a package manager is a vital tool that facilitates the installation, removal, upgrade, and management of software packages on an operating system. These can be graphical applications like software centers or command-line tools like apt-get or pacman.

### Package Installation

Different package managers, such as Yum, DNF, apt-get, and aptitude, are tailored for specific Linux distributions and enable the installation of various software packages, including Docker and Jenkins.

### Systemctl and Systemd

Systemctl is a command-line utility that allows users to examine and control the state of the "systemd" system and service manager. Systemd, in turn, is a system and service manager for Unix-like operating systems, providing a standard process for controlling system startup and managing system services.

## Tasks

### Installing Docker and Jenkins Using Package Managers

#### Ubuntu

1. **Installing Docker**:

   - Update the package list: `sudo apt-get update`.
   - Install Docker: `sudo apt-get install docker.io`.

2. **Installing Jenkins**:
   - Add the Jenkins repository key: `wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -`.
   - Append the Jenkins repository: `sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`.
   - Update the package list: `sudo apt-get update`.
   - Install Jenkins: `sudo apt-get install jenkins`.

#### CentOS

1. **Installing Docker**:

   - Install Docker: `sudo yum install docker`.

2. **Installing Jenkins**:
   - Add the Jenkins repository: `sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo`.
   - Install Jenkins: `sudo yum install jenkins`.

### Understanding Systemctl and Systemd

#### Task 1: Checking Docker Service Status

To check the status of the Docker service: `systemctl status docker`.

#### Task 2: Stopping the Jenkins Service

Capture the current status: `systemctl status jenkins`. Stop the service: `systemctl stop jenkins` and compare the status with the previous one.

#### Task 3: Understanding systemctl vs. service

Explore the differences between `systemctl` and `service` commands, such as `systemctl status docker` and `service docker status`.

# Service Management: systemctl vs service

## Overview

The `systemctl` and `service` commands are both used to manage system services on Linux, but they are part of different init systems. Below are the key differences between them:

## systemctl

- **Part of systemd:** `systemctl` is a command used to introspect and control the state of the `systemd` system and service manager.
- **Syntax:** The syntax generally follows the pattern `systemctl <command> <service>`. For example:
  - `systemctl start docker`
  - `systemctl stop docker`
  - `systemctl restart docker`
  - `systemctl status docker`
- **Features:** `systemctl` provides more advanced features and functionalities compared to `service`. It can be used to manage the state of services, mount points, devices, sockets, and other units.
- **Example:**
  `systemctl status docker`

## service

- **Part of SysVinit and others:** The `service` command is used for backward compatibility with older init systems like SysVinit. It acts as a wrapper to call the appropriate init script located in `/etc/init.d/`.
- **Syntax:** The syntax generally follows the pattern `service <service> <command>`. For example:
  - `service docker start`
  - `service docker stop`
  - `service docker restart`
  - `service docker status`
- **Features:** `service` is simpler and less powerful compared to `systemctl`. It does not provide as many features and is primarily used for basic service management.
- **Example:**
  `service docker status`

In conclusion, mastering package managers and systemctl/systemd is pivotal for effective system administration and software management in Linux environments.

## Reflection

Understanding the intricacies of package management and system service control provides a solid foundation for efficient system administration and DevOps practices. I'm excited to continue exploring these concepts as I progress in the #90DaysOfDevOps challenge!

## References

- [How to Check If the Docker Daemon or a Container Is Running](https://www.howtogeek.com/devops/how-to-check-if-the-docker-daemon-or-a-container-is-running/#:~:text=Checking%20With%20Systemctl&text=Check%20what%27s%20displayed%20under%20%E2%80%9CActive,running%20sudo%20systemctl%20start%20docker%20.)

---

Happy Learning! 🚀

**Roshan Sahani**

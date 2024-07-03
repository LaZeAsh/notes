---
title: "Docker"
---

Essentially Docker is an environment management tool that allows you to run your application on multiple different environments and manages all conflicts.

Book Definition: Docker is a tool which is used to automate the deployment of applications in lightweight containers so that applications can work efficiently in different environments

This would have been lovely to have during CalHacks where I spent most of my time trying to fix my environment for my image generation application

## Docker Client and Server

Contains of 2 main components:
- Docker Client: The primary way users interact with Docker, it provides a command line interface (CLI) for running commands and communicating with Docker Daemon
- Docker Server (Docker Daemon): Component responsible for managing Docker objects, such as images, containers, networks, and volumes. Listens for API requests from Docker Client and executes requested actions

![[Pasted image 20240625130234.png]]


## Docker Images

Docker images are read only templates that are used to create containers. An image consists of everything to run an application: code, runtime environment, libraries, env variables, and config files

Key features:
1. Immutability: Docker images are immutable, once created they cannot be changed and if they are changed it will create a new image
2. Layered Architecture: Images are built in layers. Layers are stocked in a dockerfile and only the top layer is writable
3. Efficiency: Due to shared layer architecture, docker images are space-efficient. Common layers can be shared across multiple images, saving storage space
4. Portability: Docker images can run on any system that supports Docker
5. Version Control: Images can be versioned and tagged

## Docker Containers

Docker containers are runtime instances of Docker Images. Docker Containers isolate an application in a lightweight, portable, and isolated environment. Containers are units in which Docker images are executed

Key Features:
1. Isolation: Containers run in isolation from each other and host system ensuring applications don't interfere with each other
2. Lightweight: Containers share Host OS Kernel making them more efficient and faster than virtual machines
3. Portable: Containers can run on different environments from developer's laptop to a prod server
4. Ephemeral: Containers can be stopped and removed without affecting the underlying system or other containers
5. Resource Efficiency: Containers use system resources more efficiently than in virtual machines
## Docker Registry

Docker registry is a place to store, distribute, and manage Docker images. Docker registry serves as a repository for Docker Images, allowing users to access and share images efficiently. 

Key Features:
1. Storage: Docker registries store Docker Images, allowing them to be pulled and used by users and automated systems
2. Versioning: Images in a registry can be tagged with versioning numbers
3. Access Control: Registries can enforce access control policies, allowing users to control who can push/pull images
4. Distribution: Registries distribute Docker Images to various environments, ensuring consistent deployment
5. Scalability: Registries can handle large numbers of images and high request volumes, supporting the needs of large teams and organizations.

TLDR: Docker is COOL and it would have saved me so much time if I integrated it into my workflow earlier. 
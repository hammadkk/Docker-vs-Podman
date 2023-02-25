# Docker-vs-Podman

# Comparing Two Popular Containerization Tools

![image](https://user-images.githubusercontent.com/85316531/219969237-bdb2127e-a9c6-4333-97c9-ccc30c248137.png)


Over time, containerization technology has grown in popularity, with two of the most well-known tools being Docker and Podman. Although both tools are used to deploy and manage containerized applications, there are some key distinctions between them. In this blog, we’ll look at what Docker and Podman are, how they’re used, how they differ, and which one is superior.

Before we jump into the topic, first let’s see what a container is.

# Unpacking Containers: What They Are, How They Work, and Why You Need Them.
![image](https://user-images.githubusercontent.com/85316531/219971403-601753dd-6026-4dd6-8ec9-bccf9bd94d93.png)

A container is a software package that includes all the necessary dependencies and libraries for an application to run. It uses operating system-level virtualization to create an isolated environment for the application to run in.

Before containers, developers faced difficulties configuring different environments for applications. Containers solve this problem by providing a consistent and portable runtime environment for applications to run in. They make it easy to move applications between different environments without modifying the code. This saves time and reduces errors in deployment and configuration thus becoming an essential part.

# What is docker and What it’s used for ?
Developers can package an application and all of its dependencies into a single container using the containerization tool known as Docker. It is the perfect solution for deploying applications across a variety of environments because it is portable, effective, and lightweight.

The foundation of containers is Docker images, which are kept in registries like Docker Hub using a client-server architecture. Applications are packaged, shipped, and run using Docker in a consistent and repeatable manner across various environments.

Furthermore, Docker containers are isolated from one another, enabling numerous containers to run independently on a single host. To manage large-scale container deployments, Docker supports container orchestration tools like Kubernetes and Docker Swarm.

# Docker Architecture:
![image](https://user-images.githubusercontent.com/85316531/219971443-1557ab6c-a282-450d-a2c1-8d00d2322bfc.png)

# Main Components of docker architecture:
1) Docker Containers: Docker containers are lightweight, portable, and self-contained environments that run applications. Each container is created from an image.
2) Docker Engine: The Docker Engine is the core component of the Docker that runs on the host machine. It is responsible for building, running, and managing Docker containers.
3) Docker Images: They contain everything needed to run an application, including the code, libraries, and dependencies.
4) Docker Hub: Docker Hub is a cloud-based service that provides a central location for Docker images.
5) Docker Client: The Docker Client is a command-line tool used to interact with Docker. Users can run and stop application commands to a Docker daemon using the command-line interface (CLI) provided by the Docker client.
6) Docker Daemon: The Docker daemon is responsible for handling incoming requests to the Docker API and overseeing the management of various Docker components such as containers, images, networks, and volumes.

# What is Podman?
Podman is a containerization tool that allows developers to create, run, and manage containers, similar to Docker but with some significant differences.

So before jumping into the difference first let’s see what Daemon is.

A daemon is a program or process that runs in the background and performs various tasks. Daemons are typically started when a system boots up and run continuously until the system is shut down.

In terms of containerization, A daemon is a background process used in containerization that controls and operates containers. It is in charge of creating, starting, stopping, and deleting containers. The daemon waits for requests from a client, like the Docker command-line interface, and then gets in touch with the container’s runtime to carry out the action.

# Difference between Docker and Podman.
Unlike Docker, Podman does not require a daemon and uses the “libpod” container engine. This standalone library means that Podman can be used without third-party tools.

Podman containers don’t need root access and can be run as regular processes, which can increase security. The need for root access to run Docker, on the other hand, raises security issues.

Docker Hub, a centralized repository for Docker images, is one of the Docker registries where Docker images are kept. Whereas Podman can manage images locally without the usage of a registry and can utilize any OCI-compliant registry which ensures that containers are portable across different container runtimes hence providing flexibility.

However, Since Docker has been around longer and is the more popular containerization platform, it has more third-party products and integrations. On the other side, Podman is a more recent tool that is growing in popularity because of its compatibility and security.

Note that both Docker and Podman have many similar commands and features.

# Docker Compose VS Podman Compose:
![image](https://user-images.githubusercontent.com/85316531/219971485-7555d251-7519-4f1f-b3f7-1e8bce4786a1.png)

Both the Podman Compose and Docker Compose tools are used to define and run multi-container applications. While having similar functions, there are some differences between the two.

Docker Compose requires a daemon to be running, Podman Compose does not. This makes Podman Compose a more flexible choice for some use cases since it can be utilized on computers that do not have Docker installed.

There are certain extra features in Podman Compose that are not present in Docker Compose. Podman compose gives the ability to non-root users to run containers without the need for special permissions. For developers who want to use pre-existing Docker images with Podman, Podman Compose also supports creating containers from a Docker file or a container images.

# Conclusion 
To conclude both Docker and Podman have advantages and disadvantages, and the best option will depend on your particular needs and requirements. If you’re not sure which to pick, it might be useful to try both and determine which one suits your use case the best.

# Docker 

## What are containers?

A container is a lightweight, standalone, portable, executable package of software that includes everything needed to run an application. 

They work by bundling an application along with all its dependencies, ensuring consistent performance across different environments—whether it's on your local machine, in the cloud, or on a server.

## Containers Contain:
- **Code**
- **Runtime**
- **System Libraries**
- **System Tools**
- **Settings**
- **All dependencies required for the app to run**

This essentially allows you to package software into standardised units for:
- **Development**
- **Shipment**
- **Deployment**

---

<img width="655" alt="Screenshot 2024-09-23 at 11 48 33" src="https://github.com/user-attachments/assets/823473bc-a62c-468a-92a8-a4bfa48982ff">

---

A container image is like a blueprint that includes everything needed to run an application. When this image is executed on Docker Engine, it becomes a live, running instance known as a container. A Docker image becomes a container when it is actively running on Docker.

### Components:
- **Infrastructure**: Physical/virtual hardware where everything runs.
- **OS**: the OS runs directly on the infrastructure and all containers share the host's kernel, the OS is the foundation for the components above it.
- **Docker Engine**: Provides the environment to build, run, and manage containers, making containerisation possible. Without the engine, nothing runs.
- **Docker Containers**: Hold the app and all its dependencies, e.g., bins/libs required by the app.

---

## Benefits of Containers

- **Isolation**: 
  Each container runs in its **own** environment, avoiding application conflicts and ensuring smooth operation. This is particularly important when applications require different versions of dependencies, such as Node.js 14 and Node.js 12.

- **Consistent Environment**: 
  Containers provide a consistent environment for applications, ensuring they behave the same way regardless of where they are deployed. This reduces "it works on my machine" issues, making development and deployment more predictable and reliable.

- **Portability**: 
  Containers run consistently across different environments without modifications, enhancing flexibility in deployment.

- **Efficiency**: 
  Containers are lightweight and start quickly, sharing the host OS kernel. They are more resource-efficient than traditional VMs, allowing for higher application density.

- **Simplified Maintenance**: 
  Updating and rolling back applications is straightforward by simply replacing container images.


# Docker

Docker is an open-source platform that allows developers to automate the deployment of applications inside lightweight, portable containers. It streamlines the development process, improves resource efficiency, and simplifies application management by enabling easy updates and rollbacks.

## Core Components in Docker

1. **Docker Engine**: The core service that allows you to build, run, and manage containers. It consists of a server, REST API, and a command-line interface (CLI).
  
2. **Docker Hub**: A cloud-based repository for sharing and managing Docker images. It allows users to upload, download, and collaborate on images easily—think of it as the app store for Docker images.

3. **Docker Compose**: A tool for defining and running multi-container Docker applications using a YAML file. It simplifies the orchestration of multiple containers and their configurations.

## Images and Containers

- **Docker Images**: Read-only templates used to create containers. They contain everything needed to run an application, including code, libraries, and environment variables.

- **Docker Containers**: Lightweight, standalone executable packages that run applications. They are created from Docker images and provide an isolated environment for applications.

> **Remember:** A Docker image is like a recipe, while a Docker container is the actual dish prepared from that recipe. An image provides the necessary components, and a container runs those components in an isolated environment.

## How to Create a Docker Image

- **Using a Dockerfile**: A text file containing instructions that Docker uses to assemble a Docker image. It specifies the base image, application code, dependencies, and configuration needed to set up the environment.

Docker images are **immutable**, meaning once they are created, they do not change. If you want to update or modify an image, you have to create a new one. This immutability ensures consistency and reliability regardless of where it is deployed, making it easier to track versions and roll back if necessary.

## Why is Docker Important?

1. **Simplified Deployment**: Ensures apps work consistently across different environments by packaging applications with all their dependencies, facilitating smooth rollouts.

2. **Resource Efficiency**: Containers start up quickly because they are lightweight and share the host OS's kernel. This allows for almost instantaneous launches, making containers ideal for microservices and dynamic workloads.

3. **Enhanced Collaboration**: Provides consistent development environments, reducing friction and minimizing discrepancies. New team members can quickly pull necessary images and get started without extensive setup.

4. **Streamlined Workflows**: Integrates seamlessly with CI/CD pipelines, allowing automated testing, building, and deployment of applications for faster delivery and fewer errors.

## VMs vs. Containers

<img width="655" alt="Screenshot 2024-09-23 at 13 38 50" src="https://github.com/user-attachments/assets/0041249d-e58c-440f-acf2-e19e3909d18a">

### Components of a VM

A VM allows multiple operating systems to run on a single physical machine.

1. **Infrastructure**: The physical or virtual hardware that serves as the foundation for running VMs.

2. **Operating System**: The host operating system that manages hardware resources and runs the hypervisor.

3. **Hypervisor**: A layer of software that creates and manages VMs by allocating resources such as CPUs, memory, and storage. It ensures isolation between VMs.

4. **Guest Operating System**: Each VM runs its own guest OS, isolated from others, ensuring applications do not affect each other.

5. **Binaries and Libraries**: Each VM includes its own binaries, libraries, and necessary components required for applications, contributing to resource intensity.

### Resource Consumption

Due to their isolated nature and inclusion of separate operating systems, VMs can be resource-intensive, consuming significant CPU, memory, and storage compared to containers.

## Components of a Container

Containers are lightweight, portable units that package applications along with their dependencies, providing a consistent environment for deployment. They share the host OS.

### Components of a Container

1. **Infrastructure**: The physical or virtual hardware that hosts the containers.

2. **Operating System (OS)**: Containers share the host OS kernel, allowing them to run efficiently without needing a full OS for each instance.

3. **Docker Engine**: A software component that manages the execution of containers, providing the necessary environment to build, run, and manage them.

4. **Docker Images**: Lightweight, standalone executable packages containing everything needed to run an application.

Containers are faster and more efficient than VMs because they run in isolated environments while sharing the underlying OS. This design allows for higher application density, making them ideal for modern, dynamic workloads.

| Feature               | Virtual Machines (VMs)                                  | Containers                                      |
|-----------------------|--------------------------------------------------------|------------------------------------------------|
| **Architecture**      | Each VM includes a full OS with its own kernel        | Containers share the host OS kernel            |
| **Resource Usage**    | More resource-intensive due to multiple OS instances   | Lightweight, using fewer resources              |
| **Startup Time**      | Slower startup time (minutes) due to full OS boot-up  | Quick startup (seconds) as only the application runs |
| **Isolation**         | Strong isolation, mimicking physical machines          | Process-level isolation; less overhead          |
| **Portability**       | Less portable; dependent on the hypervisor             | Highly portable across different environments    |
| **Use Cases**         | Suitable for running different OS types or complex applications | Ideal for microservices, quick deployment, and scaling |

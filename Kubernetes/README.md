## Kubernetes

- **what?** an open-source container orchestration technology developed by Google
- **why?** to help automate the deployment, scaling, and management of containerised applications
- **goal?** make it easier to manage large-scale applications consistently and reliably
- **how?** by packaging codebase for the app with all required dependencies inc tools, config files, runtimes

### Overview of containers

- Running apps start with physical hardware,i.e. machines equipped with computing power, CPU, storage, and networking capabilities.
- Traditionally, applications ran inside VMs
- VMs operate within a guest OS that runs on the host system's hardware, providing full isolation, which means issues in one VM rarely impact others.
- However, VMs are often resource-heavy and inefficient.
- Containers offer a lightweight alternative, providing similar isolation with significantly less overhead.
- Therefore containers are perfect for running microservices in the cloud

### Archictecture of Containers

<img width="500" alt="Screenshot 2024-11-02 at 03 47 35" src="https://github.com/user-attachments/assets/70b415e5-3788-4808-87da-af561df9d9b0">

- **Kernel:** Shared OS core enabling lightweight virtualisation.
- **Docker:** orchestrates container operations e.g creating, running, and stopping containers
- **Bins/Libs:** Essential dependencies shared across containers.
- **Container:** Isolated environment for applications.
- **Application:** The software/service running within the container.

### Cgroups and Namespaces

- **Cgroups (Control Groups):** Used to allocate and limit resources (CPU, memory, disk I/O, network bandwidth, etc.) for processes. They help ensure that no single process or group of processes can monopolise system resources.
- **Namespaces:** Provide isolation for system resources (e.g., process IDs, network stacks, filesystems), allowing containers to run independently without interfering with each other or the host system, thus enhancing security and modularity.

### What problem is Kubernetes trying to solve?

- it addresses the challenge of managing containerised applications at scale, ensuring efficient resource utilisation, seamless deployment, and resilience in dynamic environments.

### How does it solve this problem?

- **Efficient Resource Management:** Kubernetes optimally schedules multiple pods (which can contain one or more containers) across nodes, maximising resource usage and minimising waste.
- **Scalability:** It allows for the seamless scaling of applications by dynamically adjusting the number of running containers based on demand, ensuring that applications remain responsive under varying workloads.

### Componenet of K8s Architecture

<img width="439" alt="Screenshot 2024-11-02 at 04 36 54" src="https://github.com/user-attachments/assets/bb099144-6a92-4ace-9d04-9d522072b7b3">

| Component            | Description                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------|
| **Pod**              | The smallest deployable unit in Kubernetes; can contain one or more containers with shared resources. |
| **Kubelet**          | Node agent that ensures containers are running in a pod as specified by the master node.       |
| **Kube-Proxy**       | Manages network communication within the cluster and routes traffic to the correct pods.         |
| **Node**             | A worker machine where Kubernetes runs pods and hosts applications.        |
| **Cluster**          | A set of nodes managed by Kubernetes to collectively run and scale applications.                 |
| **Master Node**    | Manages the overall state of the cluster, including scheduling, networking, and scaling.         |
| **API Server**       | The master node’s front-end; handles communication between users and the cluster.              |
| **Kube Controller Manager** | Runs processes (controllers) that monitor and adjust cluster state to match desired configurations. |
| **etcd**             | A key-value store maintaining the cluster’s configuration and state consistency.                 |
| **Kube Scheduler**        | Assigns pods to nodes based on resource availability and other constraints for optimal workload distribution. |
| **Container Runtime**| Software responsible for running containers, such as Docker or containerd.                       |
|**Cloud Controller Manager**| Interfaces with cloud provider APIs to handle cloud-specific resources, such as provisioning load balancers, volumes, and network routing.|


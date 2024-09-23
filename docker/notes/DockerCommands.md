# Common Docker commands

| **Command**                     | **Description**                                       |
|---------------------------------|-------------------------------------------------------|
| `docker run`                    | Create and start a container from an image.          |
| `docker ps`                     | List running containers.                              |
| `docker ps -a`                  | List all containers, including stopped ones.        |
| `docker images`                 | List all available images on the local system.      |
| `docker pull <image>`          | Download an image from a Docker registry (Docker Hub). |
| `docker build -t <name> <path>` | Build an image from a Dockerfile.                   |
| `docker exec -it <container> <command>` | Run a command in a running container.           |
| `docker stop <container>`       | Stop a running container.                             |
| `docker start <container>`      | Start a stopped container.                            |
| `docker rm <container>`         | Remove a stopped container.                           |
| `docker rmi <image>`           | Remove an image from the local system.               |
| `docker logs <container>`       | View logs from a running or stopped container.       |
| `docker-compose up`             | Start services defined in a `docker-compose.yml` file. |
| `docker-compose down`           | Stop and remove services defined in a `docker-compose.yml` file. |


# 🐳 Docker Command Cheat Sheet

This document provides a comprehensive list of Docker commands with descriptions for easy reference. Ideal for developers, sysadmins, and DevOps engineers working with containers.

---

## 📦 Docker Installation & Version
```bash
docker --version
```
Check Docker version.

```bash
docker version
```
Display detailed client and server version information.

```bash
docker info
```
Display system-wide Docker information.

---

## 🧱 Docker Images
```bash
docker images
```
List all local images.

```bash
docker pull <image_name>
```
Download an image from Docker Hub.

```bash
docker build -t <name>:<tag> .
```
Build an image from a Dockerfile.

```bash
docker rmi <image_id_or_name>
```
Remove one or more images.

```bash
docker tag <image> <new_name>
```
Tag an image for a repository.

---

## 🚢 Docker Containers
```bash
docker ps
```
List all running containers.

```bash
docker ps -a
```
List all containers (running + stopped).

```bash
docker run <image>
```
Run a container from an image.

```bash
docker run -d <image>
```
Run a container in detached mode.

```bash
docker run -it <image> /bin/bash
```
Run a container in interactive mode with terminal.

```bash
docker stop <container_id_or_name>
```
Stop a running container.

```bash
docker start <container_id_or_name>
```
Start a stopped container.

```bash
docker restart <container_id_or_name>
```
Restart a container.

```bash
docker rm <container_id_or_name>
```
Remove a container.

```bash
docker exec -it <container_id> <cmd>
```
Run a command inside a running container.

---

## 🗂️ Docker Volumes
```bash
docker volume create <name>
```
Create a new volume.

```bash
docker volume ls
```
List all volumes.

```bash
docker volume inspect <name>
```
Display detailed information on a volume.

```bash
docker volume rm <name>
```
Remove a volume.

---

## 🛠️ Docker Networks
```bash
docker network ls
```
List all Docker networks.

```bash
docker network create <name>
```
Create a new network.

```bash
docker network inspect <name>
```
Display details of a network.

```bash
docker network rm <name>
```
Remove a Docker network.

---

## 🧪 Dockerfile Example
```Dockerfile
FROM node:18
WORKDIR /app
COPY . .
RUN npm install
CMD ["node", "index.js"]
```
Basic Dockerfile for a Node.js application.

---

## 🐙 Docker Compose
```bash
docker-compose up
```
Start all services defined in docker-compose.yml.

```bash
docker-compose up -d
```
Start services in detached mode.

```bash
docker-compose down
```
Stop and remove containers, networks, images, and volumes.

```bash
docker-compose build
```
Build or rebuild services.

```bash
docker-compose ps
```
List containers related to the services.

```bash
docker-compose logs
```
View output from containers.

---

## 🧹 Docker Cleanup & Context
```bash
docker context ls
```
List available Docker contexts.

```bash
docker system prune
```
Remove all unused data (containers, networks, images, etc.).

```bash
docker image prune
```
Remove unused images.

```bash
docker container prune
```
Remove stopped containers.

```bash
docker volume prune
```
Remove unused volumes.

---

## 📄 Commonly Used Flags

| Flag        | Description                           |
|-------------|---------------------------------------|
| `-d`        | Detached mode                         |
| `-it`       | Interactive terminal                  |
| `--name`    | Assign custom container name          |
| `-p`        | Port mapping (e.g., `-p 8080:80`)     |
| `-v`        | Volume mount (e.g., `-v vol:/data`)   |

---

Made with ❤️ for Docker users.

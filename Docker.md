Certainly! Here's a Docker CLI cheat sheet with commonly used commands for managing Docker containers and images:

### **Docker Information and Version:**
1. Show Docker version information:
    ```bash
    docker version
    ```

2. Display system-wide information about Docker:
    ```bash
    docker info
    ```

### **Working with Images:**
3. List locally available images:
    ```bash
    docker images
    ```

4. Pull an image from Docker Hub:
    ```bash
    docker pull <image-name>:<tag>
    ```

5. Build an image from a Dockerfile:
    ```bash
    docker build -t <image-name>:<tag> <path-to-dockerfile>
    ```

6. Remove an image:
    ```bash
    docker rmi <image-name>:<tag>
    ```

### **Working with Containers:**
7. Run a container:
    ```bash
    docker run <image-name>:<tag>
    ```

8. Run a container in the background with a specific name:
    ```bash
    docker run -d --name <container-name> <image-name>:<tag>
    ```

9. List running containers:
    ```bash
    docker ps
    ```

10. List all containers (including stopped ones):
    ```bash
    docker ps -a
    ```

11. Stop a running container:
    ```bash
    docker stop <container-id or container-name>
    ```

12. Start a stopped container:
    ```bash
    docker start <container-id or container-name>
    ```

13. Remove a stopped container:
    ```bash
    docker rm <container-id or container-name>
    ```

14. Remove a running container:
    ```bash
    docker rm -f <container-id or container-name>
    ```

15. View logs of a running container:
    ```bash
    docker logs <container-id or container-name>
    ```

16. Execute a command in a running container:
    ```bash
    docker exec -it <container-id or container-name> <command>
    ```

### **Networking:**
17. Show port mappings of a running container:
    ```bash
    docker port <container-id or container-name>
    ```

18. Expose a port from a container to the host:
    ```bash
    docker run -p <host-port>:<container-port> <image-name>:<tag>
    ```

### **Volumes:**
19. List volumes:
    ```bash
    docker volume ls
    ```

20. Create a named volume:
    ```bash
    docker volume create <volume-name>
    ```

21. Mount a volume in a container:
    ```bash
    docker run -v <host-path>:<container-path> <image-name>:<tag>
    ```

### **Cleanup:**
22. Remove all stopped containers:
    ```bash
    docker container prune
    ```

23. Remove all unused images:
    ```bash
    docker image prune -a
    ```

24. Remove all unused volumes:
    ```bash
    docker volume prune
    ```

Remember to replace placeholders like `<image-name>:<tag>`, `<container-id or container-name>`, etc., with your actual image and container names. Additionally, some commands may require administrator privileges depending on your Docker setup.
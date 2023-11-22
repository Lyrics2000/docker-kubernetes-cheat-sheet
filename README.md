
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




Certainly! Below is a Kubernetes CLI cheat sheet with commonly used commands. Please note that some commands might need adjustment based on your specific use case and configuration.

### Basic Operations:

1. **Get Cluster Information:**
   ```bash
   kubectl cluster-info
   ```

2. **Display Kubernetes Version:**
   ```bash
   kubectl version
   ```

3. **List Nodes:**
   ```bash
   kubectl get nodes
   ```

4. **List Pods:**
   ```bash
   kubectl get pods
   ```

5. **List Services:**
   ```bash
   kubectl get services
   ```

### Work with Deployments:

6. **List Deployments:**
   ```bash
   kubectl get deployments
   ```

7. **Scale a Deployment:**
   ```bash
   kubectl scale deployment <deployment-name> --replicas=<desired-replica-count>
   ```

8. **Update a Deployment:**
   ```bash
   kubectl set image deployment/<deployment-name> <container-name>=<new-image>
   ```

### Interact with Pods:

9. **Get Pod Details:**
   ```bash
   kubectl describe pod <pod-name>
   ```

10. **Tail Pod Logs:**
    ```bash
    kubectl logs -f <pod-name>
    ```

11. **Execute Command in Pod:**
    ```bash
    kubectl exec -it <pod-name> -- /bin/bash
    ```

12. **Copy files to/from Pod:**
    ```bash
    kubectl cp <local-file> <pod-name>:<pod-path>
    kubectl cp <pod-name>:<pod-path> <local-file>
    ```

### Manage Services:

13. **Expose a Deployment as a Service:**
    ```bash
    kubectl expose deployment <deployment-name> --type=NodePort --port=<port>
    ```

14. **Delete a Service:**
    ```bash
    kubectl delete service <service-name>
    ```

### ConfigMaps and Secrets:

15. **Create ConfigMap:**
    ```bash
    kubectl create configmap <configmap-name> --from-file=<path-to-file>
    ```

16. **Create Secret:**
    ```bash
    kubectl create secret generic <secret-name> --from-literal=<key>=<value>
    ```

### Networking:

17. **Port Forwarding:**
    ```bash
    kubectl port-forward <pod-name> <local-port>:<pod-port>
    ```

18. **Get External IP of Service:**
    ```bash
    kubectl get svc <service-name> -o jsonpath='{.status.loadBalancer.ingress[0].ip}'
    ```

### Monitoring and Troubleshooting:

19. **View Resource Usage of Pods:**
    ```bash
    kubectl top pods
    ```

20. **Describe Resource Quotas:**
    ```bash
    kubectl describe resourcequota
    ```

21. **Troubleshoot Pod Issues:**
    ```bash
    kubectl describe pod <pod-name>
    kubectl logs <pod-name>
    ```

### Clean Up:

22. **Delete Resources:**
    ```bash
    kubectl delete deployment <deployment-name>
    kubectl delete pod <pod-name>
    kubectl delete service <service-name>
    ```

23. **Delete All Resources in a Namespace:**
    ```bash
    kubectl delete all --all -n <namespace>
    ```

Remember to replace placeholders like `<deployment-name>`, `<pod-name>`, `<service-name>`, `<configmap-name>`, etc., with your actual resource names. Additionally, some commands may require administrator privileges depending on your Kubernetes setup.Certainly! Below is a Kubernetes CLI cheat sheet with commonly used commands. Please note that some commands might need adjustment based on your specific use case and configuration.

### Basic Operations:

1. **Get Cluster Information:**
   ```bash
   kubectl cluster-info
   ```

2. **Display Kubernetes Version:**
   ```bash
   kubectl version
   ```

3. **List Nodes:**
   ```bash
   kubectl get nodes
   ```

4. **List Pods:**
   ```bash
   kubectl get pods
   ```

5. **List Services:**
   ```bash
   kubectl get services
   ```

### Work with Deployments:

6. **List Deployments:**
   ```bash
   kubectl get deployments
   ```

7. **Scale a Deployment:**
   ```bash
   kubectl scale deployment <deployment-name> --replicas=<desired-replica-count>
   ```

8. **Update a Deployment:**
   ```bash
   kubectl set image deployment/<deployment-name> <container-name>=<new-image>
   ```

### Interact with Pods:

9. **Get Pod Details:**
   ```bash
   kubectl describe pod <pod-name>
   ```

10. **Tail Pod Logs:**
    ```bash
    kubectl logs -f <pod-name>
    ```

11. **Execute Command in Pod:**
    ```bash
    kubectl exec -it <pod-name> -- /bin/bash
    ```

12. **Copy files to/from Pod:**
    ```bash
    kubectl cp <local-file> <pod-name>:<pod-path>
    kubectl cp <pod-name>:<pod-path> <local-file>
    ```

### Manage Services:

13. **Expose a Deployment as a Service:**
    ```bash
    kubectl expose deployment <deployment-name> --type=NodePort --port=<port>
    ```

14. **Delete a Service:**
    ```bash
    kubectl delete service <service-name>
    ```

### ConfigMaps and Secrets:

15. **Create ConfigMap:**
    ```bash
    kubectl create configmap <configmap-name> --from-file=<path-to-file>
    ```

16. **Create Secret:**
    ```bash
    kubectl create secret generic <secret-name> --from-literal=<key>=<value>
    ```

### Networking:

17. **Port Forwarding:**
    ```bash
    kubectl port-forward <pod-name> <local-port>:<pod-port>
    ```

18. **Get External IP of Service:**
    ```bash
    kubectl get svc <service-name> -o jsonpath='{.status.loadBalancer.ingress[0].ip}'
    ```

### Monitoring and Troubleshooting:

19. **View Resource Usage of Pods:**
    ```bash
    kubectl top pods
    ```

20. **Describe Resource Quotas:**
    ```bash
    kubectl describe resourcequota
    ```

21. **Troubleshoot Pod Issues:**
    ```bash
    kubectl describe pod <pod-name>
    kubectl logs <pod-name>
    ```

### Clean Up:

22. **Delete Resources:**
    ```bash
    kubectl delete deployment <deployment-name>
    kubectl delete pod <pod-name>
    kubectl delete service <service-name>
    ```

23. **Delete All Resources in a Namespace:**
    ```bash
    kubectl delete all --all -n <namespace>
    ```

Remember to replace placeholders like `<deployment-name>`, `<pod-name>`, `<service-name>`, `<configmap-name>`, etc., with your actual resource names. Additionally, some commands may require administrator privileges depending on your Kubernetes setup.






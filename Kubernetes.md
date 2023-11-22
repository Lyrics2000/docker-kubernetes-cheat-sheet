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
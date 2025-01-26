```markdown

  Kubectl Cheatsheet

```

## 1. Kubectl get

**Description**: Retrieves information about resources. This command lists the pods running in your cluster, showing basic details such as names, statuses, and resource usage.

```bash

  kubectl get pods

```

## 2. Kubectl create

**Description**: Creates a resource. This command creates a new deployment with the specified name (`my-deployment`) and uses the `nginx` image for the containers.

```bash

  kubectl create deployment my-deployment --image=nginx

```

## 3. Kubectl apply

**Description**: Applies changes to resources. This command takes the contents of the `deployment.yaml` file and creates or updates resources defined within the YAML.

```bash

  kubectl apply -f deployment.yaml

```

## 4. Kubectl delete

**Description**: Deletes a resource. This command deletes the pod named `my-pod` from your Kubernetes cluster.

```bash

  kubectl delete pod my-pod

```

## 5. Kubectl get nodes

**Description**: Retrieves information about nodes in the cluster. It lists all the nodes in your Kubernetes cluster, showing details like node names, status, and roles.

```bash

  kubectl get nodes

```

## 6. Kubectl describe

**Description**: Displays detailed information about resources. This command shows in-depth details about the pod `my-pod`, such as resource usage, events, and container states.

```bash

  kubectl describe pod my-pod

```

## 7. Kubectl logs

**Description**: Displays log output for a container. This command fetches and displays logs from the container running within the specified pod (`my-pod`).

```bash

  kubectl logs pod my-pod

```

## 8. Kubectl exec

**Description**: Executes a command in a running container. This command opens an interactive terminal (`/bin/bash`) inside the container running in the `my-pod`.

```bash

  kubectl exec -it my-pod -- /bin/bash

```

## 9. Kubectl port-forward

**Description**: Exposes a service to the local machine. This command forwards traffic from your local machine's port `8080` to the Kubernetes service's port `80`.

```bash

  kubectl port-forward svc/my-service 8080:80

```

## 10. Kubectl rollout status

**Description**: Displays the current rollout status of an application. This command checks and displays the status of a deployment, showing if it’s successfully rolling out or encountering issues.

```bash

  kubectl rollout status deployment my-deployment

```

## 11. Kubectl apply-branch

**Description**: Applies a specified branch to a deployment. This command applies updates from the `production` branch to the deployment `my-deployment`.

```bash

  kubectl apply-branch production deployment=my-deployment

```

## 12. Kubectl expose

**Description**: Exposes a service to the cluster. This command creates a service from the deployment `my-deployment` and exposes it on port `30080` for external access.

```bash

  kubectl expose deployment my-deployment --type=NodePort --port=30080

```

## 13. Kubectl label

**Description**: Applies or removes labels from resources. This command adds a label `env=dev` to the pod `my-pod`, which can be used for selection or identification purposes.

```bash

  kubectl label pod my-pod env=dev

```

## 14. Kubectl annotate

**Description**: Applies or removes annotations from resources. This command adds an annotation `foo=bar` to the pod `my-pod` for additional metadata.

```bash

  kubectl annotate pod my-pod foo=bar

```

## 15. Kubectl exec -it --stdin --tty --command

**Description**: Executes a command in a running container with stdin, tty, and command-line options. This command runs `ls -l` inside the container, providing interactive terminal output.

```bash

  kubectl exec -it --stdin --tty --command="ls -l" my-pod

```

## 16. Kubectl get events

**Description**: Retrieves information about events that have occurred in the cluster. This command fetches and displays recent events like pod creations, deletions, and failures.

```bash

  kubectl get events

```

## 17. Kubectl describe node

**Description**: Displays detailed information about a node in the cluster. This command shows a detailed description of the specified node, including its status, capacity, and running pods.

```bash

  kubectl describe node <node-name>

```

## 18. Kubectl drain

**Description**: Drains nodes from running pods. This command safely evicts all pods from the `my-node`, preparing it for maintenance by disabling scheduling of new pods.

```bash

  kubectl drain node my-node --force

```

## 19. Kubectl cordon

**Description**: Cords a node to be managed by the cluster. This command marks the node `my-node` as unschedulable, preventing new pods from being scheduled on it.

```bash

  kubectl cordon node my-node

```

## 20. Kubectl unpard (Not available)

**Description**: Kubectl does not have an `unpard` command. This note clarifies that the `unpard` command does not exist in Kubernetes, and the system uses YAML/JSON files for resource creation.

```bash

  kubectl unpard (Not available)

```

## 21. Kubectl get deployments

**Description**: Retrieves information about all deployments in the cluster. This command lists all the deployments in your cluster, showing details like the number of pods and replicas.

```bash

  kubectl get deployments

```

## 22. Kubectl get replicasets

**Description**: Retrieves information about all replica sets in the cluster. It lists all replica sets, showing their names, labels, and the number of pods managed.

```bash

  kubectl get replicasets

```

## 23. Kubectl describe deployments

**Description**: Displays detailed information about a deployment in the cluster. This command shows the details of the `my-deployment`, including its pods, replicas, and status.

```bash

  kubectl describe deployments my-deployment

```

## 24. Kubectl describe replica-sets

**Description**: Displays detailed information about a replica set in the cluster. It shows details like the number of pods, status, and events related to the `my-replica-set`.

```bash

  kubectl describe replica-set my-replica-set

```

## 25. Kubectl get pods -l

**Description**: Retrieves information about all pods with a specific label. This command lists all pods that have the label `app=my-app` applied to them.

```bash

  kubectl get pods -l app=my-app

```

## 26. Kubectl get services

**Description**: Retrieves information about all services in the cluster. This command lists all services, showing their names, types, and ports.

```bash

  kubectl get services

```

## 27. Kubectl describe services

**Description**: Displays detailed information about a service in the cluster. This command gives insights into the configuration and status of the `my-service`.

```bash

  kubectl describe service my-service

```

## 28. Kubectl get persistentvolumes

**Description**: Retrieves information about all persistent volumes in the cluster. This command lists all persistent volumes available in the cluster, with their status and capacity.

```bash

  kubectl get persistentvolumes

```

## 29. Kubectl get configmaps

**Description**: Retrieves information about all config maps in the cluster. It lists all config maps and their data within the cluster.

```bash

  kubectl get configmaps

```

## 30. Kubectl describe configmaps

**Description**: Displays detailed information about a config map in the cluster. This command shows the contents and metadata of the `my-configmap`.

```bash

  kubectl describe configmap my-configmap

```

## 31. Kubectl get persistentvolumes -o yaml

**Description**: Retrieves information about all persistent volumes in the cluster, formatted as YAML. This command outputs the persistent volumes in YAML format for easy parsing.

```bash

  kubectl get persistentvolumes -o yaml

```

## 32. Kubectl apply --allow-unmanaged

**Description**: Applies changes to resources without requiring a managed control plane. This command applies updates to the `my-deployment` even in unmanaged environments.

```bash

  kubectl apply --allow-unmanaged deployment my-deployment

```

## 33. Kubectl delete all

**Description**: Deletes all resources in the cluster. This command deletes all the pods, deployments, services, and other resources in the current namespace.

```bash

  kubectl delete all

```

## 34. Kubectl get deployments -l

**Description**: Retrieves information about all deployments with a specific label. This command lists deployments that match the label `app=my-app`.

```bash

  kubectl get deployments -l app=my-app

```

## 35. Kubectl create deployment --image=nginx

**Description**: Creates a new deployment from a YAML file. This command creates a deployment named `my-deployment` using the `nginx` image.

```bash

  kubectl create deployment my-deployment --image=nginx

```

## 36. Kubectl rollout update

**Description**: Updates the current rollout state of an application. This command updates the deployment `my-deployment`, ensuring the latest version is deployed.

```bash

  kubectl rollout update deployment my-deployment

```

## 37. Kubectl get deployment

**Description**: Retrieves information about all deployments in the cluster. It lists all the deployments, showing their names, replica counts, and statuses.

```bash

  kubectl get deployment

```

## 38. Kubectl describe pod

**Description**: Displays detailed information about a pod in the cluster. This command provides detailed information on the pod `my-pod`, including containers, events, and resource usage.

```bash

  kubectl describe pod my-pod

```

## 39. Kubectl exec -it --stdin --tty --command

**Description**: Executes a command in a running container with stdin, tty, and command-line options. This command runs `ls -l` in the container of the `my-pod` and allows interactive terminal access.

```bash

  kubectl exec -it --stdin --tty --command="ls -l" my-pod

```

## 40. Kubectl get deployment status

**Description**: Displays the current rollout status of an application. This command checks the status of the deployment and reports if it's successfully rolling out or encountering issues.

```bash

  kubectl get deployment status

```

## 41. Kubectl describe node

**Description**: Displays detailed information about a node in the cluster. This command provides detailed status, capacity, and pod information for a specific node in your cluster.

```bash

  kubectl describe node <node-name>

```

## 42. Kubectl cordon node my-node --force

**Description**: Cordons a node to be managed by the cluster, forcing the node to be cordoned even if it's not running. This command prevents new pods from being scheduled on the `my-node`.

```bash

  kubectl cordon node my-node --force

```

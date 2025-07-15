# Kubernetes Voting App Deployment

This project demonstrates how to deploy a simple voting application using Kubernetes on Minikube. It includes deployments and services for the following components:

- Voting App
- Result App
- Worker
- Redis
- PostgreSQL Database

## Project Structure

- `deployment/`: Contains Kubernetes Deployment and Service YAML files for each component.
- `pods/`: Contains individual Pod and Service YAML files for manual pod creation and testing.

## Prerequisites

- [Minikube](https://minikube.sigs.k8s.io/docs/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## How to Deploy

1. **Start Minikube:**

   ```sh
   minikube start
   ```

2. **Apply Deployments and Services:**

   ```sh
   kubectl apply -f deployment/
   ```

   This will create all deployments and services defined in the `deployment/` directory.

3. **Check Status:**

   ```sh
   kubectl get pods
   kubectl get services
   ```

4. **Access the Voting App and Result App:**
   - Find the NodePort for the voting and result services:
     ```sh
     kubectl get svc
     ```
   - Use Minikube to access the services:
     ```sh
     minikube service vote --url
     minikube service result --url
     ```

## Demo

Below are screenshots of the deployed application running on Minikube:

<!-- Add your screenshots here -->

---

Feel free to experiment with the pod YAML files in the `pods/` directory for manual testing and learning.

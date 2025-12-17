# Docker + Kubernetes Deployment

The Java application is **containerized using Docker** and **orchestrated using Kubernetes (Minikube)**.


### Docker Implementation

- Created `Dockerfile`  
- Application packaged as an image  
- Image deployed locally / registry optional  


### Kubernetes Deployment

| Component | Description |
|-----------|-------------|
| Deployment | Creates multiple Pods |
| Service | Exposes the app externally |
| ReplicaSet | Ensures high availability |
| Pods | Runs app instances |

### Why This Matters?

- Shows **cloud-native, scalable deployment**.
- Demonstrates understanding of **cluster networking + high availability**.

## Docker Image Build

![Docker Image](Screenshots/docker-image-built.png)

## Docker Compose Deployment (EC2 / Local)

![Docker Compose](Screenshots/docker-compose-ec2.png)

## Application Access via Docker Compose

![App via Docker Compose](Screenshots/app-access-dockercompose.png)

## Kubernetes Deployment

![Kubernetes Deployment](Screenshots/k8s-deployment.png)

## Application Access via Kubernetes (NodePort)

![App via Kubernetes](Screenshots/app-access-K8s.png)

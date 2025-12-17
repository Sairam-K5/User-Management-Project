# User Management Application

## Overview  
**User Management Application** is a java springboot application designed to demonstrate a full production-ready microservice lifecycle — from build through containerization, deployment, orchestration, to monitoring.  
With a modern DevOps pipeline, this project showcases my ability to build, deploy, and operate applications using best practices in CI/CD, containerization, orchestration, and observability.

## Project Documentation

### Complete end-to-end documentation with screenshots is available here:

**[View Full Project Documentation](docs/)**

The documentation covers:
- Application development (Java User Management)
- CI/CD automation using Jenkins
- Docker & Kubernetes deployment
- Monitoring with Prometheus & Grafana

### Key Features & Highlights
- CRUD operations for user management (create / read / update / delete users).  
- Built with Java (Spring Boot) — leveraging industry-standard frameworks and conventions.  
- Dockerized: Runs as a container for consistent deployment.  
- Kubernetes orchestration (via Minikube) — enabling scalable, portable deployment.  
- CI/CD pipeline powered by Jenkins (with Jenkinsfile) to automate build → test → release → deploy.  
- Full observability: Integrated with Prometheus for metrics collection and Grafana for dashboards and monitoring.  
- Demonstrates real-world DevOps / SRE practices — important for production readiness.  

## Technology Stack  
| Layer / Concern        | Technology / Tool                   |
|------------------------|------------------------------------|
| Language / Framework    | Java (Spring Boot)                 |
| Build / Packaging       | Maven (or `.mvnw`)                |
| Containerization        | Docker (Dockerfile + docker-compose) |
| Orchestration / Deployment | Kubernetes (Minikube)           |
| CI / CD                 | Jenkins (Jenkinsfile)              |
| Monitoring / Observability | Prometheus + Grafana             |

## Prerequisites  
Make sure you have the following tools installed in your local/dev environment (or CI environment):

- Java 21  
- Maven (or use provided Maven wrapper `.mvnw`)  
- Docker & Docker CLI  
- Kubernetes (Minikube) + kubectl  
- Helm (optional, if using Helm charts)  
- Jenkins (for CI/CD)  
- Prometheus + Grafana (or ability to deploy them on Kubernetes)  

## Setup & Installation  

### Clone the repository  
```bash
git clone https://github.com/Sairam-K5/User-Management-Project.git
cd User-App-Project
```

### Build the application
```bash
./mvnw clean package
```

### Build Docker image
```bash
docker build -t user-app .
```

### Run with Docker
```bash
docker run -d -p 8080:8080 --name user-app-container user-app
```

### Deploy to Kubernetes (Minikube)
```bash
kubectl apply -f kubernetes/backend-deployment.yaml  
kubectl apply -f kubernetes/backend-service.yaml  
```

Then check pods and services:
```bash
kubectl get pods  
kubectl get svc  
```

### Use docker-compose for local multi-container setup
```bash
docker-compose up -d
```

## CI / CD Pipeline (Jenkins)

### The provided Jenkinsfile defines a complete CI/CD workflow:

- Checkout code & run unit (and/or integration) tests.
- Build the application (Maven).
- Build Docker image and tag appropriately.
- Push image to registry (if configured).
- Deploy to Kubernetes (Minikube or configured cluster).

This demonstrates end-to-end automation — from code commit to a running container in a cluster.


## Monitoring & Observability

### This project includes monitoring setup leveraging Prometheus & Grafana:

- Metrics exposed by the Java application via suitable instrumentation (e.g. HTTP request metrics, JVM metrics, custom application metrics).
- Prometheus scrapes metrics, and Grafana provides dashboards to visualise metrics — enabling visibility into performance, resource usage, health, and more.
- This practice reflects modern SRE/DevOps observability standards, demonstrating readiness for real-world production environments.

## Project Structure
```bash
User-Management-Project/
├── src/                 # Java source code  
├── pom.xml              # Maven/Gradle config
├── Dockerfile           # Docker Build file
├── docker-compose.yaml  # (if multi-container local setup)  
├── kubernetes/          # K8s manifests (deployment, service, etc.)  
├── Jenkinsfile          # CI/CD pipeline definition  
├── prometheus/          # (if you have config)  
├── README.md            # About the Project  
```

## What This Project Demonstrates About Me

- Shows full-cycle development: from code → build → container → deploy → monitor.
- Demonstrates hands-on experience with modern DevOps tools and practices (Docker, Kubernetes, Jenkins, monitoring).
- Reflects ability to build Java applications that are ready for scalable deployment — suitable for microservices / cloud-native environments.
- Highlights observability awareness (monitoring + dashboards), a key trait for reliability, maintenance and operational readiness.

Feel free to check out the code, spin it up locally or on a cluster — and explore how it’s built, deployed and monitored end-to-end.

### Final Impression

Screenshots in docs./ collectively prove the project is:
- Fully Deployed
- Fully Monitored
- Scalable
- Professional & Industry-Grade

**Real-World Skills**

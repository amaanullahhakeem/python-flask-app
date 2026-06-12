# DevOps End-to-End Project 🚀

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/804d28df-090a-4fc0-88b6-af70786c52c2" />

## Overview

This project demonstrates an end-to-end DevOps workflow using modern DevOps tools and practices.

The application is containerized using Docker, deployed on Kubernetes, and integrated with CI/CD pipelines using GitHub Actions.

## Project Architecture

```text
Developer
   |
   v
GitHub Repository
   |
   v
GitHub Actions
   |
   v
Docker Build
   |
   v
Docker Hub
   |
   v
Kubernetes Cluster
   |
   v
Flask Application
```

## Technologies Used

- Linux
- Git & GitHub
- Docker
- Docker Hub
- Kubernetes
- GitHub Actions
- Python Flask

## Project Structure

```text
devops-project/

├── app.py
├── requirements.txt
├── Dockerfile
├── .github/
│   └── workflows/
│       └── deploy.yml
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── namespace.yaml
└── README.md
```

## Application

A simple Flask application that displays:

```text
Hello from DevOps Project
```

## Getting Started

### Clone Repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git

cd <repository-name>
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Application

```bash
python app.py
```

Open:

```text
http://localhost:5000
```

## Docker

### Build Docker Image

```bash
docker build -t flask-devops .
```

### Run Container

```bash
docker run -d -p 5000:5000 flask-devops
```

### Verify Running Containers

```bash
docker ps
```

## Docker Hub

### Login

```bash
docker login
```

### Tag Image

```bash
docker tag flask-devops <dockerhub-username>/flask-devops:v1
```

### Push Image

```bash
docker push <dockerhub-username>/flask-devops:v1
```

## Kubernetes Deployment

### Create Namespace

```bash
kubectl apply -f k8s/namespace.yaml
```

### Deploy Application

```bash
kubectl apply -f k8s/deployment.yaml
```

### Create Service

```bash
kubectl apply -f k8s/service.yaml
```

### Verify Resources

```bash
kubectl get pods -n devops

kubectl get svc -n devops
```

## Scaling Application

```bash
kubectl scale deployment flask-app --replicas=5 -n devops
```

## Rolling Updates

```bash
kubectl set image deployment/flask-app \
flask-app=<dockerhub-username>/flask-devops:v2 \
-n devops
```

## CI/CD Pipeline

The project uses GitHub Actions to:

- Trigger on code push
- Build Docker image
- Push image to Docker Hub
- Prepare application for deployment

## Learning Outcomes

Through this project, I practiced:

- Version Control with Git
- Containerization using Docker
- Container Orchestration using Kubernetes
- CI/CD Automation using GitHub Actions
- Deployment Strategies
- Infrastructure Management Concepts

## Future Enhancements

- Add Prometheus Monitoring
- Add Grafana Dashboards
- Deploy on AWS EKS
- Implement Terraform Infrastructure as Code
- Add Ingress Controller
- Configure HTTPS with TLS

## Author

**Aman Ullah**

DevOps Engineer | Learning Cloud, Kubernetes, CI/CD & Automation

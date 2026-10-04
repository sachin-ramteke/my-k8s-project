# Automated Kubernetes CI/CD Pipeline (GitHub Actions & KinD)

A lightweight, zero-cost continuous integration and continuous deployment (CI/CD) pipeline built using GitHub Actions and KinD (Kubernetes in Docker).

## Project Architecture & Workflow
1. **Source Code**: Custom lightweight web service (`index.html` + `Dockerfile`).
2. **Build Stage**: GitHub Actions runner builds the custom Docker container image (`my-custom-app:v1`).
3. **Cluster Provisioning**: Automated spinning up of an ephemeral multi-resource KinD cluster on Ubuntu runner.
4. **Image Loading**: Sideloading the locally built image directly into the KinD node cache.
5. **Orchestration & Verification**: Deploying via Kubernetes declarative CLI, tracking rollout status, and validating active pod runtime states (`kubectl get pods -o wide`).

## Technologies Used
* **Containerization**: Docker
* **Orchestration**: Kubernetes, KinD
* **CI/CD Automation**: GitHub Actions
* **Base OS**: Alpine Linux
* 

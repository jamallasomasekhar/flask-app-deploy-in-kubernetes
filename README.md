# flask-app-deploy-in-kubernetes
Introduction
This document outlines the tasks completed as part of the DevOps internship assignment. The tasks are divided into two parts: Part 1 and Part 2. Each part contains specific tasks that were implemented, tested, and verified using Kubernetes, Docker, and Helm charts.
Architecture
![image](https://github.com/user-attachments/assets/5b7d856d-740e-40b7-99ad-a52be10e8a3c)

# Part 1 - Tasks
Task 1: Setup Flask Application with MongoDB in Docker
Objective: Set up a Flask application connected to a MongoDB database using Docker.
Steps:
Create a Flask Application:
![image](https://github.com/user-attachments/assets/b87918c4-463e-4ef5-9bec-09cfe090f449)

Developed a simple Flask application with a /data endpoint to handle POST and GET requests.
Integrated the Flask application with MongoDB to store and retrieve data.
Dockerize the Application:
Created a Dockerfile for the Flask application.
![image](https://github.com/user-attachments/assets/858f0452-b1d1-4e74-a0d3-a6901529526c)

Built, tested and push the Docker image to docker hub.
Set up a MongoDB instance using Docker.
Run and Test the Application:
Used Docker  to run both the Flask app and MongoDB in separate containers.
![image](https://github.com/user-attachments/assets/1006b3a0-73fc-4eee-b5d0-f040d200436e)

Verified the application functionality by sending HTTP requests to the Flask endpoint.

![image](https://github.com/user-attachments/assets/6af428cf-6b7c-4a22-b5b7-fd134879a008)



# Task 2: Implement Kubernetes Deployment
Objective: Deploy the Dockerized Flask application and MongoDB on a Kubernetes cluster.
Steps:
Create Kubernetes Manifests:
Developed YAML files for Flask and MongoDB deployments.
# Installing Minikube

![image](https://github.com/user-attachments/assets/56df378e-8f39-46b1-8954-fd552f2093c0)


Configured Kubernetes services to expose the Flask application externally and MongoDB internally.
Deploy to Kubernetes:
Used kubectl to apply the deployment and service manifests.
Ensured the Pods were running successfully and tested application connectivity.
Network Configuration:
Configured Kubernetes networking to allow communication between Flask and MongoDB Pods.
Part 2 - Helm Charts
Task 3: Deploy Using Helm Charts
Objective: Simplify the deployment process using Helm charts for the Flask and MongoDB application.
Steps:
Create Helm Chart for Flask Application:
Defined a Helm chart structure with values.yaml for configurable parameters.
Developed templates for deployment and service resources.

Flask-app deployment.yml

Create Helm Chart for MongoDB:
Configured MongoDB deployment and service using Helm.
Used Helm values for setting environment variables such as MongoDB credentials.

Deploy Helm Charts:
Installed and managed the Helm charts on the Kubernetes cluster.

![image](https://github.com/user-attachments/assets/7ba557df-0fda-4d6c-adaf-b5b0884ee8c4)

ALL pods ,service 

![image](https://github.com/user-attachments/assets/8267a756-42c5-4268-8969-a1c41bb6e59b)

Verified deployments and ensured the application was functioning as expected.
Results:
Tested HPA & port-forward
Task 3: Implement Kubernetes Autoscaling and Resource Management
Objective: Optimize resource usage and ensure high availability of the application.
Actions:
Configured Horizontal Pod Autoscaler (HPA) for the Flask application to manage CPU utilization.
Set resource requests and limits for both Flask and MongoDB to prevent resource starvation.

![image](https://github.com/user-attachments/assets/85fe9761-ff44-46bf-89f8-1a9052455e63)

Insert data 

![image](https://github.com/user-attachments/assets/85bde0df-c306-4cc4-a5b4-0d68eaf92ae3)

Get data

![image](https://github.com/user-attachments/assets/bd9de048-bb92-4511-bec5-de93e37e73d0)

Additional Resources
GitHub Repository: [Link to your GitHub repository with the code and configurations](https://github.com/jamallasomasekhar/flask-app-deploy-in-kubernetes.git)
Video Tutorial: [Link to a helpful video tutorial on Helm and Kubernetes](https://drive.google.com/file/d/18sRHO8p2d9TKY3n2VB1P6VqAnRiIvI4F/view?usp=sharing)


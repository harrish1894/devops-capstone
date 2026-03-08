# devops-capstone
DevOps CI/CD Pipeline for Node.js Application

# Project Overview #

This project demonstrates the implementation of an end-to-end DevOps CI/CD pipeline for deploying a Node.js web application. The pipeline automates the process of building, containerizing, and deploying the application using modern DevOps tools.

The application source code is stored in GitHub, and whenever a developer pushes new code, Jenkins automatically triggers the CI/CD pipeline. Jenkins builds the application, creates a Docker image, pushes the image to Docker Hub, and deploys it to an AWS EC2 instance.

Monitoring tools such as Prometheus and Grafana are used to track system and container performance. Additionally, cron jobs and shell scripts are implemented for automating tasks like log backups and maintenance.

This project demonstrates how DevOps practices help in achieving continuous integration, continuous deployment, automation, and monitoring in modern cloud-based applications.


---

# Architecture #

Developer
   │
   ▼
GitHub Repository
   │
   ▼
Jenkins CI/CD Pipeline
   │
   ├── Build Application
   ├── Build Docker Image
   └── Push Image to Docker Hub
   │
   ▼
Docker Hub
   │
   ▼
AWS EC2 Instance
   │
   ▼
Docker Container (Node.js App)
   │
   ▼
Monitoring System
(Prometheus + Grafana)


---

# Tech Stack #

Category	Tools

Version Control	Git, GitHub
CI/CD	Jenkins
Containerization	Docker
Container Registry	Docker Hub
Cloud Infrastructure	AWS EC2
Monitoring	Prometheus, Grafana
Automation	Bash Scripts, Cron Jobs
Application	Node.js



---

# Project Structure #

devops-capstone-project
│
├── app.js
├── package.json
├── Dockerfile
├── Jenkinsfile
├── backup.sh
└── README.md


---

# Setup Instructions (Run Locally) #

1 Install Node.js

Install Node.js and npm.

Check installation:

node -v
npm -v


---

2 Clone Repository

git clone https://github.com/yourusername/devops-capstone-project.git
cd devops-capstone-project


---

3 Install Dependencies

npm install


---

4 Run Application

node app.js

Open browser:

http://localhost:3000


---

Docker Setup

Build Docker Image

docker build -t devops-node-app .

Run Docker Container

docker run -p 3000:3000 devops-node-app

Access application:

http://localhost:3000


---

 # CI/CD Pipeline (Jenkins) #

The Jenkins pipeline automates the following stages:

# Stage 1 # – Clone Repository

Jenkins pulls the latest code from GitHub.

# Stage 2 – Build Application

Dependencies are installed and the application is prepared for deployment.

# Stage 3 – Build Docker Image

A Docker image is created using the Dockerfile.

# Stage 4 – Push Image to Docker Hub

The Docker image is pushed to Docker Hub for storage and distribution.

# Stage 5 – Deploy to AWS EC2

The EC2 server pulls the Docker image and runs the container.


---

# Monitoring

Monitoring is implemented using Prometheus and Grafana.

# Prometheus

Prometheus collects system metrics such as:

CPU usage

Memory usage

System load

Container performance


# Grafana

Grafana provides dashboards to visualize the metrics collected by Prometheus.


---

# Deployment

The application is deployed on an AWS EC2 instance using Docker containers.

# Application access:

http://<52.66.139.197>:3000


---

# Automation

A cron job is configured to automate system maintenance tasks such as:

Log backups

Data cleanup

Scheduled scripts


Example cron job:

0 0 * * * /home/ubuntu/backup.sh

This runs the backup script every day at midnight.


---

Key Learnings

Through this project, the following DevOps concepts were implemented:

Continuous Integration and Continuous Deployment (CI/CD)

Containerization using Docker

Cloud deployment using AWS EC2

Infrastructure monitoring using Prometheus and Grafana

Automation using shell scripting and cron jobs



---

# Repository

# GitHub Repository:

https://github.com/harrish1894/devops-capstone

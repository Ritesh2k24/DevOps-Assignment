# DevOps-Assessment_


📌 Project Objective:

Deploy a sample PHP Yii2 application using Docker Swarm and NGINX (host-based reverse proxy) on an AWS EC2 instance. Automate setup using Ansible and implement CI/CD via GitHub Actions.

🛠️ Key Components Used

-Application: Yii2 Basic App

-Web Server: NGINX (host-level, reverse proxy)

-Container Orchestration: Docker Swarm

-CI/CD Pipeline: GitHub Actions

-Configuration Management: Ansible

-Cloud Environment: AWS EC2 (Ubuntu)

-Version Control: GitHub

🚀 Deployment Breakdown

1. Yii2 Application Setup
   
-Cloned yii2-app-basic from GitHub.

-Moved source to own GitHub repo for CI/CD pipeline integration.

-Fixed merge conflicts from original Yii2 repo.

2. Dockerization
   
-Created Dockerfile to containerize the Yii2 app.

-Built image and published to DockerHub using GitHub Actions.

3. NGINX Reverse Proxy
   
-Configured /etc/nginx/sites-available/yii2.conf to proxy requests from port 80 to the Yii2 app running on port 8080.

-Symbolic link created in sites-enabled.

4. Docker Swarm
   
-Docker Swarm initialized on EC2.

-Application deployed via docker stack deploy.

5. Ansible Automation
   
-Wrote Ansible playbooks to:

-Install Docker, NGINX, Git

-Configure Swarm and NGINX

-Deploy Yii2 as a Swarm service

6. GitHub Actions (CI/CD)
   
-Pipeline steps:

-Checkout code

-Build Docker image

-Push to Docker Hub

-automatic SSH to EC2 using private key from GitHub Secrets

-Pull latest image and deploy using docker stack deploy

![image](https://github.com/user-attachments/assets/1ffabb2a-b1fe-4419-b5e0-33bc686afdb6)

![image](https://github.com/user-attachments/assets/8615f052-58cc-41e0-8a87-8b283f1ab9cb)


![image](https://github.com/user-attachments/assets/e22f20d5-3e8b-4660-939e-5e888fa7b169)

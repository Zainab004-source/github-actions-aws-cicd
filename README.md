 Containerized Application CI/CD Pipeline

 Project Overview

This project demonstrates an automated CI/CD pipeline for deploying a containerized web application on AWS.

The application is packaged with Docker, stored in Amazon ECR, and deployed to Amazon ECS using AWS Fargate. GitHub Actions automates the build and deployment process whenever changes are pushed to the `main` branch.

Architecture

GitHub → GitHub Actions → Docker → Amazon ECR → Amazon ECS/Fargate

 Technologies Used

 GitHub
 GitHub Actions
 Docker
 Amazon ECR
 Amazon ECS
 AWS Fargate
 AWS IAM OIDC
 Amazon VPC

 CI/CD Workflow

1. Code is pushed to the main branch.
2. GitHub Actions is triggered automatically.
3. AWS credentials are securely configured using IAM OIDC.
4. GitHub Actions builds the Docker image.
5. The Docker image is pushed to Amazon ECR.
6. The ECS task definition is updated with the new image.
7. Amazon ECS deploys the updated application using AWS Fargate.
8. GitHub Actions waits for the ECS service deployment to become stable.

 Application

The application is a simple Nginx-based web page containerized with Docker.

The Dockerfile uses the lightweight `nginx:alpine` image and copies the application HTML file into the Nginx web directory.

 Key AWS Components

 Amazon ECR

Stores the Docker image produced by the CI/CD pipeline.

 Amazon ECS

Runs the containerized application.

 AWS Fargate

Provides serverless container compute without managing EC2 servers.

 IAM OIDC

Allows GitHub Actions to authenticate with AWS without storing long-lived AWS access keys in GitHub.

 Result

The application was successfully deployed to Amazon ECS/Fargate through the GitHub Actions CI/CD pipeline.

The deployment completed successfully and the application was accessible through the running ECS task.

 Skills Demonstrated

 CI/CD pipeline implementation
 Docker containerization
 AWS ECS and Fargate deployment
 Amazon ECR image management
 GitHub Actions automation
 AWS IAM and OIDC authentication
 AWS networking
 Cloud deployment and troubleshooting

  Project Evidence

 GitHub Actions — Successful CI/CD Pipeline

![GitHub Actions Success](screenshots/github-actions-success.png)
 Project Evidence

The following screenshots document the successful deployment and CI/CD pipeline:

 [GitHub Actions — Successful CI/CD Pipeline](screenshots/github-actions-success.png)
 [GitHub Repository](screenshots/giithub-repository.png)
 [Amazon ECR — Docker Image](screenshots/ecr-docker-image.png)
 [Amazon ECS — Successful Deployment](screenshots/ecs-deployment-success.png)
 [Live Application](screenshots/live-application.png)


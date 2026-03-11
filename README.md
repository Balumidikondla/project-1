<img width="1536" height="1024" alt="3tier_image" src="https://github.com/user-attachments/assets/208a2243-b049-4ee8-959f-99bd3e7f65ae" />

## Table of Contents

1. [Project Overview](#project-overview)
2. [Architecture Overview](#architecture-overview)
3. [Pre-Requisites](#pre-requisites)

# Project Overview

## Introduction
In this project, I built a Highly Available 3-Tier Web Application architecture on AWS using VPC, EC2, ALB, RDS, S3, and CloudWatch.
The application servers run in private subnets behind an Application Load Balancer, and Auto Scaling ensures scalability during traffic spikes.
The database uses RDS Multi-AZ for high availability, and CloudWatch monitors the infrastructure with alarms.

## key features
- Secure VPC architecture with public and private subnets

- Application Load Balancer for traffic distribution

- Auto Scaling for automatic scaling

- RDS Multi-AZ for database high availability

- S3 for scalable storage

- CloudWatch for monitoring and alerts

## Architecture Overview

Presentation Tier (Frontend)

- Application Load Balancer deployed in public subnets

- Distributes incoming traffic across multiple EC2 instances

- Ensures high availability and fault tolerance

- Provides a single entry point for users to access the application

Application Tier (Backend)

- Amazon EC2 instances running the web application

- Instances deployed in private subnets for security

- Managed using an Auto Scaling Group to automatically scale based on traffic

- Processes user requests and communicates with the database layer

Data Tier

- Amazon RDS (MySQL) deployed in Multi-AZ configuration

- Provides automatic failover and high availability

- Database is placed in private subnets to prevent direct internet access

- Stores application data securely

Storage Layer

- Amazon S3 used to store static files, application assets, and backups

- Highly durable and scalable object storage

Monitoring Layer

- Amazon CloudWatch used for monitoring system performance

- Collects metrics from EC2, RDS, and Load Balancer

- CloudWatch Alarms send alerts when thresholds are exceeded

# Pre-Requisites
- AWS Account
- Git bash or Mobexterm

# AWS SNS Private Notification System

## 📌 Overview
This project implements a secure notification system using AWS SNS within a private VPC architecture.

It ensures that all communication between EC2 and SNS happens privately using VPC Endpoints (AWS PrivateLink), without using the public internet.

## 🏗️ Architecture
- EC2 instance hosts the application
- SNS topic handles notifications
- VPC provides network isolation
- Interface Endpoint enables private communication

## 🔐 Key Features
- Private communication (no internet exposure)
- Secure patient notification system
- Encrypted data transfer
- Cost optimized (no NAT Gateway)

## 🛠️ Tools & Services
- Amazon VPC
- Amazon EC2
- Amazon SNS
- VPC Endpoint (PrivateLink)
- IAM

## ⚙️ Implementation
1. Created custom VPC with subnets
2. Launched EC2 with IAM role
3. Created SNS topic and subscriptions
4. Configured VPC Endpoint for SNS
5. Tested using AWS CLI

## 💻 Sample Command
```bash
aws sns publish \
--region us-east-1 \
--topic-arn <your-topic-arn> \
--message "Test Notification"

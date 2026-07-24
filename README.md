# Production-Grade Highly Available Web Application on AWS

A production-style web application deployed on AWS following the AWS Well-Architected Framework. The solution is designed to provide high availability, scalability, security, and operational excellence using managed AWS services.

---

# 📖 Overview

This project demonstrates the deployment of a production-grade web application on AWS using a highly available architecture distributed across two Availability Zones.

The infrastructure follows AWS best practices by isolating application and database resources in private subnets while exposing only the Application Load Balancer to the internet.

## Key Features

- Multi-AZ deployment
- Highly available architecture
- Auto Scaling based on demand
- Private EC2 instances
- Multi-AZ Amazon RDS
- Global content delivery with CloudFront
- AWS WAF protection
- Secure administration using Systems Manager Session Manager
- CloudWatch monitoring with SNS notifications

---

# 🏗️ Solution Architecture

![Solution Architecture](architecture/solution-architecture.png)

---

# ☁️ AWS Services

| Service | Purpose |
|---------|---------|
| Amazon VPC | Isolated network environment |
| Public & Private Subnets | Secure network segmentation |
| Internet Gateway | Internet connectivity |
| NAT Gateway | Outbound internet access for private instances |
| Application Load Balancer | Traffic distribution |
| Auto Scaling Group | Automatic scaling |
| Amazon EC2 | Application hosting |
| Amazon RDS Multi-AZ | Highly available database |
| Amazon CloudFront | Global content delivery |
| AWS WAF | Web application protection |
| Amazon Route 53 | DNS routing |
| AWS Systems Manager | Secure instance access |
| Amazon CloudWatch | Monitoring |
| Amazon SNS | Alert notifications |

---

# 🏛️ Architecture Components

## Networking

- Amazon VPC
- Two Availability Zones
- Public and Private Subnets
- Internet Gateway
- NAT Gateways
- Route Tables

## Compute

- Launch Template
- Auto Scaling Group
- Private EC2 Instances
- Application Load Balancer

## Database

- Amazon RDS MySQL (Multi-AZ)

## Security

- Security Groups
- AWS WAF
- Systems Manager Session Manager

## Monitoring

- Amazon CloudWatch
- Amazon SNS

---

# 🔄 Request Flow

1. User sends a request.
2. Amazon Route 53 resolves the domain.
3. Amazon CloudFront receives the request.
4. AWS WAF filters malicious traffic.
5. CloudFront forwards traffic to the Application Load Balancer.
6. The ALB routes traffic to healthy EC2 instances.
7. EC2 communicates with Amazon RDS when required.
8. CloudWatch monitors resources and triggers SNS notifications when alarms are activated.

---

# 🔒 Security

The solution follows AWS security best practices.

- Private EC2 instances without public IP addresses
- Private Amazon RDS deployment
- Security Groups controlling inbound and outbound traffic
- AWS WAF protection against common web attacks
- Secure administration using AWS Systems Manager Session Manager
- NAT Gateways for secure outbound internet access

---

# 📈 High Availability & Scalability

The application is designed to remain available even during infrastructure failures.

- Multi-AZ deployment
- Application Load Balancer
- Auto Scaling Group
- Amazon RDS Multi-AZ
- CloudFront global edge locations
- NAT Gateway per Availability Zone

---

# 📷 Deployment Screenshots

## Solution Architecture

![Solution Architecture](architecture/solution-architecture.png)

## Amazon VPC

![VPC](screenshots/network/vpc.png)

## Application Load Balancer

![ALB](screenshots/compute/alb-overview.png)

## Auto Scaling Group

![ASG](screenshots/compute/autoscaling-group.png)

## Amazon RDS

![RDS](screenshots/database/RDS.png)

## Amazon CloudFront

![CloudFront](screenshots/application/cloudfront-distribution.png)

## AWS WAF

![WAF](screenshots/security/aws-waf.png)

## Amazon CloudWatch

![CloudWatch](screenshots/monitoring/cloudwatch.png)

---

# 📚 Learning Outcomes

Through this project I gained hands-on experience with:

- Designing Multi-AZ AWS architectures
- Building secure VPC networking
- Configuring Auto Scaling Groups
- Deploying private EC2 instances
- Configuring Application Load Balancers
- Securing applications with AWS WAF
- Deploying Multi-AZ Amazon RDS
- Implementing CloudFront for content delivery
- Monitoring infrastructure with CloudWatch
- Sending notifications using Amazon SNS
- Managing instances with Systems Manager Session Manager

---

# 👨‍💻 Author

**Mohamed Ahmed Elbaioumy**

- GitHub: https://github.com/Elbaioumy
- LinkedIn: https://www.linkedin.com/in/mohamed-elbaioumy/


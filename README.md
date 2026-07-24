# AWS Highly Available Web Application

A production-style AWS architecture demonstrating **High Availability**, **Scalability**, **Security**, and **Monitoring** using AWS managed services.

---

## 📖 Project Overview

This project demonstrates how to deploy a highly available web application on AWS following cloud architecture best practices.

The infrastructure is distributed across **two Availability Zones** to improve availability and fault tolerance.

The solution includes:

- Multi-AZ VPC Design
- Public and Private Subnets
- Internet Gateway
- NAT Gateways
- Application Load Balancer
- Auto Scaling Group
- Amazon EC2
- Amazon RDS Multi-AZ
- Amazon CloudFront
- AWS WAF
- Amazon Route 53
- Amazon CloudWatch
- Amazon SNS
- AWS Systems Manager Session Manager

---

## 🏗️ Solution Architecture

![Solution Architecture](architecture/solution-architecture.png)

---

# ☁️ AWS Services Used

| Service | Purpose |
|----------|----------|
| Amazon VPC | Creates an isolated virtual network for the application. |
| Public Subnets | Host internet-facing resources such as the Application Load Balancer and NAT Gateways. |
| Private Application Subnets | Host the EC2 application servers securely without public IP addresses. |
| Private Database Subnets | Host the Amazon RDS database instances. |
| Internet Gateway | Provides internet connectivity for public resources. |
| NAT Gateway | Allows private EC2 instances to access the internet securely. |
| Amazon EC2 | Runs the Apache web application. |
| Application Load Balancer | Distributes incoming traffic across multiple EC2 instances. |
| Auto Scaling Group | Automatically scales EC2 instances based on demand. |
| Amazon RDS (Multi-AZ) | Provides a highly available managed MySQL database. |
| Amazon CloudFront | Delivers content globally with low latency. |
| AWS WAF | Protects the application from common web attacks. |
| Amazon Route 53 | Provides DNS management and routing. |
| Amazon CloudWatch | Collects metrics and monitors AWS resources. |
| Amazon SNS | Sends email notifications when alarms are triggered. |
| AWS Systems Manager | Provides secure instance management without SSH. |

---

# 🏛️ Architecture Overview

The solution is designed following AWS Well-Architected Framework best practices.

The application is deployed across two Availability Zones to provide high availability and fault tolerance.

The Application Load Balancer distributes incoming traffic across EC2 instances running inside private application subnets.

Amazon RDS is deployed in Multi-AZ mode to ensure database availability.

CloudFront accelerates content delivery while AWS WAF protects the application from malicious requests.

CloudWatch monitors infrastructure metrics and sends alerts through Amazon SNS.

AWS Systems Manager Session Manager provides secure access to EC2 instances without opening SSH ports.

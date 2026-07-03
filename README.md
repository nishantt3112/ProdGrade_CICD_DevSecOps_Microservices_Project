# Production Grade Cloud Native Microservices Platform

## Project Introduction

This project demonstrates how to build a production-grade cloud native microservices platform on AWS using Kubernetes, Terraform, GitOps, DevSecOps, and modern CI/CD practices.

The application used in this project is Google's Online Boutique, which consists of multiple independently deployable microservices.

## Why Online Boutique?

This project uses **Online Boutique**, Google's official cloud-native microservices demo application, as the reference application to demonstrate modern cloud-native deployment and DevOps practices.

Online Boutique was chosen because it closely resembles a real-world e-commerce platform while remaining lightweight and easy to deploy on Kubernetes. It provides an excellent foundation for implementing production-grade infrastructure, GitOps workflows, security, observability, and progressive delivery strategies.

### Why Online Boutique?

- ✅ Official cloud-native microservices reference application developed by Google Cloud
- ✅ Consists of **11 independently deployable microservices**
- ✅ Built using multiple programming languages (Go, C#, Node.js, Python, Java)
- ✅ Uses **gRPC** for efficient inter-service communication
- ✅ Demonstrates real-world distributed system architecture
- ✅ Runs on any CNCF-compliant Kubernetes cluster, including Amazon EKS
- ✅ Ideal for implementing production-grade DevOps, GitOps, and Kubernetes best practices

This project extends the original Online Boutique application by building a complete production-ready platform around it using Infrastructure as Code, CI/CD, GitOps, security scanning, monitoring, logging, and automated deployments.

# 🏗️ Application Architecture

The Online Boutique application is composed of **11 independently deployable microservices** that communicate primarily using **gRPC**. The `frontend` service acts as the entry point for user requests, while the `checkout` service orchestrates the payment, shipping, and email services during order processing. This polyglot architecture is designed to demonstrate real-world cloud-native application patterns. :contentReference[oaicite:1]{index=1}

![Online Boutique Application Architecture](Application_architecture.png)


# 🎯 Project Goals

The primary objective of this project is to demonstrate how a real-world microservices application can be deployed and managed using production-grade cloud-native technologies and DevOps best practices.

This project focuses on achieving the following goals:

- Deploy a production-grade microservices application on Amazon EKS
- Automate infrastructure provisioning using Terraform
- Implement CI using Jenkins distributed architecture
- Implement GitOps-based deployments using Argo CD
- Enable zero-downtime deployments using Argo Rollouts
- Build a secure CI/CD pipeline with automated quality and security checks
- Perform vulnerability scanning using Trivy and OWASP Dependency Check
- Integrate code quality analysis with SonarQube
- Implement centralized monitoring, logging, and observability
- Support scalable and highly available Kubernetes workloads


# ☁️ Cloud Native Architecture

This project follows Cloud Native principles to build a scalable, resilient, and production-ready platform on Kubernetes.

The cloud-native platform is built around the following core capabilities:

- Containerized application using Docker
- Kubernetes orchestration with Amazon EKS
- Service Discovery for inter-service communication
- Horizontal Auto Scaling
- Infrastructure as Code using Terraform
- GitOps-based continuous deployment using Argo CD
- Progressive delivery with Argo Rollouts
- Centralized Monitoring and Observability
- Immutable Infrastructure and declarative deployments


# Project Architecture

![Architecture](Ecom-App-Architectural-Diagram.png)

# 🔄 End-to-End Request Flow

## 🔄 End-to-End Request Flow

```text
                           User Traffic
                                │
                                ▼
               AWS Application Load Balancer (ALB)
                                │
                                ▼
                     Gateway API (Gateway)
                                │
                                ▼
                          HTTPRoute
                                │
                                ▼
                     Argo Rollouts
                                │
                  ┌─────────────┴─────────────┐
                  │                           │
                  ▼                           ▼
      Stable Target Group (90%)    Canary Target Group (10%)
                  │                           │
                  ▼                           ▼
      Frontend Stable Service     Frontend Canary Service
                  │                           │
                  ▼                           ▼
          Stable ReplicaSet         Canary ReplicaSet
                  │                           │
                  ▼                           ▼
             Stable Pods               Canary Pods
```


# 🚀 Production-Grade Features

This project demonstrates the implementation of a production-ready cloud native platform using modern DevOps and GitOps practices.

## Infrastructure

- Amazon EKS
- Terraform
- AWS Load Balancer Controller
- IAM Roles for Service Accounts (IRSA)

## CI/CD & GitOps

- GitHub Actions
- Argo CD
- Argo Rollouts
- Helm
- Kustomize

## Security

- Trivy
- SonarQube
- OWASP Dependency Check

## Observability

- Prometheus
- Grafana
- ECK Operator
- ECK-FileBeat
- ECK-ElasticSearch
- ECK-Kibana


The application consists of **11 independently deployable microservices** that communicate primarily using **gRPC**. Each service is responsible for a specific business capability, making the application modular, scalable, and fault tolerant.

### Core Microservices

- Frontend
- Product Catalog
- Cart
- Checkout
- Currency
- Payment
- Shipping
- Email
- Recommendation
- Ad Service
- Load Generator


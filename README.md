# 3-Tier-Architecture-on-AWS-Using-Terraform

In this project, we will design and implement a scalable three-tier architecture on AWS using Terraform. The setup follows a modular approach, organizing infrastructure into separate layers: Core, Web, App, and Database. This ensures better manageability, reusability, and security while deploying cloud resources. By the end, you will have a fully automated, infrastructure-as-code (IaC) solution for hosting applications on AWS.
https://cdn-images-1.medium.com/max/1000/1*gO8Gax7gHLWTVkouFdkMbw.png
# Prerequisites
Before starting this project, ensure you have the following:
✅ AWS Account - To provision cloud resources using Terraform.
✅ Terraform Installed - Download and install Terraform on your local machine.
✅ AWS CLI Installed & Configured - Install AWS CLI and run aws configure to set up credentials.
✅ IAM User with Required Permissions – Ensure your IAM user has permissions to create and manage VPCs, EC2, RDS, ALB, and other AWS resources.
✅ Basic Knowledge of Terraform – Familiarity with writing .tf files, providers, modules, and variables.
✅ Code Editor (VS Code Recommended) – Use VS Code with the Terraform extension for syntax highlighting and better development experience.
✅ Git Installed (Optional) – For version control and managing Terraform code in a GitHub repository.
# Architecture Overview
We will deploy a three-tier architecture consisting of the following:
VPC (Core Layer): Contains public and private subnets.
Public Subnets: Bastion Host & NAT Gateway.
Private Subnets: Web/Application servers (EC2 instances) and Database (Amazon RDS).
Load Balancer: ALB to distribute traffic.
Security Groups: Restricted access at different layers

# Deployment Steps

1️⃣ Initialize Terraform

terraform init

2️⃣ Plan the Deployment

terraform plan

3️⃣ Apply the Configuration

terraform apply -auto-approve

4️⃣ Verify the Deployment

Check AWS Console for created resources.

Validate EC2 instances, ALB, and RDS.

5️⃣ Destroy Infrastructure (Optional)

terraform destroy -auto-approve

# Conclusion

This Terraform-driven 3-tier AWS deployment establishes a scalable, secure, and highly available architecture, leveraging infrastructure-as-code (IaC) best practices. By modularizing components (web, app, database) and isolating network layers, it ensures fault tolerance, simplified maintenance, and controlled access between tiers. The use of auto-scaling groups, ALBs, and RDS guarantees resilience and performance, while security groups enforce least-privilege principles. This foundation supports seamless scaling, cost optimization, and compliance readiness, providing a robust blueprint for modern cloud-native applications. Future enhancements like HTTPS, WAF, or secrets management can further strengthen production readiness.

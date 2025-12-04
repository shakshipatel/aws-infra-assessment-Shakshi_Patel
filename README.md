# AWS Infra Assessment — Shakshi_Patel

This repository contains Terraform code, setup scripts, screenshots, and documentation for the AWS assessment tasks completed by Shakshi Patel.

Tasks:

1. Networking & Subnetting (VPC, Public & Private subnets, IGW, NAT)
2. EC2 Static Website Hosting (Nginx)
3. High Availability + Auto Scaling (ALB, TargetGroup, ASG)
4. Billing & Free Tier Cost Monitoring (CloudWatch Billing Alarm, Free Tier alert)
5. Architecture Diagram (draw.io)

**Prefix used for all resources:** Shakshi*Patel*

## How to review

- Open each folder `01-vpc-subnets` … `05-architecture-diagram`.
- Each folder contains:
  - Terraform code or setup script
  - README with approach and instructions
  - required screenshots for submission
  - terraform.tfvars.example you must fill if you want to re-run

## How to destroy resources

Run `terraform destroy` in each folder (order recommended):

1. `03-ha-autoscaling-alb`
2. `02-ec2-static-site`
3. `01-vpc-subnets`
4. `04-billing-alerts`

## Notes

- Replace any placeholders like `vpc-...` or `subnet-...` when you re-run Terraform.
- Make sure to destroy resources after use to avoid charges.

## **Brief Explanation**

The architecture is designed for a highly scalable web application able to support 10,000 concurrent users. Traffic flows from users through an optional CloudFront CDN and into an Internet-facing ALB deployed across multiple AZs. The ALB spreads load across a private Auto Scaling Group of EC2 instances running the application. ElastiCache (Redis) handles caching to reduce latency, while RDS/Aurora provides a scalable, fault-tolerant database. Public subnets host ALB and NAT Gateways, while private subnets host compute and data services. Security layers include Security Groups, NACLs, IAM roles, and an optional AWS WAF. Monitoring is handled using CloudWatch, VPC Flow Logs, and CloudTrail.

---

## **Required Files**

Placed in folder: `05-architecture-diagram/`

## 📘 Overview & Approach

To enhance reliability and scalability, I migrated the web server to a **private Auto Scaling Group (ASG)** and exposed it through an **internet-facing Application Load Balancer (ALB)**.  
ALB distributes traffic across multiple Availability Zones to ensure high availability, while the ASG automatically adjusts instance count based on demand.  
Instances run Nginx via user-data and remain private—only the ALB can communicate with them.  
NAT Gateway from Task 1 provides outbound access for package installation.

This architecture follows AWS HA, multi-AZ, and security best practices.

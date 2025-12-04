## **Brief Explanation of Architecture & Traffic Flow**

To achieve high availability, I deployed an Internet-facing Application Load Balancer across two public subnets and configured it to forward traffic to a Target Group. I migrated the web server setup into private subnets and deployed an Auto Scaling Group that launches EC2 instances across two Availability Zones. The ASG ensures automatic scaling, health checks, and fault tolerance. All public traffic now flows through the ALB → Target Group → Private EC2 instances. NAT Gateway provides outbound internet for package installation inside private subnets.

---

## **Required Screenshots**

Placed in folder: `03-ha-autoscaling-alb/`

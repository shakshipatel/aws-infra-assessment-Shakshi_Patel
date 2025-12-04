## **Brief Explanation**

I created a dedicated VPC with CIDR `10.10.0.0/16` to provide isolated networking for all tasks. I designed two public subnets for internet-facing resources (ALB, NAT Gateway) and two private subnets for backend resources such as EC2 and future databases. An Internet Gateway (IGW) was attached to the VPC to enable outbound/inbound public access. A NAT Gateway was provisioned in a public subnet to allow private instances to securely access the internet without being publicly exposed. Route tables were configured to correctly associate subnets with IGW and NAT for proper traffic flow.

---

## **CIDR Ranges Used**

| Resource         | CIDR           | Reason                                |
| ---------------- | -------------- | ------------------------------------- |
| VPC              | 10.10.0.0/16   | Allows future scaling, large IP space |
| Public Subnet A  | 10.10.1.0/24   | Public resources in AZ-A              |
| Public Subnet B  | 10.10.2.0/24   | Public resources in AZ-B              |
| Private Subnet A | 10.10.101.0/24 | App tier in AZ-A                      |
| Private Subnet B | 10.10.102.0/24 | App tier in AZ-B                      |

---

## **Required Screenshots**

Placed in folder: `01-vpc-subnets/`



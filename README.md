# multi-az-vpc-implementation
This project demonstrates the creation of a highly available Virtual Private Cloud (VPC) across multiple Availability Zones in AWS. The design was implemented as part of my AWS Solutions Architect Associate learning path using Adrian Cantrill’s course.

---

## 📖 Project Overview
The goal of this project is to design and deploy a production-ready VPC that supports:
- Public and private subnets across **3 Availability Zones (AZs)**
- **Internet Gateway** for public subnet internet access
- **Bastion Host** for secure admin access

---

## 🏗️ Architecture
![VPC Architecture](/vpcdesign.jpeg)

### CIDR Allocation
- **VPC CIDR:** `10.16.0.0/16`
- Subnets divided across 3 AZs (A, B, C)
- Each AZ contains:
  - Database Subnet
  - Application Subnet
  - Web Subnet (with NAT Gateway)
  - Reserved Tier (for future scaling)

---

## ⚙️ Implementation Steps
Detailed steps can be found in [`implementation_steps.md`](implementation_steps.md).  
Key steps include:
1. Create VPC and assign CIDR block.
2. Create public and private subnets in 3 AZs.
3. Attach an **Internet Gateway**.
4. Configure **NAT Gateways** in each AZ.
5. Create and associate **Route Tables**.
6. Deploy a **Bastion Host** for secure SSH access.
7. Test connectivity across subnets and internet.

---

## 📸 Screenshots
Some highlights from my implementation:

| Description       | Screenshot |
|-------------------|------------|
| VPC Architecture  | ![VPC](screenshots/vpc-design.png) |
| Subnets in AZs    | ![Subnets](screenshots/subnets.png) |
| NAT Gateway Setup | ![NAT](screenshots/nat-gateway.png) |
| Route Tables      | ![Routes](screenshots/route-tables.png) |

---

## 🚀 Skills Demonstrated
- AWS VPC Design
- Subnetting & CIDR Planning
- High Availability Architecture
- Secure Network Access (NAT, Bastion Host)
- Internet Gateway & Route Tables

---

## 🔗 References
- [Adrian Cantrill AWS Solutions Architect Course](https://learn.cantrill.io)
- [AWS VPC Documentation](https://docs.aws.amazon.com/vpc/)

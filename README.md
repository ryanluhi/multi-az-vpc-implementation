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
  - Reserved Tier 

---

## ⚙️ Implementation Steps
Detailed steps can be found in [`implementation_steps.md`](implementation_steps.md).  
Key steps include:
1. Create VPC and assign CIDR block.
![Subnets](/vpc2.jpeg)
2. Create public and private subnets in 3 AZs.
![Subnets](/vpc4.jpeg)
![enable auto assign ip](/vpc9.jpeg) 
4. Attach an **Internet Gateway**.
![igw](/vpc5.jpeg) 
5. Create and associate **Route Tables**.
![Route Table](/vpc6.jpeg)

-associate the public subnet with the route table
![Associate rt](/vpc7.jpeg) 

-edit route 
![edit route](/vpc8.jpeg) 
8. Deploy a **Bastion Host**.
![public subnet](/vpc10.jpeg) 

---

## 🚀 Skills Demonstrated
- AWS VPC Design
- Subnetting & CIDR Planning
- High Availability Architecture
- Secure Network Access 
- Internet Gateway & Route Tables

---

## 🔗 References
- [Adrian Cantrill AWS Solutions Architect Course](https://learn.cantrill.io)
- [AWS VPC Documentation](https://docs.aws.amazon.com/vpc/)

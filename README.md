# AWS Project: VPC, EC2, RDS and Internet Gateway  
**Cloud Bootcamp Hands-on Project**

This project demonstrates a complete AWS infrastructure setup using **Amazon VPC, EC2, RDS (MySQL), Internet Gateway, NAT Gateway, Route Tables, and Security Groups**.  
The goal was to deploy a secure, scalable web application architecture following AWS best practices.

---

## 🧱 Architecture Overview

- Custom VPC with public and private subnets
- Internet Gateway for public access
- NAT Gateway for private subnet outbound access
- EC2 instance hosting a web application
- Amazon RDS (MySQL) in private subnet
- Secure networking using route tables and security groups

---

## 🛠️ Services Used

- Amazon VPC
- Amazon EC2
- Amazon RDS (MySQL)
- Internet Gateway
- NAT Gateway
- Route Tables
- Security Groups
- AWS CloudShell

---

## 📌 Step-by-Step Implementation

### 1️⃣ Create VPC
Created a custom VPC with CIDR block `10.0.0.0/16`.

![VPC Create](screenshots/01-vpc-create.png)

---

### 2️⃣ Enable DNS Resolution & Hostnames
Enabled DNS resolution and DNS hostnames to support public resources.

![Enable DNS Hostname](screenshots/02-vpc-enable-dns-hostname.png)

---

### 3️⃣ Create Subnets
Created four subnets across two Availability Zones.

- Public-1A → `10.0.1.0/24`
- Public-1B → `10.0.2.0/24`
- Private-1A → `10.0.3.0/24`
- Private-1B → `10.0.4.0/24`

![Subnet Creation Page](screenshots/03-subnet-create-page.png)
![Public Subnet 1A](screenshots/04-subnet-public-1a.png)
![Public Subnet 1B](screenshots/05-subnet-public-1b.png)
![Private Subnet 1A](screenshots/06-subnet-private-1a.png)
![Private Subnet 1B](screenshots/07-subnet-private-1b.png)

---

### 4️⃣ Verify Subnets
Confirmed all subnets were created successfully.

![Subnets Overview](screenshots/08-subnets-created-overview.png)

---

### 5️⃣ Create Private Route Table
Created a custom route table for private subnets.

![Private Route Table Create](screenshots/09-route-table-create-private.png)

---

### 6️⃣ Configure Route Table Routes
Added routes for internal traffic and internet access.

![Edit Routes](screenshots/10-route-table-edit-routes.png)

---

### 7️⃣ Route Tables Overview
Verified main and private route tables.

![Route Tables Overview](screenshots/11-route-tables-overview.png)

---

### 8️⃣ Associate Private Subnets
Associated private subnets with the private route table.

![Subnet Association](screenshots/12-route-table-subnet-association.png)

---

### 9️⃣ Create & Attach Internet Gateway
Created an Internet Gateway and attached it to the VPC.

![Attach IGW](screenshots/13-internet-gateway-attach-to-vpc.png)
![Create IGW](screenshots/14-internet-gateway-create.png)

---

### 🔟 Create NAT Gateway
Created NAT Gateway in public subnet for outbound internet access from private subnets.

![NAT Gateway](screenshots/15-nat-gateway-create.png)

---

### 1️⃣1️⃣ Configure Private Route Table for NAT
Updated private route table to route traffic through NAT Gateway.

![Private Route Table Routes](screenshots/16-private-route-table-routes.png)

---

### 1️⃣2️⃣ Create Security Group
Configured inbound and outbound rules for EC2 access.

![Security Group](screenshots/17-security-group-create.png)

---

### 1️⃣3️⃣ Launch EC2 Instance
Launched an EC2 instance using Amazon Linux AMI.

![EC2 AMI Selection](screenshots/18-ec2-launch-ami-selection.png)
![EC2 Network Settings](screenshots/19-ec2-launch-network-settings.png)

---

### 1️⃣4️⃣ Create RDS MySQL Database
Configured RDS MySQL database with free-tier eligible settings.

![RDS Engine Selection](screenshots/20-rds-database-engine-selection.png)
![RDS Credentials](screenshots/21-rds-database-credentials-settings.png)
![RDS Storage & Connectivity](screenshots/22-rds-instance-storage-connectivity.png)

---

### 1️⃣5️⃣ Connect to EC2 via CloudShell
Connected to EC2 securely using SSH.

![SSH Login](screenshots/23-cloudshell-ec2-ssh-login.png)
![System Configuration](screenshots/24-cloudshell-system-configuration.png)

---

### 1️⃣6️⃣ Deploy Application & Database
Downloaded application files and configured MySQL database.

![App Download](screenshots/25-application-files-download.png)
![MySQL Connection](screenshots/26-mysql-connection-to-rds.png)
![Show Databases](screenshots/27-mysql-show-databases.png)
![Create Database](screenshots/28-create-new-database-wikidb.png)
![Insert Dummy Data](screenshots/29-dummy-database-and-data-inserted.png)

---

### 1️⃣7️⃣ Web Application Access
Successfully accessed the deployed web application.

![Web App Login](screenshots/30-web-application-login-page.png)

---

## ✅ Final Outcome

- Secure AWS network architecture implemented
- EC2 connected to RDS using private networking
- Web application successfully deployed and tested
- Followed AWS best practices for security and availability

---

## 🧑‍💻 Author

**MD Naimur Rashid**  
University of Frontier Technology


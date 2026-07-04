# aws-vpc-nat-gateway
This project demonstrates how to configure a secure AWS networking environment using **Amazon VPC**, **Public & Private Subnets**, **Internet Gateway**, and a **NAT Gateway**.

The objective is to allow EC2 instances in a private subnet to access the internet for software updates and package installations while preventing direct inbound internet access.

---

##  Objectives

- Create a custom Amazon VPC
- Configure Public and Private Subnets
- Attach an Internet Gateway (IGW)
- Create and configure a NAT Gateway
- Configure Route Tables
- Launch EC2 instances in both subnets
- Verify secure internet connectivity from the private subnet

---

#  AWS Services Used

- Amazon VPC
- Public Subnet
- Private Subnet
- Internet Gateway
- NAT Gateway
- Elastic IP
- Amazon EC2
- Route Tables
- Security Groups

---

#  Project Implementation

## Step 1 – Create a VPC

Created a custom Virtual Private Cloud to isolate and manage cloud resources.

**Screenshot**

<img width="814" height="42" alt="image" src="https://github.com/user-attachments/assets/2d7b48b5-adae-4b2f-8b4f-3490d5ffaf70" />

---

## Step 2 – Create Public and Private Subnets

Configured one Public Subnet and one Private Subnet within different Availability Zones.

The Public Subnet hosts internet-facing resources, while the Private Subnet securely hosts backend resources.

**Screenshot**

<img width="839" height="210" alt="image" src="https://github.com/user-attachments/assets/80a1d125-0a1f-44fd-8daf-e50609e15ffc" />


---

## Step 3 – Create and Attach an Internet Gateway

Created an Internet Gateway and attached it to the VPC to enable internet connectivity for resources in the Public Subnet.

**Screenshot**

<img width="849" height="247" alt="image" src="https://github.com/user-attachments/assets/808800dd-5dfa-4ca8-a6e5-eec595b167b8" />


---

## Step 4 – Create a NAT Gateway

Allocated an Elastic IP address and created a NAT Gateway inside the Public Subnet.

The NAT Gateway allows instances in the Private Subnet to initiate outbound internet connections securely.

**Screenshot**

<img width="870" height="305" alt="image" src="https://github.com/user-attachments/assets/159bad76-2f27-42d4-94e5-1024ad285544" />


---

## Step 5 – Configure Route Tables

Configured routing rules:

### Public Route Table

- Destination: `0.0.0.0/0`
- Target: Internet Gateway

### Private Route Table

- Destination: `0.0.0.0/0`
- Target: NAT Gateway

**Screenshot**

<img width="799" height="573" alt="image" src="https://github.com/user-attachments/assets/7ceba6f7-dcf2-45b8-932b-01c4de884a6a" />



---

## Step 6 – Launch EC2 Instances

Created two EC2 instances:

- Public EC2 Instance
- Private EC2 Instance

The Public EC2 instance can be accessed from the internet, while the Private EC2 instance remains isolated.

**Screenshot**

<img width="853" height="266" alt="image" src="https://github.com/user-attachments/assets/bbacde91-e6bd-47e5-b37b-08078c8c3fbd" />


---

## Step 7 – Verify Internet Connectivity

Verified that the EC2 instance in the Private Subnet could successfully access the internet through the NAT Gateway without being directly exposed to inbound traffic.

**Screenshot**

<img width="711" height="435" alt="image" src="https://github.com/user-attachments/assets/ebffb38e-4338-4a95-b62d-ae0fdb03daa5" />


---

#  Results

Successfully implemented a secure AWS networking architecture where:

- ✔ Public resources are internet accessible.
- ✔ Private EC2 instances remain protected.
- ✔ Outbound internet access is provided using a NAT Gateway.
- ✔ Route Tables correctly manage network traffic.
- ✔ Secure cloud networking best practices are followed.

---

#  Key Learnings

- Amazon VPC Architecture
- Public vs Private Subnets
- Internet Gateway Configuration
- NAT Gateway Implementation
- Route Tables
- Elastic IP
- EC2 Networking
- Secure Cloud Infrastructure Design

---

#  Project Report

For detailed documentation, refer to the project report.

📄 **[AWS NAT Gateway Project Report]([Task-4 Implement NAT Gateway Setup.pdf](https://github.com/user-attachments/files/29652615/Task-4.Implement.NAT.Gateway.Setup.pdf))**

---

# 👨‍💻 Author

Jerin Abraham Varghese

- LinkedIn: https://www.linkedin.com/in/jerin-abraham-varghese-62a258142
- GitHub: https://github.com/jerinvarghese8022-netizen

---

⭐ If you found this project useful, feel free to star the repository!

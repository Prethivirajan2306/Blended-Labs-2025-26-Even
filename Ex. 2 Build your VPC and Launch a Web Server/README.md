# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Prethivirajan L
* **Register Number**: 212224040251
* **Date of Submission**: 24-02-2026
---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)



1. A Virtual Private Cloud was created with the CIDR block 10.0.0.0/16 to provide an isolated network environment in AWS.

2. A public subnet with the CIDR block 10.0.1.0/24 was created inside the VPC, and auto-assign public IP was enabled so that instances can be accessed from the internet.

3. An Internet Gateway was created and attached to the VPC to allow communication between the VPC and the internet.

4. A route table was created and a default route 0.0.0.0/0 was added pointing to the Internet Gateway, then the route table was associated with the public subnet.

5. A security group was created to act as a firewall, allowing inbound traffic on port 22 for SSH and port 80 for HTTP.

6. An EC2 instance using Amazon Linux 2 and t2.micro instance type was launched in the public subnet with the created security group and key pair.

7. Apache HTTP server was installed and started on the EC2 instance, a simple HTML page was created, and the web server was accessed successfully using the public IP address in a web browser.


## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1920" height="1200" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/7a3423e0-3b28-4022-af31-e7645217db35" />


---

### Screenshot 2: EC2 Instance Running

<img width="1920" height="1200" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/33d6fd23-602f-4b53-be23-c3845b1b7c8f" />



<img width="1255" height="654" alt="image" src="https://github.com/user-attachments/assets/bf9e69b6-e232-41b8-aaad-aa4c1dbefbb1" />



---

### Screenshot 3: Web Server Output in Browser


<img width="1907" height="1135" alt="Screenshot 2026-02-21 124745" src="https://github.com/user-attachments/assets/bc5204b0-a30d-4f1e-908c-bfe3c66cdb8a" />


---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.

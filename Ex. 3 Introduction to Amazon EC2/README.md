# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: PRETHIVIRAJAN L
* **Register Number**: 212224040251
* **Date of Submission**: 27-02-2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

1. Launch Your Amazon EC2 Instance task provisions a Amazon EC2 instance in the N. Virginia region with termination and stop protection enabled, configured inside a Lab VPC with a custom security group, and bootstrapped via user data to automatically deploy an Apache web server on Amazon Linux 2023.
2. Monitor Your Instance task focuses on monitoring your Amazon EC2 instance using status checks, logs, screenshots, and performance metrics through Amazon CloudWatch to ensure reliability and troubleshoot issues proactively.
3. Update Your Security Group and Access the Web Server task updates the security group of your Amazon EC2 instance to allow inbound HTTP (port 80) traffic, enabling external access to the deployed web server via its public IPv4 address.
4. Resize Your Instance task stops your Amazon EC2 instance to upgrade its instance type from t2.micro to t2.small, enables stop protection, and increases the attached Amazon Elastic Block Store volume size from 8 GiB to 10 GiB before restarting it.
5. Explore EC2 Limits task involves reviewing regional resource quotas for Amazon Elastic Compute Cloud through the Service Quotas console to understand default limits on running on-demand instances and other EC2 resources, and how they govern deployment capacity.
6.Test Stop Protection task validates stop protection on your Amazon EC2 instance by attempting to stop it, confirming the safeguard blocks the action, then disabling the protection to successfully stop the instance.

## Output Screenshots (Attach 3)


### Screenshot 1: EC2 Dashboard / Instance List

<img width="1856" height="1090" alt="Screenshot (55)" src="https://github.com/user-attachments/assets/ef77aa79-d46f-4c2c-9b36-6769368c3d54" />


<img width="1860" height="1141" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/540e111b-bbce-42cf-9f3d-620c1142a9a2" />

<img width="1860" height="1141" alt="Screenshot (60)" src="https://github.com/user-attachments/assets/dee18429-385a-4ae8-87ce-41bb48537850" />




---

### Screenshot 2: SSH Connection to Instance

<img width="1858" height="1153" alt="Screenshot (54)" src="https://github.com/user-attachments/assets/2c0c809c-46ea-472d-8458-e2163732c9e8" />


### Screenshot 3: Instance Monitoring / Status

<img width="1853" height="1139" alt="Screenshot (51)" src="https://github.com/user-attachments/assets/8cb88daa-7be7-4709-b41e-92a6c8abeb75" />


<img width="1854" height="1089" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/cf0aaaff-9081-4be6-bcc7-f6f8751738b6" />


<img width="1863" height="1146" alt="Screenshot (53)" src="https://github.com/user-attachments/assets/341a1965-4d16-4e27-8649-7eec488c774e" />



## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.

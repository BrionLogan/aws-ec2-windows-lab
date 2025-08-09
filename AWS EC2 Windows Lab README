# AWS EC2 Windows Instance Lab

## Overview
This lab demonstrates the process of launching, configuring, and connecting to a Windows EC2 instance in AWS.  
The purpose of this exercise was to gain hands-on experience with Amazon EC2, networking, and secure remote access from macOS using Microsoft Remote Desktop.

---

## Prerequisites
- **AWS Account:** You must have an active AWS account to complete this lab. Sign up at [https://aws.amazon.com](https://aws.amazon.com) if you don’t already have one.
- **Local System:** This lab was completed from a Mac running macOS, using the **Microsoft Remote Desktop** application from the Mac App Store.
- **Key Pair:** You will need to create or use an existing `.pem` key pair in AWS to decrypt the Administrator password for your Windows EC2 instance.

---

## Steps Performed

### 1. Launching the EC2 Instance
- **AMI Chosen:** Microsoft Windows Server (Free tier eligible)
- **Instance Type:** t2.micro (free tier eligible)
- **Network Settings:**
  - Used the default VPC and subnet for simplicity.
  - Created a new **security group** allowing only RDP (TCP 3389) access from **my IP address**.
- **Storage:**
  - Kept the default 8 GB gp3 EBS root volume.
  - **Reasoning:** The default size is sufficient for the operating system and basic lab testing while minimizing AWS costs.
- **Key Pair:**
  - Created/downloaded a `.pem` key pair to decrypt the Administrator password later.

---

### 2. Connecting from macOS via RDP
- Downloaded **Microsoft Remote Desktop** from the Mac App Store.
- In AWS EC2 console:
  - Selected the instance → **Connect** → **RDP Client**.
  - Downloaded the `.rdp` file.
  - Retrieved the Administrator password by uploading the `.pem` key file in the console.
- Opened the `.rdp` file in Microsoft Remote Desktop and logged in successfully.

---

### 3. Verifying the Instance
- Opened **PowerShell** and ran:
  ```powershell
  hostname
  systeminfo

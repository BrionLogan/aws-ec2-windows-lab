# 🚀 AWS EC2 Windows Instance Lab

## 📌 Overview
This lab demonstrates launching, configuring, and connecting to a **Windows EC2 instance** in AWS.  
It was completed from **macOS** using the Microsoft Remote Desktop app, showcasing AWS fundamentals, secure remote access, and basic Windows Server operations.

---

## 🛠 Prerequisites
- **AWS Account** – Sign up at [aws.amazon.com](https://aws.amazon.com) if you don’t have one.
- **Mac Computer** – Running macOS with internet access.
- **Microsoft Remote Desktop for Mac** – Download from the [Mac App Store](https://apps.apple.com/app/microsoft-remote-desktop/id1295203466).
- **AWS Key Pair (.pem)** – Required to decrypt the Administrator password for your EC2 instance.

---

## 📂 Steps Performed

### 1️⃣ Launching the EC2 Instance
- **AMI:** Microsoft Windows Server (Free tier eligible)  
- **Instance Type:** `t2.micro` (Free tier eligible)  
- **Network Settings:**
  - Used default **VPC** and **subnet**.
  - Created a **custom security group** allowing **RDP (TCP 3389)** access **only from my IP**.
- **Storage:**
  - Kept the default **8 GB gp3 EBS root volume**.
  - **Reasoning:** Enough for OS + lab activities while minimizing AWS costs.
- **Key Pair:**
  - Generated and downloaded `.pem` key for password decryption.

---

### 2️⃣ Connecting from macOS via RDP
- Downloaded Microsoft Remote Desktop from the Mac App Store.
- In the AWS console:
  - Selected instance → **Connect** → **RDP Client**.
  - Downloaded `.rdp` file.
  - Decrypted Administrator password using `.pem` key.
- Opened `.rdp` file in Microsoft Remote D

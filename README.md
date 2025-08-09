# 🚀 AWS EC2 Windows Instance Lab

## 📌 Overview
This lab demonstrates launching, configuring, and connecting to a **Windows EC2 instance** in AWS.  
It was completed from **macOS** using the Microsoft Remote Desktop app, showcasing AWS fundamentals, secure remote access, and basic Windows Server operations.

---

## 🛠 Prerequisites
- **AWS Account** – Sign up at [aws.amazon.com](https://aws.amazon.com) to provision cloud resources.
- **Mac Computer** – Running macOS with internet access.
- **Microsoft Remote Desktop for Mac** – Download from the [Mac App Store](https://apps.apple.com/app/microsoft-remote-desktop/id1295203466) to connect to the Windows EC2 instance.
- **AWS Key Pair (.pem)** – Required to decrypt the Administrator password for your EC2 instance.

---

## 📂 Steps Performed

### 1️⃣ Launching the EC2 Instance
- **AMI:** *Microsoft Windows Server (Free tier eligible)*  
  *Reasoning:* Windows Server was selected to practice RDP connections and basic server management in a cloud environment.
- **Instance Type:** `t2.micro` (free tier eligible)  
  *Reasoning:* Sufficient CPU and memory for a basic Windows server lab without incurring extra costs.
- **Network Settings:**
  - Used the default **VPC** and **subnet**.  
    *Reasoning:* The default VPC is preconfigured for internet access, which simplifies setup for a beginner lab.
  - Created a **custom security group** allowing only **RDP (TCP 3389)** from **my IP address**.  
    *Reasoning:* Restricting RDP access to a single IP follows the principle of least privilege and improves security.
- **Storage:**
  - Kept the default **8 GB gp3 EBS root volume**.  
    *Reasoning:* 8 GB is enough for the operating system and basic testing while keeping storage costs minimal.
- **Key Pair:**
  - Generated and downloaded a `.pem` key during instance creation.  
    *Reasoning:* This private key is required to decrypt the Windows Administrator password before first connection.

---

### 2️⃣ Connecting from macOS via RDP
- Downloaded Microsoft Remote Desktop from the Mac App Store.  
  *Reasoning:* This free tool from Microsoft is the standard for connecting to Windows systems from macOS.
- In the AWS console:
  - Selected the instance → **Connect** → **RDP Client**.
  - Downloaded the `.rdp` file.  
    *Reasoning:* The `.rdp` file contains preconfigured settings to simplify the connection process.
  - Clicked **Get Password** → uploaded the `.pem` key file → decrypted the Administrator password.  
    *Reasoning:* This step ensures that only someone with the correct private key can access the instance.
- Opened the `.rdp` file in Microsoft Remote Desktop and logged in using the decrypted password.

---

### 3️⃣ Verifying the Instance
- Created a folder named `LabTest` on the Windows desktop.  
  *Reasoning:* Demonstrates direct interaction with the instance and verifies that the connection was successful.
- The `LabTest` folder screenshot also includes the EC2 Instance ID, confirming the link between the AWS console and the RDP session.

---

## 📸 Screenshots

1. AWS console – EC2 instance in **running** state  
   <img width="1851" height="1172" alt="Image" src="https://github.com/user-attachments/assets/dcf25731-7ec5-4975-9afc-93cbffabb5d5" />

2. RDP connection from macOS – showing Windows desktop with `LabTest` folder and EC2 Instance ID visible  
 <img width="1819" height="1072" alt="Image" src="https://github.com/user-attachments/assets/e58814b5-37b1-499c-9186-7eaa76baf2a0" />


---

## 📚 Key AWS Concepts Demonstrated
- AWS account setup & resource creation
- EC2 instance launch process
- Windows AMI selection
- Security group configuration (least privilege)
- EBS storage basics
- AWS key pair usage for secure access
- Decrypting Windows Administrator password before first connection
- Cross-platform RDP connection
- Verifying instance functionality through desktop interaction

---

## 💡 Lessons Learned
- How to securely connect to Windows EC2 from macOS.
- Importance of restricting inbound traffic to trusted IPs.
- How to document AWS projects for a technical portfolio.

---

## 🔮 Future Improvements
- Enable and configure AWS Systems Manager for agent-based management.
- Deploy a sample application inside the Windows EC2 instance.
- Automate instance creation with AWS CLI or Terraform.


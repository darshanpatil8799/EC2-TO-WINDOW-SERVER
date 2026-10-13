<div align="center">

# ☁️ AWS EC2 – Windows Server Deployment

### 🚀 Launch, Configure & Remotely Access a Windows Server on AWS

**A beginner-friendly, hands-on cloud project by Darshan Patil**

![AWS](https://img.shields.io/badge/Cloud-AWS-orange?logo=amazonaws&logoColor=white)
![EC2](https://img.shields.io/badge/Service-Amazon%20EC2-FF9900?logo=amazonec2&logoColor=white)
![OS](https://img.shields.io/badge/OS-Windows%20Server-0078D4?logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

</div>

---

## 📌 Project Overview

This project demonstrates how to launch a **Windows Server instance on Amazon EC2** and connect to it remotely using **Remote Desktop Protocol (RDP)**.

Amazon EC2 provides virtual servers in the AWS Cloud, allowing users to deploy and manage workloads without maintaining physical hardware.

## 🎯 Objectives

- Launch a Windows Server EC2 instance.
- Configure the instance's basic networking and security settings.
- Retrieve the initial Windows Administrator password using the EC2 key pair.
- Connect to the Windows Server through Remote Desktop.
- Understand the fundamentals of cloud-based server administration.

## 🧰 AWS Services & Requirements

| Item | Purpose |
|---|---|
| **Amazon EC2** | Hosts the Windows Server virtual machine |
| **Windows Server AMI** | Provides the Windows operating system |
| **IAM permissions** | Allow authorized EC2 management |
| **Key pair** | Helps decrypt the initial Windows password |
| **VPC & subnet** | Provide network connectivity |
| **Security group** | Controls inbound and outbound traffic |
| **Remote Desktop (RDP)** | Provides a graphical remote connection |

## 🏗️ Architecture

```text
                 👤 Administrator
                        |
                        | AWS Management Console
                        v
                 ☁️ AWS Cloud / EC2
                        |
                 🖥️ Windows Server
                        |
                 🔐 Security Group
                        |
                 💻 Remote Desktop (RDP)
                        |
                        v
              Connected Windows Desktop
```

## ⚙️ Implementation Steps

1. **Sign in to AWS** and open the EC2 Dashboard.
2. **Launch an instance** and assign it a recognizable name, such as `windows-server-01`.
3. **Select a Windows Server AMI**.
4. **Choose an instance type** appropriate for your workload and budget.
5. **Create or select a key pair** and store the private key securely.
6. **Configure the security group** to allow RDP on TCP port `3389` only from your trusted IP address.
7. **Review the configuration** and launch the instance.
8. Wait until the instance is running and its status checks pass.
9. In the EC2 console, choose **Connect → RDP client**.
10. Select **Get password**, upload the private key, and decrypt the initial Windows password.
11. Download/open the Remote Desktop file, enter the Administrator credentials, and connect.
12. Verify that the Windows desktop loads successfully.

## 🔐 Security Best Practices

- **Restrict RDP (TCP 3389)** to your trusted IP address. Avoid opening it to `0.0.0.0/0`.
- Keep the private key file secure and never upload it to GitHub.
- Use IAM permissions based on least privilege.
- Use strong credentials and apply Windows updates.
- Stop or terminate resources when they are no longer needed to avoid unnecessary charges.
- Review AWS pricing and Free Tier eligibility before launching resources.

> **Important:** Windows Server uses RDP (port `3389`) for remote desktop access. SSH (port `22`) is not normally required for a standard Windows RDP connection.

## 💡 Key Learnings

- Understanding Amazon EC2 and Windows Server AMIs.
- Launching and managing a cloud-based virtual machine.
- Learning the role of key pairs and security groups.
- Connecting to a Windows instance with RDP.
- Practicing basic AWS cloud administration and security.

## 📸 Project Screenshots

Add your screenshots to a folder named `screenshots/`, then update the image links below.

```text
.
├── README.md
└── screenshots/
    ├── ec2-instance.png
    ├── security-group.png
    ├── rdp-password.png
    └── windows-desktop.png
```

Example:

```markdown
![EC2 Instance](screenshots/ec2-instance.png)
```

## 💰 Cost Awareness

EC2 instances, storage, and related resources may incur charges. Pricing and Free Tier eligibility depend on your account, region, instance type, and current AWS terms. Check the AWS pricing page before deployment and stop or terminate resources when finished.

## 🚀 Future Improvements

- Configure a secure administration workflow.
- Install and host a sample website on Windows Server.
- Explore CloudWatch monitoring and alarms.
- Document backup and recovery options.

## 👨‍💻 Author

**Darshan Patil**  
Cloud & DevOps Learner

- GitHub: [Add your GitHub profile link](https://github.com/)
- LinkedIn: [Add your LinkedIn profile link](https://www.linkedin.com/)

---

<div align="center">

**Learning by doing — building cloud skills one project at a time!** ☁️💻

⭐ If you find this project useful, consider giving the repository a star.

</div>

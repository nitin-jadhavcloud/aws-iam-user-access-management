# 🔐 AWS IAM User Access Management – Least Privilege Project

This project demonstrates how to implement **secure IAM user, group, and policy management in AWS** using the **Principle of Least Privilege**. It reflects a real-world scenario where users are assigned job-based access using AWS managed and custom IAM policies.

## 🟩 Project Summary

- 🔹 Created IAM Groups based on job roles (Admins, Developers, QA Teams)
- 🔹 Added IAM Users to respective groups
- 🔹 Attached appropriate AWS managed or custom policies to each group
- 🔹 Enforced least privilege access to services like EC2 and S3
- 🔹 Simulated support-level scenarios like permission troubleshooting and access configuration

## ❓ Why I Built This Project

As an aspiring AWS Cloud Support Engineer, I wanted to **simulate real-world IAM scenarios** faced in L1/L2 support roles.  
This project helps demonstrate how to:

- Resolve permission-related support tickets
- Create and troubleshoot IAM roles and policies
- Implement **secure access control** using the **Principle of Least Privilege**
- Apply job-role based access management (like real enterprise teams: Admins, Developers, QA)

It reflects common issues like:

- “User cannot access S3 bucket” – Solved using policy attachment
- “Developer unable to start EC2 instance” – Solved with custom EC2 policy
- “Grant full access to Admin team” – Solved using AWS managed policies

This project allowed me to practice **practical IAM concepts** beyond theory, just like those handled by support engineers in production environments.


This setup mirrors practical IAM tasks handled by AWS Cloud Support Engineers (L1/L2).

## ▶ What I Did – Step by Step (With Screenshots)

### ✅ Step 1: Created IAM Groups
I created three IAM groups to organize users by their job roles:
- `Admins`
- `Developers`
- `QA_Teams`

📸 ![IAM Group Dasboard ](./Screenshot/IAM-Group-Dashboard.png)

   ## Create user Dev_joh attach Devloper group





### ✅ Step 2: Created IAM Users and Assigned to Groups

Created 3 IAM users and added them to the appropriate group:
- `admin_riya` ➝ Assigned to `Admins`
- `dev_suresh` ➝ Assigned to `Developers`
- `qa_amit` ➝ Assigned to `QA_Teams`

📸 ![Create user Dev_joh  ](./Screenshot/Create-Devjoh-user-assignGroup-devlopers.png)

![Create user QA_amit  ](./Screenshot/QA-amit_user_assign-group.png)

![IAM dashboard  ](./Screenshot/IAM-Dashboard.png)



---

### ✅ Step 3: Created Custom S3 Read-Only Policy

Created a custom IAM policy (`S3ReadOnlyPolicy`) to allow **read-only access to a specific S3 bucket**.  
Then attached this policy to the `QA_Teams` group.

📸 ![Create S3readonly policy  ](./Screenshot/Create-S3ReadonlyPolicy-1.1.png)

## Attach S3 Read-only Policy to QA_teams Group

   ![Attach S3readonly policy  ](./Screenshot/Assign-S3ReadOnlyPolicy-QA-team-Group-1.1.png)

 ![Attach S3readonly policy  ](./Screenshot/Assign-S3ReadOnlyPolicy-QA-team-Group-1.2.png)


---

### ✅ Step 4: Created EC2 Start/Stop Policy

Created a custom IAM policy (`EC2StartStopPolicy`) to allow only **Start** and **Stop** actions for EC2 instances. 

📸 ![Create EC2Startstop policy  ](./Screenshot/Create-EC2StartStopPolicy-1.1.png)

 ## Attached this policy to the `Developers` group.

 ![Attach EC2Startstop policy  ](./Screenshot/attach-EC2policy-Devloper-group-1.1.png)

 ![Attach EC2Startstop policy  ](./Screenshot/attach-EC2policy-Devloper-group-1.2.png)


---

### ✅ tep 6: Gave Full Admin Access to Admins Group
Attached the built-in `AdministratorAccess` AWS managed policy to the `Admins` group.

- `AmazonEC2FullAccess`
- `AmazonS3FullAccess`

📸 ![Attach amazonEC2FullAccess  ](./Screenshot/Attach-AmazonEC2FullAccess-AdminGroup-1.1.png)

![Attach amazonEC2FullAccess  ](./Screenshot/Attach-AmazonEC2FullAccess-AdminGroup-1.2.png)



---


---

## 🎯 Project Objective

- Use IAM Groups to manage permissions easily
- Follow **Least Privilege Principle**
- Use Custom Policies for specific access (S3 read-only, EC2 Start/Stop)
- Use AWS Managed Policies where appropriate
- Simulate real support scenario for access issues



 


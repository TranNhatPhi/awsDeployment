---
title : "Preparation"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

{{% notice info %}}
You need to prepare the initial AWS resources, including creating an IAM Role with the necessary permissions for EC2, RDS, and S3.
{{% /notice %}}

To deploy a web application that interacts with RDS and S3, you need to configure an IAM Role that grants permissions for these services. In this preparation step, we will first create an IAM Role to ensure EC2 instances have the required permissions to interact with RDS and S3. After that, we will proceed to configure and deploy the application on EC2.

### Content
  - [Create IAM Role](2.1-create-iam-role/)
  - [Configure EC2 Instances](2.2-Configure-EC2-Instances/)

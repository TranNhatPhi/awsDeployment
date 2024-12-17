---
title : "Create ec2"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Create EC2

In this step, create an EC2 instance on AWS using the t3.small type (2GB RAM) as a server environment for the Spring Boot application, ensuring smooth performance without lag. Configure an IAM Role to connect to S3 and store images. Install AWS CLI/SDK and Docker on the EC2 instance. Use Docker to store the image of the Spring Boot application and deploy the container on EC2. Finally, use CloudWatch for monitoring and configure Auto Scaling if needed.

1. Go to [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Instances:v=3;$case=tags:true%5C,client:false;$regex=tags:false%5C,client:false)
   + Search **EC2**.
   + Click **EC2**, then click **Launch instance** to confirm.

![role](/images/2.prerequisite/Createec2-1.png)

![role1](/images/2.prerequisite/Createec2-2.png)

1. Go to [Create function](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#LaunchInstances:)
  + Create: name:Springbootdeployment2 /Name: **name:Springbootdeployment2**.
  + Click **Os:Ubuntu Server**
  + Click **Create Key pair**
  + Click **VPC Created**
  + Click **public subnet**
  + Click **Security Group**
  + Click **Check information configure storage and Launch  Instance**
![role1](/images/2.prerequisite/Createec2-3.0.png)
![role2](/images/2.prerequisite/Createec2-3.png)

![createpolicy](/images/2.prerequisite/Createec2-4.png)

![namerole](/images/2.prerequisite/Createec2-5.png)


![namerole1](/images/2.prerequisite/Createec2-6.png)

![namerole2](/images/2.prerequisite/Createec2-7.png)
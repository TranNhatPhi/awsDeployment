---
title : "Create Iam"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

This section outlines the steps to create an IAM Role for the architecture depicted in the diagram. The IAM Role will allow EC2 instances to interact with S3 for storage, RDS for database operations

The architecture overview after you complete this step will be as follows:


#### Create IAM role 

1. Go to [Create Iam Role](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/roles/create)
   + Click **Iam**.
   + Click **Create Role**.
   + Click **AWS service**, then click **ec2** to confirm.

![Iamrole1](/images/2.prerequisite/IAMrole1.png)

![Iamrole1](/images/2.prerequisite/IAMrole2.png)

![Iamrole1](/images/2.prerequisite/IAMrole3.png)

2. Go to [Add permissionsn ](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/roles/create?trustedEntityType=AWS_SERVICE&selectedService=EC2&selectedUseCase=EC2)
   + Click **AmazonEC2FullAccess**.
   + Click **AmazonS3FullAccess**.
   + Click **AmazonRDSFullAccess**

![Add permissions1](/images/2.prerequisite/IAMrole4.png)

![Add permissions2](/images/2.prerequisite/IAMrole5.png)

![Add permissions3](/images/2.prerequisite/IAMrole6.png)

1. Go to [Name, review, and create ](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/roles/details/phi1234?section=permissions)
   + Name **data-streaming-system-role**..
   + Click **Create Role**

![role1](/images/2.prerequisite/IAMrole7.png)
![role2](/images/2.prerequisite/IAMrole8.png)



### Content
  - [Create EC2](../2.2-create-ec2/)
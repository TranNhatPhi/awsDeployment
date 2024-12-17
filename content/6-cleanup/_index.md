+++
title = "Clean up resources"
date = 2022
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

We will take the following steps to delete the resources we created in this exercise.

#### Delete S3 Bucket

1. Go to [Amazon S3](https://ap-southeast-1.console.aws.amazon.com/s3/home?region=ap-southeast-1#)
   + Click **Instances**.
   + Click Name **deployment-image123*.
   + empty **bucket**.
   + delete name **deployment-image123**. 

![Clean](/images/6.clean/deleteS3.png)

![Clean](/images/6.clean/deleteS3-2'.png)

![Clean](/images/6.clean/deleteS3-3.png)

![Clean](/images/6.clean/deleteS3-4.png)
#### Delete RDS

Go to [RDS](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1#)
   + Click **Applications**.
   + Click **Actions** then enter **Delete**.

![Clean](/images/6.clean/delete-RDS.png)

#### Delete ec2
   + Click **instance springboot-myappsql**.
   + Click **stop instance**
   + click **teminate (delete)**

![Clean](/images/6.clean/deleteEc2-1.png)

![Clean](/images/6.clean/deleteec2-2.png)

#### Delete Iam role
   + Click **Roles**.
   + Click Roles name**data-streaming-system-role** then Click **Delete**, Re-enter the name and delete

![Clean](/images/6.clean/DeleteRoleIAM-1.png)

![Clean](/images/6.clean/deleteRoleiam-2.png)
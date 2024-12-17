---
title : "Deployment and Testing in ec2"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

In this step, check the inbound endpoint for Spring Boot on EC2, then test the API by registering and logging in via Postman, and verify the Product API using the GET method on Chrome.

1.check **inbound endpoint**

![File_Test](/images/5/allowinbound-rulesspringboot.png)

2.Go to **test IPv4 ec2**
 +  **test API**.
 + test postman **testapiresgiter**.
![File_Test](/images/5/TestAPiRegister.png)

 + test postman **testAPilogin**.
![File_Test](/images/5/testApilogin.png)
 + run on chorme method get **Product**
![File_Test](/images/5/testcacAPideploy.png)


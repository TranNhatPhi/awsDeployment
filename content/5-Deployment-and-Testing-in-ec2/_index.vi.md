---
title : "triển khai và kiểm thử ứng dụng springboot trên ec2"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

In this step, check the inbound endpoint for Spring Boot on EC2, then test the API by registering and logging in via Postman, and verify the Product API using the GET method on Chrome.

1.Kiểm tra **inbound endpoint**

![File_Test](/images/5/allowinbound-rulesspringboot.png)

2.truy cập vào **test IPv4 ec2**
 +  **test API**.
 + kiểm thử phần mêm postman **testapiresgiter**.
![File_Test](/images/5/TestAPiRegister.png)

 + kiểm thử phần mêmpostman **testAPilogin**.
![File_Test](/images/5/testApilogin.png)
 + chạy trên môi trương chomre method get **Product**
![File_Test](/images/5/testcacAPideploy.png)


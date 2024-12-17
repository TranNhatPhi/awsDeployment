---
title : "Tạo ec2"
ngày : "`r Sys.Date()`"
trọng lượng : 2
chương : false
trước: " <b> 2.2 </b> "
---

### Tạo ec2


Trong bước này, tạo một EC2 instance trên AWS với loại t3.small (RAM 2GB) để làm môi trường server cho ứng dụng Spring Boot, đảm bảo hoạt động mượt mà và không bị giật lag. Cấu hình IAM Role để kết nối và lưu trữ hình ảnh vào S3. Cài đặt AWS CLI/SDK và Docker trên EC2. Sử dụng Docker để lưu trữ image của ứng dụng Spring Boot và triển khai container trên EC2. Cuối cùng, sử dụng CloudWatch để giám sát và cấu hình Auto Scaling nếu cần thiết.

1. truy cập [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Instances:v=3;$case=tags:true%5C,client:false;$regex=tags:false%5C,client:false)
   + tìm kiếm **EC2**.
   + Nhấp vào **EC2**, sau dó Nhấp vào **Launch instance** to confirm.

![role](/images/2.prerequisite/Createec2-1.png)

![role1](/images/2.prerequisite/Createec2-2.png)

2. truy cập [Create function](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#LaunchInstances:)
  + Create: name:Springbootdeployment2 /Name: **name:Springbootdeployment2**.
  + Nhấp vào **Os:Ubuntu Server**
  + Nhấp vào **Tạo Key pair**
  + Nhấp vào **VPC Created**
  + Nhấp vào **public subnet**
  + Nhấp vào **Security Group**
  + Nhấp vào **check information configure storage and Launch  Instance**
![role1](/images/2.prerequisite/Createec2-3.0.png)
![role2](/images/2.prerequisite/Createec2-3.png)

![createpolicy](/images/2.prerequisite/Createec2-4.png)

![namerole](/images/2.prerequisite/Createec2-5.png)


![namerole1](/images/2.prerequisite/Createec2-6.png)

![namerole2](/images/2.prerequisite/Createec2-7.png)
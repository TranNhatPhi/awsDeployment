---
title : "Setup docker image"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

Quá trình tạo S3, RDS và Docker images bao gồm ba bước chính. Đầu tiên, để tạo S3, bạn truy cập dịch vụ S3, tạo một bucket có tên deployment-image123, bật các cài đặt cần thiết và tải hình ảnh lên S3. Tiếp theo, để tạo RDS, bạn truy cập dịch vụ RDS, tạo một cơ sở dữ liệu MySQL, cấu hình các tham số cần thiết và xác nhận để hoàn tất việc tạo cơ sở dữ liệu. Cuối cùng, với Docker, bạn truy cập Docker Hub, xây dựng Docker image bằng lệnh docker build, gắn thẻ với docker tag và đẩy image lên Docker Hub bằng lệnh docker push.

1. Go to [Create docker-image](https://hub.docker.com/repository/docker/phi1234/myapp-spring/general).
   + Go to **dockerhub**.
   + cmd **docker build -t myapp:1.0.4 -f ./DockerfileJavaSpring .** 
   + cmd **docker tag myapp:1.0.4 phi1234/myapp-spring:1.0.4**
   + cmd **docker push phi1234/myapp:1.0.4**
![Create docker-image](/images/3.s3/dockerfile1.png)
![Create docker-image](/images/3.s3/dockerfile2.png)

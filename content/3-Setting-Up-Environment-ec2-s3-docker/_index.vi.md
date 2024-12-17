---
title : "thiết lập môi truơng ec2,s3,RDS"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

Quá trình tạo S3, RDS và Docker image bao gồm ba bước chính. Đầu tiên, để tạo S3, bạn truy cập dịch vụ S3, tạo một bucket với tên deployment-image123, bật các cài đặt cần thiết và tải hình ảnh lên S3. Tiếp theo, trong bước tạo RDS, bạn truy cập dịch vụ RDS, tạo một cơ sở dữ liệu MySQL, cấu hình các thông số cần thiết và xác nhận để hoàn tất việc tạo cơ sở dữ liệu. Cuối cùng, đối với Docker, bạn truy cập Docker Hub, xây dựng Docker image bằng lệnh docker build, gắn thẻ với docker tag và đẩy image lên Docker Hub bằng lệnh docker push.

### Nội dung

 -[tạo S3](3.1-create-s3-uploadimage/) 
 
 -[tạo RDS](3.2-Create-RDS/)
 -[cài Dặt Docker image](3.3-setupDocker-Image/)
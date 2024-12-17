---
title : "Tạo RDS"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

Quy trình tạo RDS bao gồm: truy cập vào dịch vụ RDS, chọn Create Database, lựa chọn loại cơ sở dữ liệu MySQL, cấu hình các thông số cần thiết và xác nhận để tạo cơ sở dữ liệu thành công.

1. Đi tới [Tạo S3](https://ap-southeast-1.console.aws.amazon.com/s3/home?region=ap-southeast-1#).
   + Vào **jinmeister-datasource**.
   + Bấm vào **Thuộc tính**
   + Bấm vào **Thông báo sự kiện**
   + Bấm vào **Tạo thông báo sự kiện**
![Create S3](/images/3.s3/C-2.2.png)
![Create S3](/images/3.s3/C-3.png)

2. Đi tới **Tạo thông báo sự kiện**
   + Tên: data-upload/.txt .
   + Nhấn vào Tất cả sự kiện tạo đối tượng.
   + Nhấn vào Hàm Lambada.
   + Bấm chọn từ hàm Lambda của bạn.
   + Hàm Lambda: nhà sản xuất.

![Create S3](/images/3.s3/C-4.1.png)

![Create S3](/images/3.s3/C-5.png)

![Create S3](/images/3.s3/C-6.png)

![Create S3](/images/3.s3/C-7.1.png)
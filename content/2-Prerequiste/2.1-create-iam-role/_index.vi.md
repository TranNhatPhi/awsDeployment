---
title : "Tạo tôi"
ngày : "`r Sys.Date()`"
trọng lượng : 1
chương : false
trước: " <b> 2.1 </b> "
---

Phần này hướng dẫn các bước để tạo một IAM Role cho kiến trúc được mô tả trong sơ đồ. IAM Role này sẽ cho phép các phiên bản EC2 tương tác với S3 để lưu trữ và RDS để thực hiện các hoạt động cơ sở dữ liệu.

Tổng quan kiến trúc sau khi bạn hoàn thành bước này sẽ như sau:


#### Tạo vai trò IAM

1. Đi tới [Tạo vai trò Iam](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/roles/create)
   + Bấm vào **Iam**.
   + Bấm vào **Tạo vai trò**.
   + Bấm vào **Dịch vụ AWS**, sau đó bấm vào **ec2** để xác nhận.

![Iamrole1](/images/2.prerequisite/IAMrole1.png)

![Iamrole1](/images/2.prerequisite/IAMrole2.png)

![Iamrole1](/images/2.prerequisite/IAMrole3.png)

1. Đi tới [Thêm quyền](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/roles/create?trustedEntityType=AWS_SERVICE&selectedService=Lambda&selectedUseCase=Lambda)
   + Nhấp vào **AmazonEC2FullAccess**.
   + Nhấp vào **AmazonS3FullAccess**.
   + Nhấp vào **AmazonRDSFullAccess**

![Add permissions1](/images/2.prerequisite/IAMrole4.png)

![Add permissions2](/images/2.prerequisite/IAMrole5.png)

![Add permissions3](/images/2.prerequisite/IAMrole6.png)

3. Đi tới [Tên, đánh giá và tạo](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/roles/create?trustedEntityType=AWS_SERVICE&selectedService=Lambda&selectedUseCase=Lambda)
   + Tên **data-streaming-system-role**..
   + Bấm vào **Tạo vai trò**

![role1](/images/2.prerequisite/IAMrole7.png)
![role2](/images/2.prerequisite/IAMrole8.png)



### Nội dung
  - [Create EC2](../2.2-create-ec2/)
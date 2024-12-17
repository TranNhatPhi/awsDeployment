+++
  title = "Dọn dẹp tài nguyên"
  date = 2022
  weight = 6
  chapter = false
  pre = "<b>6. </b>"
+++


Chúng tôi sẽ thực hiện các bước sau để xóa tài nguyên mà chúng tôi đã tạo trong bài tập này.

#### xóa nhóm s3

1. truy cập vào [Amazon S3](https://ap-southeast-1.console.aws.amazon.com/s3/home?region=ap-southeast-1#)
   + nhấn **Instances**.
   + nhấn tên **deployment-image123*.
   + nhấn rỗng **bucket**.
   + xoó tên **deployment-image123**. 

![Clean](/images/6.clean/deleteS3.png)

![Clean](/images/6.clean/deleteS3-2'.png)

![Clean](/images/6.clean/deleteS3-3.png)

![Clean](/images/6.clean/deleteS3-4.png)
#### xóa cơ sở dữ liệu RDS

truy cập [RDS](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1#)
   + nhấn **Applications**.
   + nhấn **Actions** sau đó bấm enter **Delete**.

![Clean](/images/6.clean/delete-RDS.png)

#### Xoa môi trường ec2
   + nhấn **instance springboot-myappsql**.
   + nhấn **stop instance**
   + nhấn **teminate (delete)**

![Clean](/images/6.clean/deleteEc2-1.png)

![Clean](/images/6.clean/deleteec2-2.png)

#### xóa IAM ROle
   + nhấn **Roles**.
   + nhấn Roles tên**data-streaming-system-role** sau đó nhấn **Delete**, tiep tuc nhập tên và xoó

![Clean](/images/6.clean/DeleteRoleIAM-1.png)

![Clean](/images/6.clean/deleteRoleiam-2.png)
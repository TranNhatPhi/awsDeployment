---
  title : "các buớc chuẩn bị cho triển khai in ec2"
  date : "`r Sys.Date()`"
  weight : 1
  chapter : false
  pre : " <b> 4.1 </b> "
---


Hướng dẫn cài đặt Docker trên EC2, tạo môi trường Docker Compose cho PhpMyAdmin và MySQL, sau đó tạo cơ sở dữ liệu "myapp" trong container Docker.

#### các buớc chuẩn bị cho triển khai in ec2

1. Truy cập vào [các buớc chuẩn bị cho triển khai in ec2]()
  + Cài đặt Docker bằng lệnh  **sudo snap install docker**.
  + Tạo Docker Compose cho PhpMyAdmin 8 trên Ubuntu EC2 bằng lệnh **Create DockerCompose Phpmyadmin8 in ubuntu ec2**.
  + Tạo Docker Compose cho PhpMyAdmin 8 trên Ubuntu EC2 bằng lệnh **docker-compose -f ./deployment.yaml up -d mysql8-container**
  + Truy cập vào **ipv4 port:8100 login root in database**
  
![setup docker in ec2](/images/4/setupdockerec2.png)
![Create environment Phpmyadmin8 docker compose](/images/4/createEnvMySqlphpmyadmin8.png)
![Create server name:mysql123 port 3306](/images/4/deploymentyamlmySQL.png)
![login phpmyadmin by server in ec2](/images/4/loginphpmyadmin.png)
2. Truy cập vào **create database myapp in container docker**
  + tên: **myapp**.
  + chọn **lay co so du lieu co san tren may tinh**
  + xem **bảng đã tạo**
![tạo CSDL myapp va xem các bảng ](/images/4/createdatabase.png)
![bảng đã tạo](/images/4/tables.png)

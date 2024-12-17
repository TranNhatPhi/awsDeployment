---
title : "prerequiste-deployment-ec2"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

In this step , A guide to installing Docker on EC2, setting up a Docker Compose environment for PhpMyAdmin and MySQL, and then creating the "myapp" database within the Docker container.

#### prerequiste-deployment-in-ec2

1. Go to [prerequiste deployment ec2]()
  + Setup **sudo snap install docker**.
  + cmd **Create DockerCompose Phpmyadmin8 in ubuntu ec2**.
  + cmd **docker-compose -f ./deployment.yaml up -d mysql8-container**
  + go to **ipv4 port:8100 login root in database**
  
![setup docker in ec2](/images/4/setupdockerec2.png)
![Create environment Phpmyadmin8 docker compose](/images/4/createEnvMySqlphpmyadmin8.png)
![Create server name:mysql123 port 3306](/images/4/deploymentyamlmySQL.png)
![login phpmyadmin by server in ec2](/images/4/loginphpmyadmin.png)
2. Go to **create database myapp in container docker**
  + Name: **myapp**.
  + Click **get database in local**
  + watch **tables created**
![Create database myapp and watch infomation tables](/images/4/createdatabase.png)
![tables created](/images/4/tables.png)


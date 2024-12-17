---
title : "setup dockerhub in ec2"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

this step,A guide to setting up Docker and configuring Docker Compose on EC2 for services like MySQL, PhpMyAdmin, Redis, and Spring Boot.

#### setup **dockerhub-in-ec2**

1. cmd **cat deployment.yaml** 
  + Correct the following code.
  + docker compose **docker-compose -f ./deployment.yaml up -d mysql8-container**
  + check docker in ec2 **docker ps**
  + docker compose springboot **docker-compose -f ./deployment.yaml up -d myapp-spring-container**
  ```
  #scp -pr . root@103.124.93.29:/root/
services:
  mysql8-container:
    container_name: mysql123
    image: mysql:8.3.0    
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: 123456
      MYSQL_DATABASE: myapp
    ports:
      - 3308:3306
    #volumes: 
    #- ./sql/myapp.sql:/docker-entrypoint-initdb.d/init-script.sql
    networks:
      - myapp-network  

  phpmyadmin8-container:
    #intel host
    image: phpmyadmin/phpmyadmin    
    #image: arm64v8/phpmyadmin #choose this if you are running on Mac Apple Silicon(M1, M2,...)
    container_name: phpmyadmin8-container
    restart: always
    depends_on:
      - mysql8-container
    ports:
      - "8100:80" #port mapping
    environment:
      PMA_HOST: mysql8-container #phpMyAdmin Host, PMA = PHP My Amin
      PMA_PORT: 3306
      UPLOAD_LIMIT: 500M
    networks:
      - myapp-network
  
  redis-container:
    image: docker.io/redis:7.2.3
    container_name: redis-container
    restart: always
    ports:
      - "6379:6379" # Port mapping for Redis, you can change the host port as needed
    volumes:
      - ./redis-data:/data # Mount a volume for Redis data persistence
    networks:
      - myapp-network
  myapp-spring-container:    
    container_name: myapp-spring-container    
    build:
      context: .
      dockerfile: DockerfileJavaSpring      
      #docker tag <image_id> myapp-spring:1.0.0    
    ports:
      - 8099:8070
    environment:
      #SPRING_DATASOURCE_URL: jdbc:mysql://mysql8-container:3306/myapp?serverTimezone=UTC&allowPublicKeyRetrieval=true
      SPRING_DATASOURCE_URL: jdbc:mysql://mysql123:3306/myapp?serverTimezone=UTC&allowPublicKeyRetrieval=true            
      MYSQL_ROOT_PASSWORD: 123456
      REDIS_HOST: redis-container
      REDIS_PORT: 6379
      #Kafka broker
      # KAFKA_BROKER_SERVER: kafka-broker-01      
      # KAFKA_BROKER_PORT: 19092
    #depends_on only waits for the container to start, not for the service inside the container to be fully operational
    depends_on:      
      - mysql8-container
    networks:
      - myapp-network    
    # healthcheck:
    #   #test: ["CMD-SHELL", "curl --fail http://localhost:8088/healthcheck/health || exit 1"]
    #   test: ["CMD-SHELL", "curl --fail http://localhost:8088/api/v1/actuator/health || exit 1"]
    #   interval: 30s
    #   timeout: 10s
    #   retries: 3
    #   start_period: 20s #20s after container created, health check    
  #  angular-container:
  #   container_name: angular-container
  #   build:
  #     context: .  
  #     dockerfile: DockerfileAngular   # Dockerfile để xây dựng ứng dụng Angular
  #   ports:
  #   - "6000:4200"  # Port mapping, Angular sẽ chạy trên port 4200
  #   environment:
  #   - NODE_ENV=production
  #   volumes:
  #   - ./dist:/usr/share/nginx/html  # Mount the Angular build directory to the Nginx container
  #   depends_on:
  #   - backend  # Optionally add a dependency to your backend container if needed
  #   networks:
  #   - myapp-network
     
  # python-container:
  #   container_name: python-app-container
  #   build:
  #     context: .
  #     dockerfile: DockerfilePython  # Dockerfile cho ứng dụng Python
  #   ports:
  #     - "6000:5000"  # Mapping port cho Flask hoặc ứng dụng Python
  #   environment:
  #     - FLASK_APP=OCR4_python.py  # Tên file ứng dụng Python của bạn
  #     - FLASK_ENV=production  # Môi trường sản xuất
  #   depends_on:
  #     - mysql8-container
  #     - redis-container
  #   networks:
  #     - myapp-network
    
   
#docker-compose -f ./deployment.yaml down 

#docker-compose -f ./deployment.yaml rm -s -f mysql8-container
#docker-compose -f ./deployment.yaml up -d mysql8-container

#docker-compose -f ./deployment.yaml rm -s -f phpmyadmin8-container
#docker-compose -f ./deployment.yaml up -d phpmyadmin8-container


#docker-compose -f ./deployment.yaml rm -s -f myapp-spring-container 
#docker-compose -f ./deployment.yaml up -d myapp-spring-container 
#docker logs myapp-spring-container

#docker-compose -f ./deployment.yaml rm -s -f redis-container
#docker-compose -f ./deployment.yaml up -d redis-container

#docker-compose -f ./deployment.yaml rm -s -f angular-container

networks:
  myapp-network:
    name: myapp-network
    driver: bridge
  ```

![docker compose](/images/4/deploymentyamlmySQL.png)
![docker compose](/images/4/CreateSQl8-Container.png)
![docker compose](/images/4/dockerps.png)
![docker compose](/images/4/setupfileyamlspringboot.png)
![docker compose](/images/4/setupfileyamlspringboot.png)
![docker compose](/images/4/myappspringbootcontainer.png)
  
 
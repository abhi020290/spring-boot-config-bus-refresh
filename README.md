# spring-boot-config-server
spring-boot-config-server

#Refresh 
http://localhost:8888/actuator/refresh POST API

config should be git repository

Below is git repo Change it to you local git repo
https://github.com/abhi020290/spring-cloud-config 


docker run -d -p 15672:15672 -p 5672:5672 rabbitmq
rabbit MQ should run on 15672 port

Add below dependencies in client application

		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-bus-amqp</artifactId>
		</dependency>

Add below in application properties:

    spring.rabbitmq.host=localhost
    spring.rabbitmq.port=5672
    spring.rabbitmq.username=guest
    spring.rabbitmq.password=guest
    spring.rabbitmq.address=localhost:15672

URL to hit :  
        
    http://localhost:8090/actuator/bus-refresh

This will refresh all the application which as rabbit mq enable with port number.

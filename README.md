# Spring-Cloud-Eureka-with-Zuul
This is a sample about Spring Cloud Eureka and Spring Cloud Zuul.  
There are 3 modules in the sample.
## demo-eureka-server
The registration centre. Module demo-gateway and module demo-web are registered on this Spring Cloud Eureka server.
## demo-gateway
The gateway filter by Spring Cloud Zuul. The filter implemented in the sample is a "pre" filter, which means will be called before routing.
## demo-web
The destination after routing. There is only one method named "hello" showing the response message.

# Spring-Cloud-Eureka-with-Zuul
This is a sample about Spring Cloud Eureka and Spring Cloud Zuul.  
There are 3 modules in the sample.
## demo-eureka-server
The registration centre. Module demo-gateway and module demo-web are registered on this Spring Cloud Eureka server.
## demo-gateway
The gateway filtered by Spring Cloud Zuul. The filter implemented in the sample is a "pre" filter, which means will be called before routing.
## demo-web
The destination when you request "http://localhost:8767/web/hi" after routing. There is only one method named "hello" showing the response message. The "pre" filter in demo-gateway will check if there is any parameter named "id". The difference will be logged in console.
# Something new
## 2019.11.25
Add some configurations about exposing endpoints. You will see the mapping relationship between service and path after requesting "http://localhost:8767/actuator/routes".
## 2019.12.3
Add RestTemplate POST in demo-gateway to invoke method on service demo-web. You will reach "http://localhost:8768/hi" actually  when you request "http://localhost:8767/hello". 

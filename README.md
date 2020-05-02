# Microservices with Spring Boot and Eureka (with Feign Client)
This is an example of Spring boot microservices with Eureka and Feign client example.

The eurekaregistryserver acts as the Eureka Registry Server where microservices get registered. Here we have two microservices called userdata and countryclient which talks with each other using feign client by registering themselves on Eureka.

# Steps to test the application

Start the eurekaregistryserver as java application which will run on embeded Tomcat with port: 8761 

Then start userdata and countryclient services as java application which will run on embeded Tomcat with port: 8001 and post: 8000 respectively.

Then hit the URL: http://localhost:8001/user/country/detail/91 either through Postman or browser which will give output as,

{
    "country_id": 91,
    "name": "India",
    "capital": "Delhi",
    "continent": "Asia",
    "population": "130B"
}

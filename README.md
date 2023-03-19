

# Flight Booking System API DESIGN

This is an API Design of the Flight Booking System which was designed using the MICROSERVICE Architecture.It has 4 microservices  
1. Authentication Service  
2. Booking Service   
3. Flights Search Service  
4. Remainder Service


## High Level Design Diagram

[![FLIGHT-BOOKING-SYSTEM-API-Design.png](https://i.postimg.cc/7ZyP4wzP/FLIGHT-BOOKING-SYSTEM-API-Design.png)](https://postimg.cc/GHqnJ0z6)



## Tech Stack
**Server:** Node, Express  
**DataBase** : MySQL,Redis  
**Message Broker** : RabbitMQ  
**Architechture** : Microservice Architechture(Repository Pattern)  
**Tools** : Postman , Sequelize




## Features

- It is developed on the **Microservice** Architecture. 
- Implemented **JWT Token** authentication mechanism for authentication and authorisation of users.
- Implemented **API Gateway** which authenticates thetoken and also apply **Rate Limiting** does  which basically works as an **Reverse Proxy** and helps in preventing **Dos Attacks**.
- Implemented **Caching(Cache Aside Pattern)** in the **Flights Search Service**using **Redis** there by optimizing the response time.
- Implemented **CronJobs** in **Remainder Service** which automatically delete the already sent emails to the customers and **automatically sends an email** to customer.
- Implemented **interservice synchronous communication** using **HTTP(REST)APIs** and also **asychronous communication** using **Message Brokers** like **RabbitMQ**.



## Services

- ***Authentication service***   
It is used to autheticate the user using the JWT tokens   
Github Repo Link : [clickhere](https://github.com/SHAIKASIFALI/AUTH_SERVICE)

- ***FlightsSearchService*** 
It is used to search the flights between two different cities   
Github Repo Link : [clickhere](https://github.com/SHAIKASIFALI/FlightsandSearchService)  

- ***Booking Service***
It is used to Book the flights .  
Github Repo Link : [clickhere](https://github.com/SHAIKASIFALI/BoookingServicee)

- ***Remainder Service***
It is used to send emails to user regarding their flight bookings 
Github Repo Link : [clickhere](https://github.com/SHAIKASIFALI/REMAINDER-SERVICE)

- ***API Gateway***
It is used to route the client requests to their respective microservices also have ratelimiting in the API Gateway.  
Github Repo Link :[clickhere](https://github.com/SHAIKASIFALI/API-Gateway)




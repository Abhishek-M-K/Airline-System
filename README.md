# Airline-System

- Airline System's complete backend built on Node and Express following Microservice Architecture. 
Followed a linear approach while setting up the structure of services with implementation of MVC architecture and applied solid OOP principles for developing scalable APIs.
Tried to keep the codebase as maintainable as possible making it easier for debugging and future changes-updations .

- This Airline System consists of 4 Microservices primarily **Search Flights Service** , **Authentication Service** , **Booking Service** and **Flight Reminder Service** .
Each microservice has it's own set of service and can inter-communicate with other microservices.

- Followed manual error handling using clean practices as well as leveraged *http-status-codes* node package for enumerating the HTTP status codes for better error handling .

### Current Implementation :
- Implementing Message-Queues using *amqplib* node package and **RabbitMQ** for better query processing between inter-connected microservices .

### Search Flights Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-SearchFlights)
- Add Cities and Airports for each , there's a One-to-Many association

### Authentication Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-Auth)

### Flight Booking Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-Booking)

### Flight Reminder Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-FlightRemainder)


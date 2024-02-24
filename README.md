# Airline-System

- Airline System's complete backend built on Node and Express following Microservice Architecture. 
Followed a linear approach while setting up the structure of services with implementation of MVC architecture and applied solid OOP principles for developing scalable APIs.
Tried to keep the codebase as maintainable as possible making it easier for debugging and future changes-updations .

- This Airline System consists of 4 Microservices primarily **Search Flights Service** , **Authentication Service** , **Booking Service** and **Flight Reminder Service** .
Each microservice has it's own set of service and can inter-communicate with other microservices.

- Followed manual error handling using clean practices as well as leveraged *http-status-codes* node package for enumerating the HTTP status codes for better error handling .
- Deployed on AWS EC2 with horizontal autoscaling technique.

### Current Implementation :
- Implementing Message-Queues using *amqplib* node package and **RabbitMQ** for better query processing between inter-connected microservices .

### API Gateway 
**[Repository]** : (https://github.com/Abhishek-M-K/Airline-API-Gateway)

### Search Flights Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-SearchFlights)
- Add Cities and Airports for each , there's a One-to-Many association.
- Airplanes can be added with parameters like capacity, src_city, org.
- User can search flights by custom filters like maxPrice, minPrice, flight_id, src_city to dest_city.

### Authentication Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-Auth)
- Multi-level authorization with user/passenger, flight_staff, admin.
- Users are authenticated and authorized before performing a certain operation like adding a flight detail, etc.

### Flight Booking Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-Booking)
- Passenger is free to book flights through this microservice for him/herself + for the whole family (multiple booking).
- Connected with *Search Flights* service such that if a user has booked flight and then someone searches for the flight, the capacity/vacant seats appears dynamic.
- Orchestrated Nodemailer email-service for confirmation of Flight Booking.

### Flight Reminder Microservice 
**[Repository]** : (https://github.com/Abhishek-M-K/Microservice-FlightRemainder)
- Implemented cron-job for scheduling emails/reminders to the passengers after every specific time-interval through emails.
- Connected with *Booking* service to keep track of passengers and their bookings so as to schedule reminders.
- Adopted Message Queue **RabbitMQ** for better query handling between *Booking* & *Reminder* service.


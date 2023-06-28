# Loan System-BE

This project is a Java Spring Boot application that provides a backend API for a loan management system.
### Technologies Used
- Java Spring Boot
- Spring Data JPA
- MySQL Database

### System Design
- For user-based authentication, we are using a simple JWT token-based implementation. This is implemented using the Spring Security project.
- Spring Data JPA is being used for JPA based data access layers. DB entities, their relationships and repositories are being exposed using JPA.
- For auto settlement of the loans, Spring Schedulers are being used along with Spring @Async to execute the settlement request in parallel based on configured thresholds by the scheduler.

### Database Schema 
![image](https://user-images.githubusercontent.com/12005138/154504507-8fccc00d-89c3-4bd7-9d5a-80d012f5ed25.png)

The schema consists of the following tables:

users - This table stores the user information, such as the user's name, email address, and password.
loans - This table stores the loan information, such as the loan amount, the loan interest rate, and the loan term.
settlements - This table stores the settlement information, such as the settlement amount, the settlement date, and the settlement status.

### Improvements
- Shedlock/Quartz job-scheduling framework to make sure our scheduled tasks run only once at the same time in a multi-instance environment
- Application Dockerization
- Complete Microservices architecture using Spring Cloud/Kubernetes

### License
This project is licensed under the MIT License.


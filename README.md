# Learning Management System
---
I developed a full-stack web based LMS application that implements the core workflows of modern online learning platforms. The system offers an intuitive, role-specific interface that streamlines common academic interactions between students and instructors in a digital environment. For demo purposes, I designed and populated the platform with real courses and layouts inspired by my university and hosted the application on the cloud so users can use it reliably without needing to install anything.

You can check out the platform here:

**Live Demo**: [http://34.173.28.213:4200/login](http://34.173.28.213:4200/login)
---
## Features

- Secure login system provides personalized access and functionality based on whether the user is a student or instructor
- Students can browse available courses, manage their enrollments, and track their academic progress in one personalized home page
- Each course a student is enrolled in has its own dedicated page displaying course content, assignments, due dates, submissions, and grades (specific to the user)
- Instructors can create and manage courses, edit enrollment, post assignments, and view/grade student submissions
- Assignments can be submitted by students online prior to the due date, and returned with individual feedback from the instructor
- Grades are automatically calculated and updated, helping students stay informed across all courses

---

## Tech Stack

### Backend:
- **Java 17**, **Spring Boot** - Core application framework
- **Gradle** – Build automation and dependency management
- **PostgreSQL** - Relational database used by each service
- **Spring Security**, **JWT** - Authentication and role-based authorization
- **Spring Cloud Gateway**, **Eureka Discovery** – API routing and service registry
- **Spring Data JPA** – Data persistence and database interaction
- **Feign Clients** - Inter-service communication via REST
- **RESTful API** – Backend communication pattern for client interaction
- **RabbitMQ** - Asynchronous messaging between services

### Frontend:
- **Angular** - framework for building the UI
- **TypeScript** – Strongly typed JavaScript used in Angular
- **HTML**, **CSS** – Markup and styling for components
 

### DevOps:
- **Git** -	Version control and project collaboration
- **Docker** - Containerization of microservices
- **Docker Compose** – Orchestration tool to manage multi-container application setup
- **Postman** - API testing tool used for validating backend endpoints
- **Google Cloud Platform** - deployed via Compute Engine VM instance

---

## Microservices Overview

- **Inter-Service Communication**: Independent microservices communicate via REST using Feign clients
- **User Service** – Handles user registration, login, and role assignment using JWT for secure authentication
- **Course Service** – Manages course data, search functionality, and CRUD operations  
- **Enrollment Service** – Handles student enrollment using data retrieved from the User and Course services
- **Assignment Service** – Enables instructors to create assignments and students to view assigned work and due dates
- **Submission Service** – Handles student assignment submissions and scores/feedback from the instructor side
- **Gradebook Service** – Calculates overall grades for students based on submission scores and exposes grade data per course and student
- **Discovery Service** - Allows microservices to register themselves with Eureka so they can be dynamically discovered by other services
- **API Gateway Service**: Routes traffic to the appropriate service by acting as a centralized entry point for all client requests (via Spring Cloud Gateway and Eureka)
- **Containerization**: Dockerized all services and used Docker Compose to orchestrate and deploy the application on Google Cloud Platform


## Future Improvements

- OAuth2 support and enhanced security
- Redis caching and performance optimization
- CI/CD with Jenkins
- Kubernetes deployment for orchestration
- UI/UX improvements and full mobile responsiveness

---
## Author

**Sachin Manivannan**   


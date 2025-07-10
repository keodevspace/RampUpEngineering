Study Roadmap: Software Engineer (.NET, Angular, AWS, Docker, RabbitMQ, Kafka, Kubernetes)
==========================================================================================

This roadmap details a weekly study plan from July 2025 to March 2026, focusing on Angular, .NET Core, microservices architecture, AWS, Docker, messaging systems (RabbitMQ, Kafka), and Kubernetes. Practical projects will be integrated to consolidate learning.

📅 July 2025 - Month 1: Angular Fundamentals
--------------------------------------------

This month will be dedicated to the foundation of frontend development with Angular, essential for your future fullstack projects.

*   **Week 1:** Introduction to Angular
    
    *   Environment setup (Node.js, Angular CLI).
        
    *   Creating a new Angular project.
        
    *   Basic Angular project structure (modules, components, templates).
        
    *   Creating and using components (selectors, templates, styles).
        
    *   Component lifecycle (ngOnInit, ngOnDestroy, etc.).
        
*   **Week 2:** Data Binding and Directives
    
    *   Data Binding: Interpolation {{}}, Property Binding \[\], Event Binding (), Two-way Binding \[()\] with ngModel.
        
    *   Structural Directives: \*ngIf, \*ngFor, \*ngSwitch.
        
    *   Attribute Directives: ngClass, ngStyle.
        
    *   Creating custom directives (basic).
        
*   **Week 3:** Modules and Dependency Injection
    
    *   Concept of NgModule (root module, feature modules).
        
    *   Code organization with modules.
        
    *   Dependency Injection in Angular.
        
    *   Creating and using Services for business logic and data sharing.
        
    *   Providers and service scope.
        
*   **Week 4:** Routing in Angular
    
    *   RouterModule configuration and basic routes.
        
    *   Programmatic and declarative navigation.
        
    *   Passing route parameters (path params, query params).
        
    *   Lazy Loading modules for performance optimization.
        

📅 August 2025 - Month 2: Advanced Angular and Communication
------------------------------------------------------------

Deep dive into essential Angular features for building robust applications and interacting with APIs.

*   **Week 5:** Angular Forms
    
    *   Template-driven Forms: ngModel, basic validation.
        
    *   Reactive Forms: FormControl, FormGroup, FormArray.
        
    *   Custom and asynchronous validations.
        
    *   Handling complex forms.
        
*   **Week 6:** HTTP Communication and RxJS
    
    *   Using HttpClient to make HTTP requests (GET, POST, PUT, DELETE).
        
    *   Introduction to Observables with RxJS (subscribe, map, filter).
        
    *   Error handling in HTTP requests.
        
    *   CORS (Cross-Origin Resource Sharing) and how to handle it.
        
*   **Week 7:** State Management and Interceptors
    
    *   State management patterns (introduction to concepts like Redux/NgRx, BehaviorSubjects for simple state).
        
    *   Using Subjects and BehaviorSubjects for component communication.
        
    *   HTTP Interceptors to add headers (e.g., authentication tokens) or handle errors globally.
        
*   **Week 8:** Authentication, Authorization, and Frontend Project
    
    *   Implementing Route Guards (CanActivate, CanDeactivate).
        
    *   Frontend authentication and authorization strategies (JWT token storage).
        
    *   **Mini-Project Angular:** Build a small frontend CRUD that consumes a mocked API or the authentication API that will be developed.
        

📅 September 2025 - Month 3: ASP.NET Core, Clean Code & Start of Auth API Project
---------------------------------------------------------------------------------

Focus on backend fundamentals with .NET Core and the beginning of the first practical project.

*   **Week 9:** ASP.NET Core Web API and CRUD
    
    *   Creating an ASP.NET Core Web API project from scratch.
        
    *   Implementing CRUD (Create, Read, Update, Delete) operations for an entity (e.g., Order).
        
    *   Database configuration (SQL Server) and using Entity Framework Core.
        
*   **Week 10:** Dependency Injection and Logging
    
    *   Principles of Dependency Injection (DI) and how ASP.NET Core implements it.
        
    *   Configuring and using Serilog for structured logging.
        
    *   **Start of Project: 🔐 Auth API** - Initial structure of the authentication API. Definition of user models and roles.
        
*   **Week 11:** JWT Authentication and Documentation
    
    *   Implementing JWT (JSON Web Tokens) authentication in ASP.NET Core.
        
    *   Creating endpoints for registration, login, and token refresh.
        
    *   API documentation using Swagger/OpenAPI.
        
    *   **Project: 🔐 Auth API** - Full implementation of registration and login endpoints with JWT.
        
*   **Week 12:** Clean Code, SOLID, and Gitflow
    
    *   Refactoring the Auth API project applying Clean Code principles.
        
    *   Applying SOLID principles (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion).
        
    *   Introduction and practice of the Gitflow workflow for version control.
        

📅 October 2025 - Month 4: Testing, Docker, CI/CD & Conclusion of Auth API Project
----------------------------------------------------------------------------------

This month focuses on code quality, containerization, and automated deployment.

*   **Week 13:** Unit and Integration Tests
    
    *   Creating Unit Tests for the Auth API business logic (e.g., services, validations).
        
    *   Implementing Integration Tests with an in-memory or local database for API endpoints.
        
    *   Using testing frameworks (xUnit, NUnit, MSTest) and mocking (Moq).
        
    *   **Project: 🔐 Auth API** - Add unit and integration test coverage for the Auth API.
        
*   **Week 14:** Dockerization
    
    *   Introduction to Docker: concepts of images, containers, volumes.
        
    *   Creating a Dockerfile for the Auth API.
        
    *   Building and running the Docker image locally.
        
    *   **Project: 🔐 Auth API** - Dockerize the Auth API, ensuring it runs in a container.
        
*   **Week 15:** Docker Compose
    
    *   Using docker-compose to orchestrate multiple containers (e.g., Auth API + SQL Server + RabbitMQ).
        
    *   Configuring networks and volumes in docker-compose.
        
    *   **Project: 🔐 Auth API** - Create a docker-compose.yml for the Auth API and its database, allowing local execution with a single command.
        
*   **Week 16:** Basic CI/CD
    
    *   Introduction to CI/CD (Continuous Integration/Continuous Delivery) pipelines.
        
    *   Setting up a simple pipeline (GitHub Actions or Azure DevOps) for building and publishing the Docker image of the Auth API.
        
    *   **Project: 🔐 Auth API** - Configure a basic CI/CD pipeline for the Auth API, automating the build and push of the image to a registry.
        

📅 November 2025 - Month 5: RabbitMQ, Basic AWS & Start of Event-Driven API Project
-----------------------------------------------------------------------------------

Exploring messaging systems and the first steps in the AWS cloud.

*   **Week 17:** RabbitMQ Producer
    
    *   Introduction to Message Queues and RabbitMQ.
        
    *   Configuring RabbitMQ in the .NET Core project.
        
    *   Creating a Producer that sends an event (e.g., "Order Created") to a queue/exchange in RabbitMQ.
        
*   **Week 18:** RabbitMQ Consumer and Start of Event-Driven API Project
    
    *   Creating a Consumer that listens for and processes order events (e.g., status changes, sending notifications).
        
    *   **Start of Project: 📦 Event-Driven API** - Initial structure of an event-focused API. Definition of event types and their contracts.
        
*   **Week 19:** Dead Letter Queue and Retries
    
    *   Implementing Dead Letter Queue (DLQ) for messages that could not be processed.
        
    *   Configuring Retry policies for reprocessing failed messages.
        
    *   **Project: 📦 Event-Driven API** - Implement DLQ and retries to ensure the robustness of event processing.
        
*   **Week 20:** AWS EC2 and S3 Deployment
    
    *   Introduction to AWS: EC2 (virtual machines) and S3 (object storage).
        
    *   Deploying the Auth API or a simple service to AWS EC2.
        
    *   Storing files in S3 (e.g., order receipts, logs).
        
    *   **Project: 📦 Event-Driven API** - Initial deployment of one of the Event-Driven API services on EC2.
        

📅 December 2025 - Month 6: AWS, Kafka & Conclusion of Event-Driven API Project
-------------------------------------------------------------------------------

Deep dive into AWS services and introduction to Kafka for data stream processing.

*   **Week 21:** AWS RDS and CloudWatch
    
    *   Configuring a relational database (SQL Server) on AWS RDS (Relational Database Service).
        
    *   Monitoring logs and metrics with AWS CloudWatch.
        
    *   **Project: 📦 Event-Driven API** - Configure RDS for the API's database and CloudWatch for log monitoring.
        
*   **Week 22:** AWS SQS
    
    *   Introduction to AWS SQS (Simple Queue Service) for simple message queues.
        
    *   Creating and using SQS queues for asynchronous events (e.g., order confirmation emails).
        
    *   **Project: 📦 Event-Driven API** - Integration with SQS for a simpler message flow, perhaps for notifications.
        
*   **Week 23:** Kafka Producer
    
    *   Introduction to Apache Kafka: concepts of topics, producers, consumers, brokers.
        
    *   Configuring a Kafka Producer in the .NET Core project to publish order status updates to a Kafka topic.
        
    *   **Project: 📦 Event-Driven API** - Implement a Kafka Producer to emit status events.
        
*   **Week 24:** Kafka Consumer and Conclusion of Event-Driven API Project
    
    *   Creating a Kafka Consumer to read status events and update order status.
        
    *   **Project: 📦 Event-Driven API** - Implement a Kafka Consumer and conclude the project, ensuring communication between services via RabbitMQ and Kafka.
        

📅 January 2026 - Month 7: Microservices, Event-Driven Architecture & Start of Dashboard with Tests Project
-----------------------------------------------------------------------------------------------------------

Transition to microservices architecture and the beginning of a more complex fullstack project.

*   **Week 25:** Event-Driven Architecture (EDA) Modeling
    
    *   Review and deepen understanding of EDA, combining RabbitMQ and Kafka for different purposes (domain events vs. data streams).
        
    *   Microservices patterns (API Gateway, Service Discovery, Circuit Breaker).
        
*   **Week 26:** Microservices Division and Start of Dashboard Project
    
    *   Divide the Order API into two microservices:
        
        *   **Order Service:** Responsible for Order CRUD and acts as a RabbitMQ Producer.
            
        *   **Processing Service:** Consumes RabbitMQ events and acts as a Kafka Producer.
            
    *   **Start of Project: 📊 Dashboard with Tests** - Planning the dashboard architecture. Defining the backend microservices that will provide data for the dashboard.
        
*   **Week 27:** Status Update Microservice
    
    *   Creating a new microservice that consumes Kafka events to update order status in a centralized database or a query service.
        
    *   **Project: 📊 Dashboard with Tests** - Developing the backend microservices that the dashboard will consume, ensuring they provide the necessary data.
        
*   **Week 28:** Review, Refactoring, and Dockerization of Microservices
    
    *   Review and refactor existing microservices to ensure consistency and best practices.
        
    *   Update and optimize docker-compose to orchestrate all microservices.
        
    *   **Project: 📊 Dashboard with Tests** - Dockerization and integration of all backend microservices for the dashboard, ensuring they work together in a containerized environment.
        

📅 February 2026 - Month 8: DDD, Final Project & Conclusion of Dashboard with Tests Project
-------------------------------------------------------------------------------------------

Deep dive into Domain-Driven Design and the final phase of the fullstack project.

*   **Week 29:** Domain-Driven Design (DDD)
    
    *   Introduction to DDD: Bounded Contexts, Aggregates, Entities, Value Objects, Repositories.
        
    *   Analysis of the Order domain and adaptation: Order as Aggregate Root, OrderItem as Value Object.
        
*   **Week 30:** DDD Application and Dashboard Frontend
    
    *   Refactor existing microservices applying basic DDD concepts (Entities, Value Objects, Repositories).
        
    *   **Project: 📊 Dashboard with Tests** - Developing the Angular frontend of the dashboard, consuming data from backend microservices. Focus on data visualization and interactivity.
        
*   **Week 31:** Observability, E2E Tests, and Kubernetes Introduction
    
    *   Simulating failures in microservices and implementing resilience strategies.
        
    *   Implementing distributed logging (e.g., OpenTelemetry, Jaeger) and advanced monitoring with CloudWatch.
        
    *   **Introduction to Kubernetes:** Basic concepts of pods, deployments, services, and namespaces.
        
    *   **Project: 📊 Dashboard with Tests** - Implementing E2E (End-to-End) tests for the dashboard, covering both the Angular frontend and interaction with backend microservices.
        
*   **Week 32:** Finalizing the Complete Project
    
    *   Finalize the Dashboard with Tests project ensuring:
        
        *   Complete and functional microservices architecture.
            
        *   RabbitMQ and Kafka fully integrated for asynchronous communication.
            
        *   Dockerized APIs deployed on AWS (EC2, RDS, S3, SQS, CloudWatch).
            
        *   Working CI/CD pipeline for automated build and deployment.
            
        *   Complete documentation (Swagger for APIs, README for the project).
            
        *   Functional and tested Angular frontend.
            

📅 March 2026 - Month 9: Deepening and Review
---------------------------------------------

Month dedicated to consolidating knowledge, exploring advanced topics, and preparing for the job market.

*   **Week 33:** General Review and Reinforcement
    
    *   Review of all covered concepts: Angular, .NET Core, Microservices, AWS, Docker, RabbitMQ, Kafka, DDD, Testing, Kubernetes.
        
    *   Identification of weak points and deeper study of topics that generated more doubts.
        
*   **Week 34:** Advanced Topics
    
    *   Exploration of advanced topics: security (OAuth 2.0, OpenID Connect), performance (caching, query optimization).
        
    *   **Kubernetes Deep Dive:** Advanced topics like StatefulSets, Helm, Ingress, and autoscaling.
        
    *   Study of additional design patterns or more complex architectures.
        
*   **Week 35:** Interview Preparation
    
    *   Review of common algorithms and data structures in technical interviews.
        
    *   Practice solving logic and coding problems.
        
    *   Preparation of answers for behavioral questions and project experience.
        
*   **Week 36:** Personal Project or Open Source Contribution
    
    *   Start a new small personal project to apply and consolidate knowledge, or explore a new technology/framework of interest.
        
    *   Alternatively, contribute to an open-source project to gain practical and collaborative experience.

🧭 Task Management System — Spring Boot Microservices
📁 Project Structure
.
├── api-gateway/       # Routes client requests to appropriate microservices
├── task-service/      # Manages task creation, updates, and completion
├── user-service/      # Handles user registration, authentication, and profiles

🚀 Overview

The Task Management System is a distributed application built using Spring Boot microservices architecture.
It allows users to efficiently create, assign, and manage tasks while providing modular, scalable, and secure service boundaries.

Each service operates independently and communicates via REST APIs through a centralized API Gateway.

⚙️ Key Features
🧩 1. Microservices Architecture

Modular design with independent services.

Simplifies scaling, deployment, and maintenance.

Each service can have its own database and configurations.

🔐 2. API Gateway

Acts as a single entry point for all requests.

Routes API calls to the correct service (user or task).

Handles cross-cutting concerns such as:

Authentication & Authorization

Rate Limiting

Logging and Monitoring

CORS Configuration

👤 3. User Service

User registration, login, and authentication (using JWT or Spring Security).

Stores and manages user profiles.

Validates credentials and issues tokens.

📝 4. Task Service

Allows users to:

Create, update, and delete tasks.

Mark tasks as Pending, In Progress, or Completed.

Associates tasks with users (via user IDs).

Provides APIs to fetch user-specific tasks or tasks by status.

⚡ 5. Scalability & Flexibility

Each microservice can run independently on different ports.

Supports horizontal scaling.

Easy to extend with new services (e.g., notification, reporting).

🧱 6. Database Layer

Each service maintains its own database schema.

Promotes loose coupling and avoids direct inter-service data dependencies.

🌐 7. Inter-Service Communication

REST-based synchronous communication between microservices.

API Gateway manages and routes external requests.

🧰 Tech Stack
Layer	Technology
Framework	Spring Boot
API Gateway	Spring Cloud Gateway
Service Discovery (optional)	Netflix Eureka
Communication	REST API (Spring Web)
Security	Spring Security + JWT
Database	MySQL / PostgreSQL / MongoDB
Build Tool	Maven / Gradle
Containerization (optional)	Docker
🧩 Microservice Ports (Example)
Service	Port
API Gateway	8080
User Service	8081
Task Service	8082
🧪 How to Run the Project
1️⃣ Clone the Repository
git clone https://github.com/Kabirichhpilani/OrganizePro.git
cd OrganizePro

2️⃣ Run Each Service

In separate terminals:

# Start User Service
cd user-service
mvn spring-boot:run

# Start Task Service
cd ../task-service
mvn spring-boot:run

# Start API Gateway
cd ../api-gateway
mvn spring-boot:run

3️⃣ Access the Application

API Gateway: http://localhost:8080

🔗 Example Endpoints
👤 User Service
Method	Endpoint	Description
POST	/users/register	Register new user
POST	/users/login	Authenticate user
GET	/users/{id}	Get user details
📝 Task Service
Method	Endpoint	Description
POST	/tasks	Create a task
GET	/tasks/user/{userId}	Get all tasks for a user
PUT	/tasks/{id}/status	Update task status
DELETE	/tasks/{id}	Delete task
🚀 Future Enhancements

🧠 Add Service Discovery (Eureka Server)

📨 Add Notification Service (Email/SMS)

📊 Include Task Analytics Dashboard

🧾 Centralized Logging with ELK Stack

☁️ Docker & Kubernetes Deployment

👨‍💻 Author

Kabir Ichhpilani(2310990705)

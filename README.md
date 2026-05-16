# ecommerce-microservices-platform
Distributed E-Commerce backend platform built using Spring Boot, Spring Cloud, Microservices Architecture, Docker, and REST APIs.

## Architecture Diagram

![Architecture](architecture/microservices-architecture.svg)


## Tech Stack

- Java
- Spring Boot
- Spring Cloud
- Eureka Discovery Server
- API Gateway
- Config Server
- Docker
- Resilience4j
- Zipkin
- MongoDB / MySQL
- JWT Authentication
- Stripe Integration
- Swagger UI
- Cloudinary - assets upload

## Services

| Service | Description |
|---      |---          |
| Auth Service | Handles user authentication, JWT token generation/validation, and credential management |
| Product Service | Manages product catalog APIs, product operations, and inventory-related workflows |
| Order Service | Handles order creation, order workflows, and communication with payment services |
| Profile Service | Manages user profile data, account-related operations, and user information APIs |
| Gateway Service | Centralized API Gateway responsible for request routing, filtering, authentication flow, and load-balanced communication between clients and microservices |
| Discovery Service | Eureka-based service registry enabling dynamic service registration, discovery, and inter-service communication in the distributed system |
| Config Server | Centralized configuration management using environment-specific YAML configurations for different deployment environments such as dev, test, and production |
| Payment Validation Service | Handles payment verification, business rules validations like HMAC Signature, Payment Attempt thresold and, Duplicate Transaction Rule, and secure payment processing logic |
| Stripe Provider Service | Integrates Stripe payment gateway APIs for payment execution and external transaction handling |

---

# 🔗 Service Repositories

- [Auth Service](https://github.com/C00deian/FlipkartAuthService)
- [Gateway Service](https://github.com/C00deian/FlipkartGatewayService)
- [Product Service](https://github.com/C00deian/FlipkartProductService)
- [Order Service](https://github.com/C00deian/FlipkartOrderService)
- [Profile Service](https://github.com/C00deian/FlipkartUserService)
- [Payment Service](https://github.com/C00deian/FlipkartPaymentValidationService)
- [Stripe Integration Service](https://github.com/C00deian/FlipkartStripeProviderService )
- [Discovery Service](https://github.com/C00deian/FlipkartDiscoveryService )
- [Config Server](https://github.com/C00deian/flipkartclone-config-server )


---

# 🔄 Request Flow

```text
Client → API Gateway → Microservice → Database
```

### Payment Workflow

```text
Order Service → Payment Validation Service → Stripe Provider Service
```

---

# 🏗️ Architecture Highlights

- Distributed Microservices Architecture
- API Gateway-based centralized routing
- Eureka Service Discovery for dynamic service registration
- Centralized Configuration Management using Config Server
- JWT-based Authentication & Authorization
- Dockerized Services for scalable deployment
- Independent Database per Service
- REST API-based inter-service communication
- Kafka-based asynchronous event processing
- Environment-specific YAML configurations

---

# 🐳 Docker Support

All services are containerized using Docker for easier deployment, scalability, and environment consistency.

---

# 📡 Event-Driven Communication

Kafka and Zookeeper are used for asynchronous communication and event-driven workflows between services such as order processing and payment operations.

---


---

# ⚡ Production-Grade Engineering Features

- Distributed tracing implemented using Zipkin for request tracking across microservices
- Centralized logging and monitoring support for observability across distributed services
- Rate limiting implemented at API Gateway level for request throttling and protection
- Circuit Breaker pattern implemented between Auth Service and Profile Service for fault tolerance
- Resilient payment workflow using Circuit Breaker pattern:
  
```text
Order Service → Payment Validation Service → Stripe Provider Service
```

- Fault-tolerant inter-service communication using resilience patterns
- Environment-specific centralized configuration management
- Dockerized distributed deployment architecture


# 📚 Future Improvements

- Redis Caching
- CI/CD Pipelines using GitHub Actions
- Kubernetes Deployment
- Centralized Metrics Dashboard
- Automated Cloud Deployment

---

# 🎯 Current Goals

- Building scalable backend systems
- Improving distributed system design
- Learning production-grade microservices architecture
- Enhancing cloud and DevOps knowledge

---

# 👨‍💻 Author

Ritik Kumar

Java Backend Developer focused on scalable backend systems, distributed architecture, and microservices engineering.
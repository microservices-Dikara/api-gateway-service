# API Gateway Service

## Overview
The **API Gateway Service** acts as a **single entry point** for all client requests in a microservices architecture.  
It is responsible for routing requests to the appropriate microservices while handling security and other cross-cutting concerns.

By centralizing access through the API Gateway, clients do not need to know the internal structure or locations of individual services.

---

## Responsibilities
The API Gateway Service is responsible for:

- **Authentication & Authorization**  
  Validating JWT tokens before forwarding requests to downstream services.

- **Request Routing**  
  Routing incoming requests to the appropriate microservices such as Auth Service and User Service using service discovery.

- **Security Layer**  
  Protecting internal microservices by exposing only the gateway to external clients.

- **Cross-Cutting Concerns**  
  Handling logging, request filtering, header forwarding, and security policies.

---

## Architecture Flow
Client  
→ API Gateway  
→ Microservices (Auth Service, User Service, etc.)  
→ Response back to Client

---

## Tech Stack
- Java  
- Spring Boot  
- Spring Cloud Gateway  
- Spring Cloud Netflix Eureka  
- JWT Authentication  

---

## Integration
This service integrates with:

- **Discovery Service (Eureka Server)**  
  For dynamic service registration and discovery.

- **Auth Service**  
  For token validation and access control.

- **User Service and other microservices**  
  As routing destinations for client requests.

---

## Benefits
- Centralized entry point for clients
- Improved security through centralized authentication
- Simplified client-side communication
- Scalable and maintainable microservices architecture

---

## Notes
This API Gateway Service is part of a **Spring Cloud Microservices Architecture**, designed to support scalable, secure, and maintainable distributed systems.

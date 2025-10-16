# 🧱 Common Module - Shared DTO Library

The **Common DTO** module provides a set of **shared data transfer objects (DTOs)** and **utility classes** used across all microservices in the architecture.  
It acts as a lightweight dependency that ensures **consistent data structures**, **serialization**, and **communication** between services.

---

## 🚀 Overview

This library centralizes all common objects exchanged between services, avoiding duplication and ensuring data consistency across the system.  
It is imported as a Maven dependency by other services, such as **BookingService**, **InventoryService**, and **OrderService**.

---

## ⚙️ Key Features

- **Shared DTOs** for inter-service communication  
- **Lightweight JAR module** with no runtime dependencies  
- **Lombok** integration to reduce boilerplate code  
- **Java 21** compatibility  

---

## 🧩 Architecture Integration

![Architecture du projet](docs/schemaProject.png)

The **Common DTO** module is part of a **5-repository microservice ecosystem**:

1. **Common (common-dto)** – Shared DTOs and utilities used across all services.  
2. **Booking Service** – Handles booking operations and publishes events using DTOs.  
3. **Inventory Service** – Manages venue and event availability using shared DTOs.  
4. **Order Service** – Manages customer orders and consumes booking/inventory events.  
5. **API Gateway** – Routes and secures API access to all backend services.

All microservices depend on this module to exchange messages and payloads consistently — both over REST APIs and **Kafka** topics.

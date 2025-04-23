# ecommerce-backend-microservices-springboot
 Scalable e-commerce backend built with Spring Boot microservices, Docker, and PostgreSQL. Features API Gateway, Eureka Discovery, and service observability with Grafana.

This project is a hands-on implementation of a **microservices-based backend system** built with **Spring Boot, Docker, and PostgreSQL**. It simulates a simplified e-commerce platform where users can view products, place orders, and check product availability in inventory.

The entire system is broken down into independent, scalable services that talk to each other securely and reliably — just like real-world cloud-native systems used by companies like Amazon or Netflix.

---

## 💡 What This Project Is About

The goal of this project is to demonstrate how different microservices can work together in a distributed architecture. Each microservice focuses on a single responsibility and communicates with others through well-defined APIs. The services are containerized using Docker and orchestrated using Docker Compose.

If you're learning **Spring Boot**, **microservices**, or **cloud-native development**, this project is a great real-world example to explore.

---

## 🧱 Architecture Overview

Here's how the services interact:

![image](https://github.com/user-attachments/assets/28cb7c89-c968-48c6-b064-bf3af5cdbeb0)

![image](https://github.com/user-attachments/assets/b9231911-65fb-4ebd-adb4-bf4ebc8491fe)


User Requests
     │
     ▼
API Gateway (Routing & Auth)
     │
     ├──► Product Service (List products)
     ├──► Order Service (Place orders)
     └──► Inventory Service (Check stock)
     
Discovery Server (Eureka) helps them find each other.
Each service has its own PostgreSQL database.
Monitoring handled by Grafana.
```

## 📦 Tech Stack

- **Java 17 + Spring Boot 3**
- **Spring Cloud** (Gateway, Eureka)
- **Docker & Docker Compose**
- **PostgreSQL** (each service has its own DB)
- **Grafana** for monitoring
- **Maven** for build & dependencies

## 🚀 How to Run the Project

**Requirements:**
- Docker installed on your system
- Java 17 (if you want to run individual services outside Docker)

**To run everything:**

```bash
git clone https://github.com/your-username/spring-boot-microservices.git
cd spring-boot-microservices
docker-compose up --build
```

> ⏱ First run might take a few minutes as Docker builds and pulls images.


## 🌐 Services Overview

| Service           | Port | Description |
|------------------|------|-------------|
| API Gateway       | 8080 | Entry point for all services |
| Eureka Discovery  | 8761 | Registers all microservices |
| Product Service   | 8081 | Returns product info |
| Order Service     | 8082 | Places new orders |
| Inventory Service | 8083 | Checks stock availability |
| Grafana Dashboard | 3000 | Monitors service health |

---

## 📊 Observability

Grafana is pre-configured with dashboards to visualize service metrics. You'll find the dashboard config in `Grafana_Dashboard.json`.

**Login:**
- URL: `http://localhost:3000`
- Username: `admin`
- Password: `admin`


## 🧪 Testing

Each service includes basic unit and integration tests.

```bash
./mvnw test
```

## 📁 Project Structure

```
spring-boot-microservices/
├── api-gateway/
├── discovery-server/
├── product-service/
├── order-service/
├── inventory-service/
├── docker-compose.yml
├── Grafana_Dashboard.json
└── README.md
```

## 🙌 Contributing

Feel free to fork this repo and contribute! Whether it's fixing bugs, writing docs, or adding features — contributions are always welcome.


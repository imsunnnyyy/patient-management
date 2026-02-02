# Patient Management System

A backend microservices project built using Spring Boot to manage patients, billing, and analytics with event-driven and service-to-service communication.

## Services Overview

patient-service  
Handles patient CRUD operations and publishes domain events to Kafka.

billing-service  
Manages billing logic and communicates with patient-service using gRPC.

analytics-service  
Consumes Kafka events for reporting and analytical use cases.

## Technology Stack

- Java 17
- Spring Boot
- REST APIs
- Apache Kafka
- gRPC
- PostgreSQL
- Docker (local infrastructure)

## Architecture Summary

- patient-service publishes events to Kafka
- billing-service and analytics-service consume those events
- patient-service calls billing-service using gRPC

## Running the Application Locally

### Prerequisites

- Java 17 or higher
- Maven 3.9 or higher
- Docker and Docker Compose

### Start Infrastructure

Run Kafka and databases using Docker:


### Run Services

Navigate into each service directory and run:


Recommended order:
1. patient-service
2. billing-service
3. analytics-service


## Key Takeaways

- Clean microservices separation
- Event-driven architecture using Kafka
- gRPC-based inter-service communication
- Docker-based local development setup



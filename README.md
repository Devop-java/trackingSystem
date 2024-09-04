# Spring Boot REST API with JPA and PostgreSQL

## Overview

This project is a Spring Boot REST API application that uses JPA (Java Persistence API) for data persistence and PostgreSQL as the database. It demonstrates a typical CRUD (Create, Read, Update, Delete) application.

## Features

- RESTful API endpoints for managing resources
- JPA for ORM (Object-Relational Mapping)
- PostgreSQL as the database
- Basic error handling and validation

## Prerequisites

Before running the application, ensure you have the following installed:

- Java 11 or later
- Maven or Gradle (for building the project)
- PostgreSQL
- IDE (e.g., IntelliJ IDEA, Eclipse, or Visual Studio Code)

## Setup and Installation

### 1. Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
#Configure PostgreSQL
CREATE DATABASE trackdb;

# Configure Application Properties

Edit the src/main/resources/application.properties file to set up your PostgreSQL database connection. Replace placeholders with your actual database details:
Like:
spring.datasource.url=jdbc:postgresql://localhost:5432/your_database_name
spring.datasource.username=your_database_username
spring.datasource.password=your_database_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

#Build and Run the Application
java -jar yourjar.jar

#API Endpoints
Post : /parsel/save
Save All Required Detail
RequestBody: {"originCountryId":"91","destinationCountryId":"91","weight":"34gm","customerId":"17","customerName":"Ranjit Kumar","customerSlug":"Blue-Dart"}
Response:{
    "status": "Ok",
    "code": 200,
    "message": "Save Successfully",
    "data": {
        "id": 9,
        "trackNumber": "nNsTtqDSSz3C",
        "originCountryId": "91",
        "destinationCountryId": "91",
        "weight": "34gm",
        "createdAt": "2024-09-04T10:32:19.157+00:00",
        "customerId": "17",
        "customerName": "Ranjit Kumar",
        "customerSlug": "Blue-Dart"
    }
}




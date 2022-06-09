# capgemini-microservice

# Content
- [ About }
- [ Getting Started ]
- [ Usage ]
- [ Scope ]
# About
A simple project to demonstrate how micro-services can communicate and share data between each other.

# Getting Started
The follow instructions will guide you on how to have a copy of the project up and running on your computer for development and testing purposes.

## Prerequisites
- Java 11 or later
- Docker
## Dependencies
The project is a combination of three (independent) git repos:

- Customer Service: ( https://github.com/jango042/customer-service.git )
- Account Service: ( https://github.com/jango042/account-service.git )
- Transaction Service: ( https://github.com/jango042/transaction-service.git )
Git Submodules is used to sync the dependencies.

## Installing
- Clone this repo
- Pull submodules
> git submodule update --init --recursive 
cd into individual service and build them to create the .jar file using this below command

> mvn clean install -DskipTests=true
> Run Docker compose

> docker-compose up --build

# OR run detached
> docker-compose up --build -d
# Usage
See the postman api docs

# Scope
The project demonstrates a simple microservices communication setup.

The scope does not includes:

- Authenticated RESTful-based communication between customer-service and Account-service.
- Account-service and billing-worker-service communicates using OpenFeign
- Some level of request validation

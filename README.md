# sov-tech-assignment
### A Full-Stack StarWars Web Application using Spring Boot 3 and Angular 16
This repository is a parent repository that contains two submodules, starwars-graphql-service (a backend service) and starwars-service-client (a front end service).

## Getting Started
### Prerequisites
1. Java 17+
2. Maven
3. Node
4. Angular CLI
5. Docker

### How to  Run



1. #### To run the complete application using ```docker-compose```, follow the steps below: `Recommended method`

   1. Clone the parent repository with its submodules using the command below:
      ````
      git clone --recurse-submodules git@github.com:asopiah/sov-tech-assignment.git
      ````
      This will clone the parent repository along with its submodules.
   
   2. Navigate to the `starwars-graphql-service` directory and run the command below to build and package the backend service:

      ```mvn clean install```
   
      ##### NB: you can run the command directly without navigating to the directory using ``mvn clean install -f starwars-graphql-service`
   3. Navigate to the `starwars-service-client` directory and run the command below to build the front end service:
      ```agsl
      npm install
      ng build
      ```
      ##### NB: you can run the command directly without navigating to the directory using below

      ```agsl
      npm install --prefix starwars-service-client
      ng build --prefix starwars-service-client
      ```
   4. Once the above steps are completed successfully, navigate to the root directory of the parent repository and run the following command to start the application:

      ```docker-compose up --build```
   5. Finally, visit http://localhost:4200 in your browser to access the application.

2. #### To run the application by starting **[backend]()** and **[frontend]()** separately - _the traditional way_
   **Backend**
   1. Clone the parent repository with its submodules using the command below:
      ````
      git clone --recurse-submodules git@github.com:asopiah/sov-tech-assignment.git
      ````
        This will clone the parent repository along with its submodules.
   
   2. `cd starwars-graphql-service`
   3. Run `mvn install`
   4. Run `mvn spring-boot:run`
   5. The backend server is running on [localhost:8080]()
   
   **Frontend**

   1. Install [Node.js and npm](https://www.npmjs.com/get-npm)
   2. `cd starwars-service-client`.
   3. Run `npm install`.
   4. Run `ng serve`
   5. The frontend client is running on [localhost:4200]().

## Technology Stacks
Docker-Compose - _use to build and run the whole application_

**Backend**
- Java 17
- Spring Boot 3.0.6
- Spring Security
- Basic Authentication
- WebFlux 
- GraphQL
- Logback
- Maven
- Docker

**Frontend**
- Angular 16
- Angular CLI
- [Clarity Design](https://clarity.design/) for UI
- Docker
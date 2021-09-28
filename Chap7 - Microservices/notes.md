# Microservices
- Traditionally, softwares were made in a way that all the dependencies and libraries were packaged in one large application
- With the advent of microservice architecture, a single big application is deployed as a set of smaller services
- Each service is independent from each other and communicate with each other mostly via REST APIs
- Suited for projects which are continuously changing and complex
- The following image illustrates the difference:

<p align="center"><img src="https://courses.edx.org/assets/courseware/v1/c8353742b159161f64edbcbabce031a6/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Monoliths-Microservices.png" align=""></p> 

## Refactoring monolith into microservices
- Some basic ideas which can help in this process are listed below:
    1. For existing large monlith application, it is better to dismantle it piece by piece. Overtime, the functionalities would become microservices
    2. Split the monolith based on business logic (Presentation layer, data access, etc.). It is recommended to have a local database for each service. 
    3. Splitting based on modules
## Benefits of microservices
- Components can be written in differnet languages, since they communicate only using API endpoints
- Each service is independent and the failure of one service does not break the whole application
- Services can be reused in other projects
- Allows Continuous Delivery (CD) since services can be updated at runtime
- Services can be deployed across different data centers as well as different cloud providers
## Challenges
- Selecting the scope of a service, meaning how much functionalities should it implement
- Deployment needs to be done using an orchestrator
- Testing of the whole system due to many moving parts
- Inter-service communication cost 
- Many databases that depend/need to sync to each other
- Monitoring of microservices
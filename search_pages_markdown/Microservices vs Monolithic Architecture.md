# Microservices vs Monolithic Architecture

## Monolithic Architecture

![monolithic](../search_pics/Microservices%20vs%20Monolithic%20Architecture/monolithic.png)

- Applications were built modularly, but deployed in a large single applications.
- If you needed to make a change, you would have to test the entire application after the change to see if it worked before redeploying.
- If there is a large increase in activity for a specific feature of an application for a brief time period, you need resources to scale the entire application (not just that feature) since all the features are deployed in the large application package.

## Microservices

![microservices](../search_pics/Microservices%20vs%20Monolithic%20Architecture/microservices.png)

- The entire application is split into multiple different sub-applications called "microservices" which are each deployed separately on their own servers.
- The "microservices" communicate with each other through REST APIs, to allow the application to run like normal. For example, a "microservice" could be made for a shopping catalogue application and another for a user's view application. The user's view application would communicate with the shopping catalogue application to determine and show the relevant items in the shopping catalogue.
- It allows for more flexible scaling (can scale up only certain parts of application as needed) and development (only need to test the "microservice" where the change was made)."Microservice Architecture" refers to how an application is split into microservices for maximal efficiency.A Docker container can be used to run each microservice.
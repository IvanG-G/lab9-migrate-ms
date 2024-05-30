# lab9-migrate-ms

## **Objectives:**
  * Design a microservices architecture based on a given set of requirements.
  * Simulate the decomposition of a monolithic architecture into microservices.
  * Reflect on the design decisions and discuss alternative approaches.

## **Tasks:**
  * **Design Exercise:**
  * **Application Brief:** Participants are given a description of a monolithic e-commerce application handling user management, product catalog, order processing, and customer support.
  * **Task:** Identify and outline potential microservices based on domain-driven design principles. Participants will determine service boundaries, define how services will communicate, and plan how to handle shared data.



## **Monolithic E-Commerce Application Description:**
The application is a traditional e-commerce platform that encompasses all functionalities within a single, unified software architecture. The application handles the following key operations:

  * **User Management:** Manages user profiles, authentication, and authorization. It stores personal information, manages login sessions, and handles user preferences.

  * **Product Catalog:** Maintains a comprehensive list of products, including descriptions, pricing, images, and inventory levels. It supports product search and categorization functionalities.

  * **Order Processing:** Manages all aspects of the ordering process, from cart management to order placement, payment processing, and order history tracking.

  * **Customer Support:** Handles customer inquiries, returns, complaints, and feedback through a ticket-based system integrated with the user and order databases.

The application is built on a single relational database that holds all user data, product information, orders, and customer support interactions. It currently operates on a single code base with a web-based frontend that communicates directly with the backend server.

The platform has been experiencing challenges with scaling during high-traffic periods, frequent downtimes during updates, and increasing difficulty in implementing new features without affecting existing functionalities. The goal is to decompose this monolithic architecture into a microservices-based architecture to address these issues and improve overall agility and scalability.

## **Implementation Simulation:**
  * **Migration Roadmap:** Develop a detailed plan for migrating the identified monolithic components to microservices. This plan should include prioritization of services to be migrated, identification of dependencies, and a strategy for data migration.
  * **Architecture Documentation:** Document the proposed microservices architecture, illustrating the interaction between services and the migration steps. Include a brief narrative explaining the rationale behind key decisions.


## **Plan:**

The first thing to do is to create the databases and migrate the most important to clients, their personal information, we also should be creating the user management API, and modify and erase all the things where we are using user information on monolithic service, then when the micro service is running, we should point to those endpoints from the front. 
We should repeat this in order to create all the microservices in the next order of APIs:
  * User Management
  * Order Processing
  * Product Catalog
  * Customer Support
  * Orchestrator API: meanwhile we dont use this orchestrator we can use lambdas or serverless event driven services to orchestrate the microservices. Then change to Orch API, because is cheaper. 
<img width="907" alt="image" src="https://github.com/IvanG-G/lab9-migrate-ms/assets/138608967/afbf5cb8-cad5-41df-bf7c-e6e0e95c1619">





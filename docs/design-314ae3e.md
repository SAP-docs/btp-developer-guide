<!-- loio314ae3eac1244588b15dd146f1aa0a51 -->

# Design

In ABAP you decide and prepare during the design phase for each ABAP Cloud use case: transactional, analytical, and integration. ABAP Cloud follows a model-driven architecture that standardizes the programming model and tooling to deliver efficiency, scalability, and consistency from the database layer to business service exposure.



<a name="loio314ae3eac1244588b15dd146f1aa0a51__section_c5g_mb3_tyb"/>

## ABAP Cloud Design Principles

ABAP Cloud builds on the strengths of powerful frameworks and a standardized architecture for different use cases, aiming at saving as much implementation time as possible while providing you with flexibility - you can model your business processes with apps and services based on your business requirements along predefined technical processes. As much as possible is handled by the frameworks to decrease the probability of consistency errors during runtime. This standardized and consistent architecture across all apps and services developed with ABAP Cloud has many advantages from development perspective:

-   Model-driven and standardized: A common architecture and powerful frameworks cover routine technical tasks, reducing boilerplate and runtime inconsistencies while giving you flexibility to shape business processes.
-   Productivity and scale: Once you learn the ABAP Cloud development model, patterns and artifacts are reused across apps and services, decreasing effort for every additional implementation.
-   Maintainability and testability: Consistent structure improves code quality. Built-in mock frameworks for data models and events support automated tests and help prevent regressions at all test levels.
-   High abstraction: Low‑level infrastructure concerns are handled by the frameworks. Cloud-optimized ABAP languages such as the Data Definition Language \(DDL\) and Entity Manipulation Language \(EML\) align closely with data modeling and the ABAP development process.



<a name="loio314ae3eac1244588b15dd146f1aa0a51__section_f5h_3fy_ygc"/>

## **Typical Development Use Case Patterns**

We recommend implementing the following use case patterns on SAP BTP:

-   Customer-focused applications and extensions \(loosely coupled\)

    -   Decoupled lifecycle from the core system

    -   Separate user groups without SAP S/4HANA Cloud access

    -   Independent workload management

    -   Hub scenarios consolidating data from multiple backend systems for cloud use


-   Partner solutions

    -   Create and operate multitenant SaaS applications on SAP BTP

    -   Develop Add-On Products that customers can install directly in their own SAP BTP ABAP environment


-   Other use cases

    -   Develop mobile applications or business process automation that connect multiple systems

    -   Build extensions requiring scalability and elasticity independent of the SAP S/4HANA Cloud system

    -   Analyze ABAP code using the ABAP Test Cockpit \(ATC\) with integrated SAP Code Vulnerability Analyzer \(CVA\) checks for static quality assurance and to evaluate the impact of custom code during the transition to a clean core





<a name="loio314ae3eac1244588b15dd146f1aa0a51__section_c2s_mb3_tyb"/>

## Benefits of the Model-Driven Approach

A standardized architecture approach has the following benefits:

-   Faster delivery and easier reuse

    A standardized stack scales across many apps and services. Clear separation of concerns between data model behavior and service exposure makes the same domain model usable for transactional and analytical scenarios.

-   Interoperability by design

    Implementations follow the same technical rules, contracts, and process flows. You can design end-to-end processes without reinventing authorization, locking, or consistency mechanisms for each step.




<a name="loio314ae3eac1244588b15dd146f1aa0a51__section_ynz_z43_tyb"/>

## Basic Design-Time Architecture

Get to know the basics of the design-time architecture:

-   Three-tier structure

    All programming aspects build on a three-tier architecture covering data access, domain model and implementation, and service exposure. This design is derived from the transactional aspect and applied consistently across use cases.

-   Multipurpose Core Data Service \(CDS\) models

    The same CDS-based domain model can serve multiple purposes. With aspect‑specific annotations, you can expose the model as both an OData service \(transactional\) and an Information Access \(InA\) service \(analytical\).


**Related Information**  


[ABAP Cloud: Background Concepts and Overview: Design](https://help.sap.com/docs/abap-cloud/abap-cloud/design-with-programming-model-aspects)


<!-- loio314ae3eac1244588b15dd146f1aa0a51 -->

# Design



<a name="loio314ae3eac1244588b15dd146f1aa0a51__section_c5g_mb3_tyb"/>

## ABAP Cloud Design Principles

ABAP Cloud is based on a model-driven architecture approach that focuses on improving development efficiency through standardization and formalization of the programming model and the tooling environment ensuring efficiency and scalability. Programming models generally define the design time software architecture with specific technologies, concepts, and development objects. It essentially defines a standard architecture for app and service development from the database to the business service exposure.

ABAP Cloud builds on the strengths of powerful frameworks and a standardized architecture for different use cases, aiming at saving as much implementation time as possible while providing you with flexibility - you can model your business processes with apps and services based on your business requirements along predefined technical processes. As much as possible is handled by the frameworks to decrease the probability of consistency errors during runtime. This standardized and consistent architecture across all apps and services developed with ABAP Cloud has many advantages from development perspective:

-   Efficiency increase and scalability

    The developer efficiency is increased because standard architecture patterns are easily scalable. Once you are familiar with developing with the ABAP Cloud development model, the additional effort decreases with each developed service or application.

-   Adaptability and maintenance

    A standardized architecture fosters code quality and thus testability and code maintenance. ABAP Cloud comes with specific mock-frameworks for data models and events that support the code quality assurance and avoid regressions on all test levels.

-   High abstraction level

    The development model executes all low-level technical and infrastructure-related tasks.


The cloud-optimized ABAP languages like Data Definition Language or the Entity Manipulation Language match the data modeling requirements and are designed to support the modeling and ABAP-specific development process as closely as possible.



<a name="loio314ae3eac1244588b15dd146f1aa0a51__section_c2s_mb3_tyb"/>

## Benefits of the Model-Driven Approach

A standardized architecture approach saves you time and scales easily with multiple apps or services. In case of ABAP Cloud, also ensures the separation of concerns between data model behavior, and service exposure ensuring interoperability between different use cases, so that you can reuse data models for different purposes like analytical reports and transactional apps at the same time.



<a name="loio314ae3eac1244588b15dd146f1aa0a51__section_ynz_z43_tyb"/>

## Transactional Consistency Across Applications and Services

Interoperability is guaranteed because all implementations adhere to the same technical rule set, and the framework determines the technical contracts and process flows. This enables you to design end-to-end processes without having to worry about how to implement an authorization or locking concept for only for one specific part of the process. Instead, you make process design decisions that incorporate the technological advantages of the different ABAP Cloud technologies, frameworks, and building blocks in each step of a process. For more details about transactional consistency, see Transactional Consistency.

**Related Information**  


[Design a Transactional Application](design-a-transactional-application-608432c.md "")

[Design an Analytical Application](design-an-analytical-application-8819cb7.md "")

[Design an Integration Service](design-an-integration-service-ec2ac31.md "")


# Domain-Driven Design

## What is Domain-Driven Design?

Domain-Driven Design (DDD) is an approach to software development that focuses on modelling the core domain of a problem space and aligning the software design with the domain's concepts and language.
It emphasizes collaboration between domain experts and developers to create a shared understanding of the problem domain.

DDD is well-suited for finding an appropriate modularization for a business application by identifying *Bounded Contexts* that represent distinct *subdomains*.
A microservice architecture aligns well with DDD's principles of modularization and encapsulation, making it a suitable choice for implementing the modular structure defined by DDD.
This leads to highly maintainable, scalable, and loosely coupled systems that accurately reflect the problem domain.

Following the steps below will assist you in designing and developing your application.

* **Discover the Domain:**
  * Collaborate with domain experts to gain a deep understanding of the problem domain.
  * Identify key concepts, behaviors, and relationships within the domain.
* **Define the Ubiquitous Language:**
  * Establish a common language that domain experts and developers can use to communicate effectively.
  * Create a glossary of terms that accurately represent the domain concepts.
* **Define Bounded Contexts:**
  * Divide the system into Bounded Contexts, which are self-contained units representing specific subdomains.
  * Define clear boundaries between Bounded Contexts to enable independent development and encapsulation.
* **Model the Domain:**
  * Design the domain model by identifying and defining domain entities, aggregates, value objects, and domain services.
  * Capture domain behavior through domain events and domain-specific business rules.
* **Iteratively Refine the Model:**
  * Continuously refine and iterate on the domain model based on feedback from domain experts and the development team.
  * Validate the model's correctness and usability through tests and domain exploration.
* **Apply Tactical Design Patterns:**
  * Utilize tactical design patterns like Aggregates, Entities, Value Objects, Repositories, and Domain Services to structure the domain model.
  * Implement the patterns to ensure consistency, encapsulation, and maintainability.
* **Integrate with Infrastructure:**
  * Connect the domain model with the underlying infrastructure, such as databases, messaging systems, or user interfaces.
  * Use patterns like the Repository pattern to abstract data access and ensure persistence and retrieval of domain objects.
* **Continuously Collaborate:**
  * Maintain an ongoing collaboration between developers, domain experts, and stakeholders to refine the model and align it with evolving business needs.
  * Adapt the model as the understanding of the domain deepens or requirements change.

## Benefits and Challenges

DDD aims to create a shared understanding of the business goals and the domain model that underlies the software system.
It comes with its own benefits and challenges:

### Benefits

* **Simplicity**: DDD helps manage large and complex domains by breaking them down into smaller, simpler parts that can be understood and implemented independently.
* **Alignment**: DDD helps align the software system with the business goals and the domain model, ensuring each part of the system has its own clear and focused purpose and language.
* **Team Autonomy and Collaboration**: DDD enables team autonomy and collaboration by allowing teams to work on different parts of the system without interfering with each other, while still maintaining the integration and alignment of the whole system.
* **Consistency and Integrity**: DDD ensures the consistency and integrity of the domain model by encapsulating the internal state and behavior of domain objects, and enforcing the business rules and invariants within the design patterns and building blocks.
* **Readability and Expressiveness**: DDD enhances the readability and expressiveness of the code by using a common and consistent vocabulary that reflects the domain concepts and terms, and expressing the domain logic and rules through the design patterns and building blocks.
* **Agility and Adaptability**: DDD enables the agility and adaptability of the software system by allowing it to evolve along with the changing needs and expectations of the stakeholders.
* **Domain Understanding**: DDD enforces the stakeholders to gain a good understanding of the domain and its subdomains, as well as the relationships and dependencies between them. This may involve a lot of analysis, experimentation, and feedback from the stakeholders.

### Challenges

* **System Design and Maintenance**: DDD requires careful design and maintenance of the parts of the system, such as the bounded contexts, the ubiquitous language, and the context mapping, which should be meaningful and stable, and should protect the integrity and the consistency of the system.
* **Interface Design and Maintenance**: DDD requires careful design and maintenance of the interfaces and the integration strategies between different parts of the system, as well as the management of the data consistency and the evolution of the schemas.
* **Collaboration and Communication**: DDD requires close collaboration and communication between domain experts, users, and developers, as well as a common and consistent language that can be used to describe and implement the system.
* **Skill and Experience**: DDD requires a high level of skill and experience from the developers, as well as a good knowledge of the design patterns and building blocks that are used to design and implement domain-driven systems.

## Core Concepts

### Strategic Design

Strategic Design is the process of defining and modeling the high-level architecture and organization of a software system.
It focuses on creating a shared understanding of the business goals and the domain model that underlies the software system:

* Identifying the core domains, subdomains, and bounded contexts that make up the system. A domain is a sphere of knowledge or activity that the system supports. A subdomain is a subset of the domain that has its own specific logic and rules. A Bounded Context enforces a well-defined boundary that separates a subdomain from other subdomains and contains a consistent and coherent domain model that is aligned with the business language and processes.
* Establishing a clear and consistent language that can be used to communicate about the system’s architecture and organization. This language is called the ubiquitous language and it is a common and consistent vocabulary that is used by both domain experts and developers to communicate about the domain. The ubiquitous language should be reflected in the code, the database, and the documentation of the system.
* Defining the boundaries and the relationships between different bounded contexts. This is done by using context mapping, which is a technique that shows how different bounded contexts interact and depend on each other. Context mapping also helps to identify the integration strategies and the patterns that can be used to ensure the consistency and the integrity of the data and the behavior across different bounded contexts.

### Tactical Design

Tactical Design is a set of design patterns and building blocks that are used to design and implement domain-driven systems.
It is more hands-on and closer to the actual code than Strategic Design, which deals with the high-level architecture and organization of the system and aims to refine the domain model to a stage where it can be converted into working code. Tactical Design involves the following patterns and building blocks:

* **Entities:** Objects that have a unique identity and a lifecycle, and that represent concepts of the business, information about the business situation, and business rules.
* **Value Objects:** Objects that have no identity and are defined only by the values of their attributes, and that are immutable and self-validating.
* **Aggregates:** Clusters of one or more entities and value objects that form a consistency boundary and have a root entity that acts as the entry point and the gatekeeper for the aggregate.
* **Domain Services:** Standalone interfaces that represent domain operations that require multiple domain objects as inputs or outputs, and that encapsulate the domain logic and rules for that operation.
* **Repositories:** Abstractions over the data access layer that provide a way to store and fetch aggregates while hiding the details of how they are persisted.
* **Factories:** Abstractions that provide a way to create complex objects, such as aggregates, entities, or value objects, while hiding the details of how they are constructed.
* **Events:** Indications of significant occurrences that have happened in the domain and that need to be reported to other stakeholders belonging to the domain.
* **Modules:** Logical groupings of domain objects that help to segregate concepts and follow the ubiquitous language.

### Domain

In the context of DDD , the term **"domain"** refers to the specific subject area or problem space in which the software system operates.
It represents the real-world business or technical context that the software aims to model and address.

The domain encompasses a particular industry, business sector, or application area.
It includes the concepts, rules, processes, behaviours, and relationships that are relevant to the problem at hand.
The Domain is the focal point of DDD, as the approach emphasizes understanding and capturing the intricacies of the domain to drive the software design.
By deeply understanding the Domain, DDD practitioners can develop a shared language and mental model that aligns the software solution with the business requirements and objectives.
This alignment enables the development team to create a more effective, maintainable, and flexible software system that accurately reflects the needs of the problem domain.
In DDD, the Domain is often broken down into subdomains, which represent specific areas or divisions within the larger problem space.
Each subdomain may have its own bounded context(s), which defines the boundaries and scope of the associated models and concepts.
Overall, the Domain in DDD refers to the unique problem space, including its rules, concepts, and behaviours, that the software system aims to model and support.
Understanding and effectively modelling the Domain is key to creating successful software solutions using DDD principles.

### Ubiquitous Language

Ubiquitous Language, a term coined by Eric Evans, is a common and consistent vocabulary used by both domain experts and developers to communicate about the domain.
It's a key practice of DDD as it helps bridge the gap between the business and technical sides of a software project, ensuring that the domain model reflects the true understanding and needs of the stakeholders.
Here are the key characteristics of Ubiquitous Language:

* **Expression**: Ubiquitous Language is expressed in the domain model, the code, the database, and the documentation of a software system. It should be reflected in every aspect of the software implementation, making the code readable and meaningful to both developers and domain experts.
* **Unity**: Ubiquitous Language unites the people of the project team, regardless of their roles and backgrounds. It fosters a collaborative and productive environment where everyone speaks the same language and understands each other clearly.
* **Elimination of Inaccuracies**: Ubiquitous Language eliminates inaccuracies and contradictions from the domain. It's based on the careful analysis and validation of the domain concepts and terms, avoiding the use of ambiguous or misleading words that may cause confusion or misunderstanding.
* **Shared Language**: Ubiquitous Language is not a business language imposed by domain experts, nor a technical language invented by developers. It's a shared language co-created and evolved by both domain experts and developers, based on their mutual feedback and learning.
* **Contextual Language**: Ubiquitous Language is not a generic language used in industries, nor a specific language used in subdomains. It's a contextual language tailored to the particular domain and Bounded Context of a software project. Ubiquitous Language may vary from one Bounded Context to another, depending on the different perspectives and purposes of the subdomains.

### Bounded Context

Bounded Contexts help to manage large and complex domains by dividing them into smaller, more manageable parts.
A Bounded Context is a well-defined area of responsibility that contains a consistent and coherent domain model aligned with business language and processes. They are often *good candidates for modules or microservices*.

They help to deal with the complexity and diversity of large and evolving domains. A Bounded Context is a part of the domain where a specific model, language, and logic apply consistently. By dividing a large domain into smaller and more manageable Bounded Contexts, developers can focus on the core concepts and behavior of each context, and avoid confusion and inconsistency with other contexts.

Here are the key characteristics of a Bounded Context:

* **Logical Boundary**: A Bounded Context is a logical boundary that separates a subdomain from other subdomains. A subdomain is a subset of the domain with its own specific logic and rules.
* **Physical Boundary**: A Bounded Context is a physical boundary that isolates a software implementation from other implementations. It can be implemented as a separate service, module, or application that communicates with other Bounded Contexts through well-defined interfaces.
* **Linguistic Boundary**: A Bounded Context is a linguistic boundary that defines a Ubiquitous Language for a subdomain. A Ubiquitous Language is a common and consistent vocabulary used by both domain experts and developers to communicate about the domain.
* **Complexity Reduction**: Bounded Contexts reduce the complexity of the domain by breaking it down into smaller and simpler parts that can be understood and implemented independently.
* **Cohesion and Consistency**: Bounded Contexts increase the cohesion and consistency of the domain model by ensuring that each Bounded Context has its own clear and focused purpose and language.
* **Team Autonomy and Collaboration**: Bounded Contexts enable the autonomy and collaboration of teams by allowing them to work on different Bounded Contexts without interfering with each other, while still maintaining the integration and alignment of the whole system.
* **Domain Understanding**: Defining Bounded Contexts requires a good understanding of the domain and its subdomains, as well as the relationships and dependencies between them.
* **Interface Design**: Bounded Contexts require a careful design of the interfaces and the integration strategies between different Bounded Contexts. This may involve the use of methods such as Context Mapping.

### Aggregate

An Aggregate is a cluster of domain objects that can be treated as a single unit, which has a well-defined boundary and identity, and it helps manage the complexity and consistency of a domain model.
Here are the key characteristics of an Aggregate:

* **Composition**: An Aggregate is composed of one or more entities and value objects, which are the building blocks of a domain model. Entities have a unique identity and a lifecycle, while value objects represent a value or a measurement and are immutable.
* **Aggregate Root**: The Aggregate has an aggregate root, an entity that acts as the entry point and the gatekeeper for the Aggregate. The aggregate root enforces the business rules and the invariants of the Aggregate, ensuring its consistency and integrity.
* **Transactional Boundary**: An Aggregate is a transactional boundary that defines the scope and the granularity of the changes that can be made to the Aggregate. Any operation that affects the Aggregate should be atomic, consistent, isolated, and durable (ACID).
* **Consistency and Integrity**: Aggregates ensure the consistency and integrity of the domain model by encapsulating the internal state and behavior of a cluster of related objects.
* **Atomicity and Transactional Integrity**: Aggregates enable atomicity and transactional integrity by treating the changes made within an Aggregate as a single unit of work.
* **Optimized Data Access**: Aggregates help optimize data access and minimize data consistency conflicts by reducing the number of objects that need to be loaded into memory.
* **Modular and Scalable Design**: Aggregates facilitate modular and scalable software design by allowing developers to focus on the behavior and the identity of the Aggregate.
* **Agility and Adaptability**: Aggregates enable the agility and adaptability of the software system by allowing it to evolve along with the changing needs and expectations of the stakeholders.

### Entities

Entities are objects that have a unique identity and a lifecycle, and they represent concepts of the business, information about the business situation, and business rules.
Here are the key characteristics of an Entity:

* **Identity**: An Entity is defined by its identity, rather than its attributes. An Entity can be distinguished from other entities even if they have the same attributes.
* **Continuity and History**: An Entity has a continuity and a history. It can change its state over time, but it remains the same entity throughout its lifespan.
* **State and Behavior**: An Entity encapsulates the state and the behavior of an object in the domain. It has attributes that describe its properties, and methods that define its operations.
* **Aggregation**: An Entity aggregates other entities and value objects. It can contain other entities or value objects that are related to it, and that form a cohesive whole.
* **Transactional Boundary**: An Entity is a transactional boundary. It should be modified as a whole, and not partially or concurrently. This means that any operation that affects the Entity should be atomic, consistent, isolated, and durable (ACID).
* **Consistency and Integrity**: Entities ensure the consistency and integrity of the domain model by encapsulating the internal state and behavior of an object in the domain, and by enforcing the business rules and invariants within the Entity.
* **Identification and Tracking**: Entities enable the identification and tracking of objects in the domain by providing a unique and stable identity for each Entity, and by allowing the Entity to change its state over time without losing its identity.
* **Communication and Collaboration**: Entities facilitate the communication and collaboration between domain experts, users, and developers by using a common and consistent vocabulary that reflects the domain concepts and terms, and by expressing the domain logic and rules through the Entity methods.
* **Agility and Adaptability**: Entities enable the agility and adaptability of the software system by allowing it to evolve along with the changing needs and expectations of the stakeholders.
* **Entity Identity Design and Maintenance**: Entities require a careful design and maintenance of the entity identity, which is the entry point and the gatekeeper for the Entity. The entity identity should be meaningful and stable, and should protect the integrity and the consistency of the Entity.
* **Interface Design and Maintenance**: Entities require a careful design and maintenance of the interfaces and the integration strategies between different entities, as well as the management of the data consistency and the evolution of the schemas.

### Value Objects

Value Objects represent a concept or a thing in the domain that is defined solely by its attributes or properties, rather than by its identity.
In other words, value objects have no distinct identity and are defined entirely by their state.
Here are the key characteristics of a Value Object:

* **Immutability**: A Value Object is immutable, meaning that its state cannot be changed after creation. Any operation that would modify the state of a Value Object should return a new Value Object instead.
* **Equality**: A Value Object is equal to another Value Object of the same type if and only if they have the same attributes or properties.
* **Self-Validation**: A Value Object is self-validating, meaning that it can only be created with valid values. Any attempt to create a Value Object with invalid values should result in an exception or a failure.
* **Side-Effect Free**: A Value Object is side-effect free, meaning that it does not depend on or affect any external state. A Value Object should only use its own attributes or properties to perform its operations, and should not cause any changes to other objects or resources.
* **Consistency and Integrity**: Value Objects ensure the consistency and integrity of the domain model by encapsulating the internal state and behavior of a concept or a thing in the domain, and by enforcing the business rules and invariants within the Value Object.
* **Readability and Expressiveness**: Value Objects enable the readability and expressiveness of the code by using a common and consistent vocabulary that reflects the domain concepts and terms, and by expressing the domain logic and rules through the Value Object methods.
* **Performance and Scalability**: Value Objects facilitate the performance and scalability of the software system by reducing the memory footprint and the database access, and by allowing the Value Objects to be cached, shared, or distributed.
* **Agility and Adaptability**: Value Objects enable the agility and adaptability of the software system by allowing it to evolve along with the changing needs and expectations of the stakeholders.

### Repositories

Repositories provide a standardized interface for abstracting the storage and retrieval of domain objects.
They encapsulate the logic for querying and persisting entities and aggregates, shielding the rest of the application from the details of the underlying data access mechanism.
Here are the key characteristics of a Repository:

* **Interface Definition**: A Repository is defined by an interface in the domain layer that specifies the operations and the criteria for accessing the domain objects. The interface should be based on the domain language and the domain logic, not on the technical details of the data access layer.
* **Implementation**: A Repository has an implementation in the infrastructure layer that provides the concrete data access mechanism for the domain objects. The implementation should adhere to the repository interface and should use the appropriate data access technology.
* **Work with Aggregates**: A Repository works with aggregates, which are clusters of domain objects that can be treated as a single unit. A repository should only store and retrieve whole aggregates, not individual entities or value objects.
* **Transactional Boundary**: A Repository is a transactional boundary that defines the scope and the granularity of the changes that can be made to the domain objects. A repository should ensure that any operation that affects the domain objects is atomic, consistent, isolated, and durable (ACID).
* **Abstraction and Decoupling**: Repositories enable the abstraction and decoupling of the domain layer from the data access layer by providing a common and consistent interface for accessing the domain objects, and by hiding the implementation details of the data access layer.

### Domain Services

Domain Services are a crucial component of the domain model.
They encapsulate business logic that doesn't naturally fit within a domain object.
These are not typical CRUD operations – those would belong to a Repository.
They are objects that perform actions or calculations related to the business domain.
They should be designed to work with domain entities and should follow the principles of DDD.
Domain Services are different from Application Services, which provide technical functionality.
While Domain Services encapsulate domain logic, Application Services are used by external consumers to talk to your system.
If consumers need access to CRUD operations, they would be exposed here.
The Domain Service is an additional layer that also contains domain logic, and it's part of the domain model, just like entities and value objects.
The domain service layer can also contain domain logic of its own and is as much part of the domain model as entities and value objects.
Domain Services are a key part of the domain model in DDD.
They encapsulate business logic that doesn't naturally fit within a domain object and are designed to work with domain entities.
They are different from Application Services, which provide technical functionality and are used by external consumers to interact with the system.

### Domain Events

Domain Events represent something significant that happens within the domain that is of interest to domain experts.

A Domain Event is an event that domain experts care about.
These events typically occur regardless of whether or to what extent the domain is implemented in a software system.
They are also independent of technologies.
Domain Events are used to model the behavior of the domain and to communicate changes between different parts of the system.
They allow for decoupling of entities and independent evolution of system components.
An important benefit of Domain Events is that side effects can be expressed explicitly.
For example, if you're just using Entity Framework and there has to be a reaction to some event, you would probably code whatever you need close to what triggers the event.
So the rule gets coupled, implicitly, to the code, and you have to look into the code to, hopefully, realize the rule is implemented there.
On the other hand, using Domain Events makes the concept explicit, because there's a DomainEvent and at least one DomainEventHandler involved.
For example, in the eShopOnContainers application, when an order is created, the user becomes a buyer, so an OrderStartedDomainEvent is raised and handled in the ValidateOrAddBuyerAggregateWhenOrderStartedDomainEventHandler, so the underlying concept is evident.
In short, Domain Events help you to express, explicitly, the domain rules, based in the ubiquitous language provided by the domain experts.
Domain Events also enable a better separation of concerns among classes within the same domain.
It's important to ensure that, just like a database transaction, either all the operations related to a Domain Event finish successfully or none of them do.
Domain Events are similar to messaging-style events, with one important difference.
With real messaging, message queuing, message brokers, or a service bus using AMQP, a message is always sent asynchronously and communicated across processes and machines.
However, with Domain Events, you want to raise an event from the domain operation you're currently running, but you want any side effects to occur within the same domain.
The Domain Events and their side effects (the actions triggered afterwards that are managed by event handlers) should occur almost immediately, usually in-process, and within the same domain.

### Module

A Module is a logical grouping of domain objects that helps segregate concepts and follow the ubiquitous language.
It serves as a container for a specific set of classes of an application, such as entities, value objects, aggregates, domain services, repositories, factories, or events.
A Module should be named after an important concept of the domain derived from the ubiquitous language, reflecting the role and responsibilities of the classes within it.
Here are the key characteristics of a Module:

* **Definition**: A Module is defined by a namespace or a package that contains all the related classes for that specific concept.
* **Cohesion and Coupling**: A Module has high cohesion and low coupling, meaning that the classes within a Module are closely related and work together, while the classes between different Modules are loosely related and communicate through well-defined interfaces.
* **Communication**: A Module operates in the same process and can communicate without using a network. A Module can refer directly to objects in memory synchronously by executing methods or asynchronously using some kind of mediator that is still running in the same process.
* **Bounded Context**: A Module is contained within a bounded context, which is a well-defined boundary that separates a subdomain from other subdomains and contains a consistent and coherent domain model that is aligned with the business language and processes.
* **Code Organization**: Modules help organize the code and the domain model by grouping the classes that are related to a specific concept of the domain, and by separating the classes that are related to different concepts of the domain.
* **Readability and Maintainability**: Modules help improve the readability and maintainability of the code by using a common and consistent vocabulary that reflects the domain concepts and terms, and by reducing the complexity and the dependencies between the classes.
* **Performance and Scalability**: Modules facilitate the performance and scalability of the system by reducing the memory footprint and the database access, and by allowing the Modules to be cached, shared, or distributed.
* **Agility and Adaptability**: Modules enable the agility and adaptability of the system by allowing it to evolve along with the changing needs and expectations of the stakeholders.

## Contacts

If you have questions regarding [DDD](./domain-driven-design.md)  and [DDD Modelling Process](domain-modelling-process.md), you can reach out to the [DDD Community within SAP](https://workzone.one.int.sap/site#workzone-home&/groups/o5LMntX4ueKuxgcKVSar9u/overview_page/UjJS9VFWLNJ3tZj1uxGtAV).
Please join their [MS Teams](https://teams.microsoft.com/l/team/19%3AGC89jqP1T9HUOAKM4bcxpWDiGE_lba9LbRRtHOknl8g1%40thread.tacv2/conversations?groupId=40c59874-f04d-46bd-80fb-fd7c47d050a4&tenantId=42f7676c-f455-423c-82f6-dc2d99791af7) or contact them via [Slack](https://sap-cloud-enablement.slack.com/archives/C031LU4JMUM).
They also have a [consulting hour](https://workzone.one.int.sap/site#workzone-home&/blogs/show/bCBwtxRv3l07yLE8ITeB9U) on Thursdays (08:30 CET & 16:30 CET).

## Resources

### Books

* **"DDD: Tackling Complexity in the Heart of Software" by Eric Evans:** This seminal book by Eric Evans introduced and popularized the concepts and principles of DDD. It provides a comprehensive guide to understanding and applying DDD, covering topics such as strategic design, modeling, aggregates, repositories, and more.
* **"Implementing DDD" by Vaughn Vernon:** Building upon Eric Evans' work, Vaughn Vernon delves deeper into practical implementation details of DDD. This book focuses on how to apply DDD principles and patterns in real-world scenarios, discussing topics like bounded contexts, aggregates, entities, value objects, and application services.
* **"DDD Distilled" by Vaughn Vernon:** This book by Vaughn Vernon offers a concise and practical introduction to DDD. It covers the core concepts of DDD, including the strategic design, tactical design, aggregates, entities, value objects, and repositories, providing a streamlined and accessible introduction to the subject.
* **"DDD Reference - Definitions and Pattern Summaries" by Eric Evans:** This reference book by Eric Evans is a handy companion that provides a collection of definitions, pattern summaries, and guidelines for applying DDD principles effectively. It serves as a quick reference for key concepts and patterns within DDD.
* **"Patterns, Principles, and Practices of DDD" by Scott Millett and Nick Tune:** This book provides practical insights into applying DDD in real-world projects. It covers both the foundational principles and advanced patterns of DDD, discussing topics such as context mapping, bounded contexts, aggregates, domain events, and more.

### Web

**Within SAP:**

* [DDD-Community@SAP (external)](https://github.com/SAP/curated-resources-for-domain-driven-design): This repository contains curated resources on the topic of Domain Driven Design  and Event Storming that are recommended internally at SAP and shared with the community.
* [Eureka Collaboration - Domain-Driven Design](https://wiki.one.int.sap/wiki/display/Eureka/DDD+-+Domain+Driven+Design): Industry Cloud used Domain-Driven Design extensively in their methodology.
* [DAXC DDD Kata Preparation Material](https://sap.sharepoint.com/:u:/r/sites/126487/SitePages/SelfStudy-Domain-Driven-Design-and-Event-Storming.aspx?csf=1&web=1&e=g3ytWm): This page contains the material as preparation for the DDD Kata, which is part of DAXC Curriculumn.

**Additional DDD Resources:**

* [DDD Community](https://dddcommunity.org/): A community-driven website dedicated to sharing knowledge and resources on DDD. It offers articles, case studies, videos, and forums to connect with other DDD practitioners.
* [DDD Reference](https://domainlanguage.com/ddd/): Eric Evans' website dedicated to DDD resources. It includes articles, papers, and definitions of key DDD concepts and patterns.
* [DDD Distilled Cheat Sheet](https://leanpub.com/ddd-distro): A concise cheat sheet by Vaughn Vernon summarizing the key concepts and patterns of DDD in a single-page reference.
* [DDD Slack Channel](https://domainlanguage.com/slack/): A Slack community focused on DDD discussions, Q&A, and knowledge sharing. It provides an opportunity to connect with DDD practitioners from around the world.
* [DDD in Practice: Pluralsight Course by Julie Lerman](https://www.pluralsight.com/courses/domain-driven-design-in-practice): An online video course on Pluralsight by Julie Lerman, covering the practical application of DDD principles using real-world examples and demonstrations.
* [Software Engineering Radio: DDD Episode](https://www.se-radio.net/2007/08/episode-97-eric-evans-on-domain-driven-design/): A podcast episode featuring an interview with Eric Evans, the author of "DDD: Tackling Complexity in the Heart of Software," where he discusses the key concepts and benefits of DDD.
* [DDD Europe Conference Videos](https://www.youtube.com/c/DDDEurope): A YouTube channel featuring recorded talks from DDD Europe conferences. It covers a wide range of DDD topics, case studies, and insights from industry experts.
* [DDD Weekly Newsletter](https://dddweekly.com/): A curated newsletter delivering weekly updates on DDD-related articles, blog posts, events, and resources from around the web.
* [Pluralsight: Learn DDD](https://app.pluralsight.com/paths/skill/domain-driven-design): Understand the philosophy and major design patterns that underlie the DDD approach to software architecture. Focus on the importance of the core domain and domain logic of your business.
* [EventStorming](https://www.eventstorming.com/): EventStorming is a flexible workshop format for collaborative exploration of complex business domains.
* [What is Domain-Driven Design (DDD) | Pros & Cons | Codez Up](https://codezup.com/what-is-domain-driven-design-ddd-pros-cons/): An article discussing the pros and cons of Domain-Driven Design.
* [The advantages and disadvantages of domain-driven design - Appdevcon](https://appdevcon.nl/the-pros-and-cons-of-domain-driven-design/): A resource outlining the advantages and disadvantages of Domain-Driven Design.
* [Domain-Driven Design: What is it and how do you use it? - Airbrake](https://blog.airbrake.io/blog/software-design/domain-driven-design/): An introduction to Domain-Driven Design and its practical applications.
* [Domain Driven Design disadvantages? - Stack Overflow](https://stackoverflow.com/questions/5167756/domain-driven-design-disadvantages): A Stack Overflow thread discussing potential disadvantages of Domain-Driven Design.
* [An Introduction to Domain Driven Design and Its Benefits](https://dzone.com/articles/an-introduction-to-domain-driven-design-and-its-be): An article providing an introduction to Domain-Driven Design and highlighting its benefits.

**Strategic Design:**

1. [Why Strategic Design Matters in Domain-Driven Design](https://towardsdev.com/why-strategic-design-matters-in-domain-driven-design-5ea56b0ee219): An article discussing the importance of strategic design in Domain-Driven Design.
2. [What is Strategic Design? - DDD - The Domain Driven Design](https://thedomaindrivendesign.io/what-is-strategic-design/): An explanation of strategic design in the context of Domain-Driven Design.
3. [DDD Part 1: Strategic Domain-Driven Design | Vaadin](https://vaadin.com/blog/ddd-part-1-strategic-domain-driven-design): A blog post on strategic domain-driven design as part of the Vaadin DDD series.
4. [Strategic Domain Driven Design | AOE Technology Radar](https://www.aoe.com/techradar/methods-and-patterns/strategic-domain-driven-design.html): AOE's insights into strategic domain-driven design as part of their Technology Radar.
5. [DDD Model Integrity Patterns - Medium](https://rafaelritter.medium.com/ddd-model-integrity-patterns-36d0e8ac9561): An article on Medium discussing domain-driven design model integrity patterns.
6. [Domain-Driven Design: Unleashing the Power of Strategic Software Design - Medium](https://medium.com/bimar-teknoloji/domain-driven-design-unleashing-the-power-of-strategic-software-design-e7d7e8f637c2): Medium post on the power of strategic software design in Domain-Driven Design.
7. [I. Strategic Design - Learning Domain-Driven Design [Book] - O'Reilly Media](https://www.oreilly.com/library/view/learning-domain-driven-design/9781098100124/part01.html): Chapter on strategic design from the book "Learning Domain-Driven Design."
8. [Domain-Driven Design: Unleashing the Power of Strategic... - Medium](https://medium.com/bimar-teknoloji/domain-driven-design-unleashing-the-power-of-strategic-software-design-e7d7e8f637c2): A Medium article exploring the power of strategic software design in DDD.
9. [The Open Group - DDD Strategic Patterns](https://pubs.opengroup.org/architecture/o-aa-standard/DDD-strategic-patterns.html): The Open Group's publication on DDD strategic patterns.
10. [Wikipedia - Domain-Driven Design](https://en.wikipedia.org/wiki/Domain-driven_design): Wikipedia's page on Domain-Driven Design, covering various aspects, including strategic design.
11. [Microsoft Learn - Domain Analysis](https://learn.microsoft.com/en-us/azure/architecture/microservices/model/domain-analysis): Microsoft Learn's guide on domain analysis in the context of microservices.

**Tactical Design:**

1. [Tactical Domain-Driven Design - DEV Community](https://dev.to/peholmst/tactical-domain-driven-design-17dp): An article on DEV Community discussing tactical Domain-Driven Design.
2. [Using tactical DDD to design microservices - Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/microservices/model/tactical-ddd): Microsoft Learn's guide on using tactical Domain-Driven Design for designing microservices.
3. [What is Tactical Design? - DDD - The Domain Driven Design](https://thedomaindrivendesign.io/what-is-tactical-design/): An explanation of tactical design in the context of Domain-Driven Design.
4. [DDD Part 2: Tactical Domain-Driven Design | Vaadin](https://vaadin.com/blog/ddd-part-2-tactical-domain-driven-design): Part 2 of Vaadin's blog series on Tactical Domain-Driven Design.
5. [What Is Tactical Design – PrecisionOutdoors](https://precisionoutdoors.org/what-is-tactical-design/): An article exploring the concept of tactical design, particularly in a different context.
6. [The Two Sides of Domain-Driven Design (DDD) - Gorodinski](http://gorodinski.com/blog/2013/03/11/the-two-sides-of-domain-driven-design/): A blog post discussing the two sides of Domain-Driven Design, which may include tactical aspects.

**Bounded Context:**

1. [DDD Strategic Patterns: How to Define Bounded Contexts](https://dzone.com/articles/ddd-strategic-patterns-how-to-define-bounded-conte)
2. [BoundedContext - Martin Fowler](https://martinfowler.com/bliki/BoundedContext.html)
3. [DDD und Bounded Context: Eigentlich ganz einfach, oder ...](https://www.heise.de/hintergrund/Domain-driven-Design-und-Bounded-Context-Eigentlich-ganz-einfach-oder-4634258.html)
4. [DDD: Understanding Bounded Context and the Context Map](https://www.developer.com/design/domain-driven-design-understanding-bounded-context-and-the-context-map/)
5. [Explaining Bounded Context in Microservices](https://www.kindsonthegenius.com/microservices/explaining-bounded-context-in-microservices/)
6. [Bounded Context - thedomaindrivendesign.io](https://thedomaindrivendesign.io/bounded-context/)

**Ubiquitous Language:**

1. [The Importance of Ubiquitous Language - VMware](https://tanzu.vmware.com/developer/blog/ubiquitous-language/)
2. [What is Ubiquitous Language? | Agile Alliance](https://www.agilealliance.org/glossary/ubiquitous-language/)
3. [Developing the ubiquitous language - DDD - The Domain Driven Design](https://thedomaindrivendesign.io/developing-the-ubiquitous-language/)
4. [UbiquitousLanguage - Martin Fowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
5. [What Is a Ubiquitous Language?](https://wonderus.app/what-is-a-ubiquitous-language/)

**Aggregate:**

1. [What Is an Aggregate? | DDD in PHP - Packt Subscription](https://subscription.packtpub.com/book/application-development/9781787284944/8/ch08lvl1sec56/what-is-an-aggregate)
2. [What Are DDD Aggregates? - James Hickey](https://www.jamesmichaelhickey.com/domain-driven-design-aggregates/)
3. [DDD_Aggregate - Martin Fowler](https://martinfowler.com/bliki/DDD_Aggregate.html)
4. [Difference between an entity and an aggregate in domain driven design](https://stackoverflow.com/questions/32353835/difference-between-an-entity-and-an-aggregate-in-domain-driven-design)
5. [DDD Aggregates](https://dzone.com/articles/domain-driven-design-aggregate)
6. [DDD-Oriented Microservice - Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/ddd-oriented-microservice)
7. [Exploring the Power of Aggregates in DDD and Clean Architecture - Medium](https://medium.com/@edin.sahbaz/exploring-the-power-of-aggregates-in-domain-driven-design-and-clean-architecture-6408d6128d3b)
8. [Demystifying the DDD Aggregate - Medium](https://medium.com/codex/demystifying-the-ddd-aggregate-c93e605b22ae)
9. [Aggregates, Entities and Value Objects in DDD - InfoQ](https://www.infoq.com/news/2015/01/aggregates-value-objects-ddd/)
10. [What Are DDD Aggregates? - James Hickey](https://www.jamesmichaelhickey.com/domain-driven-design-aggregates/)

**Entities:**

1. [The meaning of "entity" in DDD](https://stackoverflow.com/questions/57367017/the-meaning-of-entity-in-domain-driven-design)
2. [DDD: Entities, Value Objects, and How To Distinguish Them](https://blog.jannikwempe.com/domain-driven-design-entities-value-objects)
3. [Relational database entities vs. DDD entities](https://www.cockroachlabs.com/blog/relational-database-entities/)
4. [DDD: Entities, Value Objects and Services (chapter 5.1)](https://dev.to/ielgohary/domain-driven-design-entities-value-objects-and-services-chapter-51-22cm)

**Value Objects:**

1. [Modeling Complex Domains with Aggregates, Entities, and Value Objects](https://towardsdev.com/modeling-complex-domains-with-aggregates-entities-and-value-objects-42600f880a1b)
2. [DDD: Entities, Value Objects, and How To Distinguish Them](https://blog.jannikwempe.com/domain-driven-design-entities-value-objects)
3. [DDD Building Blocks: Value Object — Domain Centric](https://domaincentric.net/blog/ddd-building-blocks-in-php-value-object/)
4. [Value object (DDD series part 6)](https://kisztof.medium.com/value-object-ddd-series-part-6-3b330f021ac2)
5. [DDD C# - Pluralsight](https://www.pluralsight.com/blog/software-development/domain-driven-design-csharp)

**Repositories:**

1. [Repository – DDD: A Practitioner's Guide](https://ddd-practitioners.com/home/glossary/domain-driven-design/tactical-design/repository/): A comprehensive guide on repositories in DDD from the DDD Practitioners website.
2. [DDD - Wikipedia](https://en.wikipedia.org/wiki/Domain-driven_design): Wikipedia's overview of DDD, covering various aspects including tactical design patterns like repositories.
3. [What is repository in DDD? – ITExpertly.com](https://itexpertly.com/what-is-repository-in-domain-driven-design/): An article explaining the concept of a repository in DDD.
4. [DDD, part 5 — Repository - Medium](https://svatasimara.medium.com/domain-driven-design-part-5-repository-d5ad32b2e06f): Part 5 of a series on DDD, focusing on the repository pattern.
5. [ddd repositories - domain driven design repository - Stack Overflow](https://stackoverflow.com/questions/66891936/domain-driven-design-repository): Stack Overflow discussion on repositories in DDD.
6. [Pros and cons of DDD Repositories - Stack Overflow](https://stackoverflow.com/questions/1975657/pros-and-cons-of-ddd-repositories): Stack Overflow discussion highlighting the pros and cons of using repositories in DDD.
7. [Designing the infrastructure persistence layer - .NET](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design): Microsoft's guide on designing the infrastructure persistence layer in .NET, which includes considerations for DDD repositories.
8. [Stack Exchange: Which layer do DDD repositories belong to](https://softwareengineering.stackexchange.com/questions/396151/which-layer-do-ddd-repositories-belong-to): A discussion on the appropriate layer for placing DDD repositories.
9. [Stack Overflow: Which layer should repositories go in](https://stackoverflow.com/questions/3499119/which-layer-should-repositories-go-in): Stack Overflow discussion on the layering of repositories in DDD.

**Domain Services:**

1. [Designing a DDD-oriented microservice - .NET | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/ddd-oriented-microservice): A guide by Microsoft Learn on designing a DDD-oriented microservice in .NET.
2. [Articles Tutorials | AspNet Boilerplate](https://aspnetboilerplate.com/Pages/Documents/Domain-Services): Documentation on domain services from AspNet Boilerplate, offering articles and tutorials.
3. [GitHub - dddshelf/ddd: Domain Driven Design PHP helper classes](https://github.com/dddshelf/ddd): A GitHub repository for "ddd," featuring Domain Driven Design PHP helper classes.
4. [Using tactical DDD to design microservices - Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/microservices/model/tactical-ddd): Microsoft's guide on using tactical DDD to design microservices in the Azure Architecture Center.

**Domain Events:**

1. [How to succeed with domain events – Domain-driven Design](https://ddd-practitioners.com/2023/03/09/how-to-succeed-with-domain-events/): A detailed article providing insights into succeeding with domain events in the context of Domain-Driven Design.
2. [Domain-driven design - Wikipedia](https://en.wikipedia.org/wiki/Domain-driven_design): Wikipedia's entry on Domain-Driven Design, offering a general overview of the concept.
3. [Domain Driven Design: What is the difference between Domain Events vs. Event Sourcing](https://tigosoftware.com/domain-driven-design-what-difference-between-domain-events-vs-event-sourcing): An article explaining the difference between Domain Events and Event Sourcing in Domain-Driven Design.
4. [Domain events: Design and implementation - .NET | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/domain-events-design-implementation): Microsoft Learn's guide on the design and implementation of domain events in .NET within the context of microservices and Domain-Driven Design.
5. [Domain Event pattern · Microservices Architecture](https://badia-kharroubi.gitbooks.io/microservices-architecture/content/patterns/tactical-patterns/domain-event-pattern.html): A resource explaining the Domain Event pattern in the context of microservices architecture.
6. [Demystifying Domain-Driven Design (DDD) in Modern Software Architecture](https://blog.bitsrc.io/demystifying-domain-driven-design-ddd-in-modern-software-architecture-b57e27c210f7): An article demystifying Domain-Driven Design in modern software architecture, including domain events.
7. [What Are Domain Events?](https://dzone.com/articles/what-are-domain-events): An article providing insights into what domain events are and their significance.
8. [SampleDDD on GitHub](https://github.com/Sajadmetall/SampleDDD/tree/4e55cb048f6c26773e9a56976496661545624b15/README.md): GitHub repository (SampleDDD) containing information related to Domain-Driven Design and domain events.

**Modules:**

1. [What are Modules in Domain Driven Design? | Culttt](https://culttt.com/2014/12/10/modules-domain-driven-design/): An article exploring the concept of modules in Domain-Driven Design.
2. [Module Domain Driven Design - iSAQB CPSA Advanced Level](https://software-architecture-camp.com/isaqb-advanced-level/module-ddd-domain-driven-design/): Information on modules in Domain-Driven Design as part of the iSAQB CPSA Advanced Level.

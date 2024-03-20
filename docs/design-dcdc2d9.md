<!-- loiodcdc2d9e48f042c3ba23e8656df921e9 -->

# Design



<a name="loiodcdc2d9e48f042c3ba23e8656df921e9__section_qf2_bqh_1zb"/>

## CAP Design Principles

SAP Cloud Application Programming Model \(CAP\) focuses on the domain of the application, by capturing domain knowledge and intent instead of imperative coding. This means:

-   Close collaboration of developers and domain experts in domain modeling.

-   Out-of-the-box implementations for best practices and recurring tasks.

-   Platform-agnostic approach to avoid lock-ins, hence protecting investments.




<a name="loiodcdc2d9e48f042c3ba23e8656df921e9__section_pgh_rsh_1zb"/>

## Agnostic Design

CAP avoids technology lock-ins through higher-level concepts and APIs, which abstract low-level platform features and protocols to a large extent. In particular, this applies to:

-   Platform-specific deployment approaches and techniques

-   Platform-specific identity providers and authentication strategies

-   Onboarding and offboarding of tenants in Software-as-a-Service \(SaaS\) solutions and tenant isolation

-   Synchronous protocols like REST, OData, or GraphQL

-   Asynchronous channels and brokers like SAP Event Mesh, Message Queue, or Kafka 

-   Different database technologies including SQL and NoSQL


These abstractions allow CAP to quickly adapt to new emerging technologies or platforms, without affecting the application code.



<a name="loiodcdc2d9e48f042c3ba23e8656df921e9__section_lfp_ssh_1zb"/>

## Open and Opinionated Design

While CAP certainly gives opinionated guidance, it does this without sacrificing openness and flexibility. You as a developer stay in control of which tools or technologies to choose, or which architecture patterns to follow.

-   All abstractions follow a glass-box pattern that allows unrestricted access to lower-level things, if necessary.

-   Best Practices served out of the box with generic solutions for many recurring tasks.

-   Out-of-the-box support for SAP Fiori and SAP HANA.

-   Dedicated tools support provided in SAP Business Application Studio, and Visual Studio Code or Eclipse.




<a name="loiodcdc2d9e48f042c3ba23e8656df921e9__section_tgs_wsh_1zb"/>

## Domain-Driven Design

CAP uses Core Data Services as its ubiquitous modelling language, with Core Data Service Aspects separating core domain aspects from generic aspects.Core Data Service's human-readable nature fosters collaboration of developers and domain experts.

As Core Data Service models are used to fuel generic providers — the database as well as application services — CAP ensures that the models are applied in the implementation. And as coding is minimized you can more easily refine and revise their models, without having to refactor large boilerplate code bases.


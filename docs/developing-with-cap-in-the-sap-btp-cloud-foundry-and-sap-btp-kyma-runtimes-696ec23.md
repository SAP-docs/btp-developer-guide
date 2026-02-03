<!-- loio696ec2328d02468eb1455c280e1eb969 -->

# Developing with CAP in the SAP BTP, Cloud Foundry and SAP BTP, Kyma Runtimes



<a name="loio696ec2328d02468eb1455c280e1eb969__section_w2m_ksx_lxb"/>

## Overview

The SAP Cloud Application Programming Model \(CAP\) is a framework of languages, libraries, and tools for building enterprise-grade services and applications. It guides developers along a path of proven best practices and a great wealth of out-of-the-box solutions to recurring tasks.

CAP-based projects benefit from a primary focus on domain. Instead of delving into overly technical disciplines, CAP focuses on accelerated development and safeguarding investments in a world of rapidly changing cloud technologies.

The following graphic shows that the CAP framework features a mix of proven and broadly adopted open-source and SAP technologies:

![Diagram of CAP framework components and their integration.](images/CAP_Overview_7e017ac.png)

On top of open-source technologies, CAP mainly adds:

-   Core Data Services \(CDS\) as its universal modeling language for both domain models and service definitions.

-   Service SDKs and runtimes for Node.js and Java, offering libraries to implement and consume services as well as generic provider implementations serving many requests automatically.


These are the CAP development profiles you can use:

-   Development profile: use mocked services for local testing and development.

    You can begin building SAP Cloud Application Programming \(CAP\) applications locally without needing a subscription or initial setup in SAP BTP. This approach offers several advantages during the early stages of development:

    -   Rapid Prototyping

        You can quickly design and test domain models and services locally, enabling faster iteration and feedback cycles.

    -   Deferred Integration

        You can postpone the integration with SAP BTP services until later stages, allowing you to focus on core functionality first.

    -   Mocked Platform Services

        The CAP development profile includes mocked variants of some SAP BTP services dealing with authentication, database, messaging, and application gateway. These mocks allow applications to run locally without requiring the application to be deployed to SAP BTP.


-   Hybrid profile: local development and testing using selected real services

    Over time, you can add things gradually, only when they're needed. For example, you can move ahead to running your applications in close-to-productive setups for integration tests and delivery, without any change in models or code:

    -   Run locally, but bind to real services \(for example, SAP HANA Cloud, and the Destination service\) using cds bind or a local default-env.json that simulates Cloud Foundry or Kyma service bindings.
    -   Great for integration tests \(for example, real SAP HANA Cloud schema, real authorization flows\) before you deploy.

-   Production profile: use SAP BTP services and deploy the application to SAP BTP.

    Run in SAP BTP, Cloud Foundry or SAP BTP, Kyma runtime with platform-managed service bindings and production-grade settings.

    -   Real service instances \(SAP HANA Cloud, Destination services, and others\) are bound by the platform.

    -   Production configuration for logging, security, scaling, and multitenancy.

    -   Database migrations done via cds deploy \(for example, to SAP HANA Cloud\).



See [Grow as You Go](https://cap.cloud.sap/docs/get-started/grow-as-you-go) in the CAP documentation.

**Related Information**  


[Strengths and Benefits of the Runtimes and Their Programming Models](strengths-and-benefits-of-the-runtimes-and-their-programming-models-86688d1.md "")

[Explore](explore-03139be.md "")

[Discover](discover-7eae382.md "")

[Design](design-6bb7339.md "")

[Deliver](deliver-3efbd5b.md "")

[Run and Scale](run-and-scale-fcb51b5.md "")

[Tutorials and Reference Sample for Full-Stack Multitenant SaaS Applications for Partners](tutorials-and-reference-sample-for-full-stack-multitenant-saas-applications-for-partners-11d9894.md " 		")

[Tutorials for SAP Cloud Application Programming Model](tutorials-for-sap-cloud-application-programming-model-eb7420a.md "")


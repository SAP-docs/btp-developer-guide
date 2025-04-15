<!-- loioba26ec41130d4835aef2265ad3d3704e -->

# SAP BTP Developer’s Guide

The SAP BTP Developer’s Guide is the starting point for developing a business application on SAP BTP. It contains **recommendations** and **best practices** that give you an overview of what you should consider when working on development projects on SAP BTP. It also contains links to step-by-step instructions when required.



<a name="loioba26ec41130d4835aef2265ad3d3704e__section_s1p_yzv_rcc"/>

## Is This Guide for You?

If you're an **architect or a development project lead**, this guide helps you to plan the architecture of your application and the services on SAP BTP you can use to achieve your goal.

If you're a **developer**, this guide helps you to define the correct methodologies and tools for your development project.

If you're an **SAP partner**, this guide helps you to set up SAP BTP for developing and running applications and services for your customers.

> ### Note:  
> If you're an **administrator**, you have to set up the correct organizational structure to create an account and security model. In this case, use the [SAP BTP Administrator's Guide](https://help.sap.com/docs/btp/best-practices/best-practices-for-sap-btp?version=Cloud).

> ### Note:  
> This guide is targeted at customers who want to run and use applications in a production environment. If you're an SAP BTP trial user, you might still find that some information in this guide is useful. Check out the following page for more details about trial accounts: [Trial Accounts and Free Tier](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/046f127f2a614438b616ccfc575fdb16.html "Explore the different options for trying out SAP BTP.") :arrow_upper_right:. Please note that the services available in the trial version differ from the ones in the enterprise version.



<a name="loioba26ec41130d4835aef2265ad3d3704e__section_vlt_r4f_xcc"/>

## Prerequisites

If you're new to SAP BTP, read:

-   [SAP Business Technology Platform](https://www.sap.com/products/technology-platform/what-is-sap-business-technology-platform.html)

    SAP BTP is a cloud platform that brings together application development, automation, data management, analytics and planning, integration, and AI capabilities into one unified environment optimized for SAP applications. It offers:

    -   An intuitive, modern development environment for both, professional IT and citizen and business developers,

    -   Built-in data models, integrations, workflows, app templates, and AI business services

    -   Self-service data discovery, modeling, planning, and analytics for business users in a governed environment


-   [SAP BTP Guidance Framework](https://help.sap.com/docs/sap-btp-guidance-framework/guidance-framework/what-is-sap-btp-guidance-framework)

    This is the central access point for architects, developers, and administrators to build and run enterprise-grade solutions on SAP BTP. It comprises decision guides, reference architectures, methodologies, recommendations, and DevOps principles.

-   [Basic Platform Concepts](https://help.sap.com/docs/btp/sap-business-technology-platform/btp-basic-platform-concepts?version=Cloud)

    Contains regions, runtimes, accounts, members, quotas, capabilities and links to in-depth explanations.

-   [Getting Started Checklist](https://help.sap.com/docs/BTP/df50977d8bfa4c9a8a063ddb37113c43/cbd76632d8aa4cb7bbf175d7607db463.html?locale=en-US&state=PRODUCTION&version=Cloud)

    Explains your responsibilities and SAP's responsibilities when it comes to application lifecycle management.

-   [SAP BTP Administrator's Guide](https://help.sap.com/docs/btp/best-practices/best-practices-for-sap-btp?version=Cloud)

    This guide helps you plan and set up your landscape and your lifecycle management for running applications on SAP Business Technology Platform \(SAP BTP\). It's part of the SAP BTP Guidance Framework and contains recommendations for planning development projects – from setting up the correct organizational structure to creating an account and security model, to operating applications.

-   [SAP Discovery Center](https://discovery-center.cloud.sap/index.html)

    Helps you turn your data into business value with SAP BTP. In the SAP Discovery Center you can find end-to-end scenarios, called missions, the Service Catalog of SAP BTP, and reference architectures.




<a name="loioba26ec41130d4835aef2265ad3d3704e__section_tf1_xml_s2b"/>

## How to Use This Guide

Use the SAP BTP Developer’s Guide to help you implement business applications on SAP BTP. This guide is part of the SAP BTP Guidance Framework and explains the building blocks for developing, delivering, and integrating business applications.

Development projects for business applications have similar characteristics. Standardized development guidance is driving developer efficiency.

Based on the experiences of successful business applications, this guide condenses best practices and technologies that can be safely recommended to you. These recommendations are structured following the design-led development phases:

![](images/Development_Process_in_the_SAP_BTP_Developer_s_Guide_f52c607.png)

-   **[Explore](explore-03139be.md)**

    Identify the business opportunity and set up the roles and responsibilities in your team.

-   **[Discover](discover-7eae382.md)**

    -   [Identifying Required Use Cases](identifying-required-use-cases-98e01cf.md)

        Understand your end users, their working methods, and their needs in more depth.

    -   [Understanding Available Technology](understanding-available-technology-c1f21a4.md#loioc1f21a47f38b467997436c13fe773513)

        -   [Development Use Cases](understanding-available-technology-c1f21a4.md#loio4efd0bc86ade42c28bf4c4c8dbc4451b)

            Get to know the use case patterns that can be implemented on SAP BTP.

        -   [Business Application Services](understanding-available-technology-c1f21a4.md#loiof3641a5635504edab2c6bb84fa86a42a)

            Explore the comprehensive set of tools and services that allow you to keep the pace when developing your application and at the same time benefit from future innovations in SAP BTP.



-   **[Design](design-6bb7339.md)**

    -   [User Experience Design](user-experience-design-323bd93.md)

        Design the user experience of your application to provide good usability.

    -   [Technology Design](technology-design-a5b8129.md)

        Use domain-driven design to create an application that is modularized and has shorter innovation cycles and a clearer focus.


-   **[Deliver](deliver-3efbd5b.md)**

    -   [Set Up](set-up-3b774f8.md)

        Before you begin developing your applications, make sure your landscape setup is appropriate for managing their lifecycles.

    -   [Develop](develop-and-build/develop-7e30686.md)

        Develop your application by following the recommendations outlined in this section about the two programming models, the numerous programming languages, the respective development tools and also about aspects such as multitenancy, security, extensibility and others.


-   **[Run and Scale](run-and-scale-fcb51b5.md)**

    Get constant feedback from your users, optimize the application based on this feedback, and operate the application using the services and capabilities SAP BTP offers.

-   **[Programming Model Specifics](programming-model-specifics-cc37b7a.md)**

    -   [ABAP Cloud](abap-cloud-9aaaf65.md)

        ABAP Cloud reflects the modern way to develop ABAP. It allows you to build lifecycle-stable and cloud-ready business applications, services, and extensions.

    -   [SAP Cloud Application Programming Model \(CAP\)](sap-cloud-application-programming-model-cap-696ec23.md)

        The SAP Cloud Application Programming Model \(CAP\) is a framework of languages, libraries, and tools for building enterprise-grade services and applications. It supports Java \(with Spring Boot\), JavaScript, and TypeScript \(with Node.js\), which are some of the most widely adopted languages. CAP guides developers along a path of proven best practices and a great wealth of out-of-the-box solutions to recurring tasks.





<a name="loioba26ec41130d4835aef2265ad3d3704e__section_mfx_qws_zxb"/>

## Contribute to the SAP BTP Developer’s Guide

> ### Tip:  
> The English version of this guide is open for contributions and feedback using GitHub. This allows you to get in contact with responsible authors of SAP Help Portal pages and the development team to discuss documentation-related issues. To contribute to this guide, or to provide feedback, choose the corresponding option on SAP Help Portal:
> 
> -   *Feedback* \> *Create issue*: Provide feedback about a documentation page. This option opens an issue on GitHub.
> 
> -   *Feedback* \> *Edit page*: Contribute to a documentation page. This option opens a pull request on GitHub.
> 
> 
> You need a GitHub account to use these options.
> 
> More information:
> 
> -   [Contribution Guidelines](https://help.sap.com/docs/open-documentation-initiative/contribution-guidelines/readme.html)
> 
> -   [Introduction Video](https://www.youtube.com/watch?v=WJ0oarMlVW4)
> 
> -   [Introduction Blog Post](https://blogs.sap.com/2021/11/29/sap-btp-documentation-goes-github-new-collaboration-process/)


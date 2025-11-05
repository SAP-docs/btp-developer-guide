<!-- loio6bb733981248482e86559bc52a87aaff -->

# Design

Good user experience \(UX\) goes beyond aesthetics and can have substantial business benefits, both financially and in overall efficiency. A great UX can improve productivity, enhance data quality, reduce training costs, and decrease the number of change requests.

A positive UX boosts user satisfaction, customer loyalty, and overall application adoption. Users are more likely to embrace an application that is intuitive and easy to use.

However, achieving a good UX involves overcoming several common challenges. Users often struggle with finding information, dealing with scattered data, excessive clicks, poor data entry interfaces, and unhelpful error messages. Beyond design, bad performance and unhelpful data visualization can also frustrate users.

The essential approach to designing a good application is design thinking, which emphasizes understanding users' needs through observation and feedback. Iteration is key: quickly sketch prototypes, gather user feedback, and refine your designs before moving to development. This ensures that the final product truly meets users' needs and optimizes resources effectively.

For organizations working with multiple applications, consistency is crucial. Users expect uniform visual design and interactions, easy access and navigation between applications, and common functions readily available. To achieve this, a design system is necessary. It ensures consistent user experience across various channels such as desktop, mobile, and so on.

In large-scale development, you also need robust frameworks, libraries, and user experience integration runtimes to manage hundreds of applications efficiently. Proper authorization tools are essential to control access for an extensive user base.

The SAP Fiori design system along with its enabling UI tools and technologies gives you the above: a comprehensive design system for web and mobile, along with a suite of development tools and UI frameworks, enabling SAP to provide a consistent UX with good usability across all SAP products, and enabling you to do the same for your applications. Using SAP's design system enables you to bring together business value, modern technology and excellent UX, thus benefitting business and users alike.

Find out more about user experience design and technology design in the next sections:

-   [User Experience Design](user-experience-design-323bd93.md)

-   [Technology Design](technology-design-a5b8129.md)




<a name="loio6bb733981248482e86559bc52a87aaff__section_fvz_33k_bzb"/>

## Typical Development Use Case Patterns

We recommend implementing the following use case patterns on SAP BTP:

-   Automate processes across backend systems

    This pattern provides low code/no code capabilities to automate processes and is meant for business experts and developers.

-   Build web and mobile applications

    This pattern provides mobile-native and web development capabilities and is meant for business experts and developers.

-   Develop full-stack applications

    This pattern is meant for professional developers and has the following flavors:

    -   Full-stack single-tenant applications

        This pattern is meant for customers and implementation partners enabling them to develop full-stack applications on SAP BTP.

    -   Full-stack multitenant Software-as-a-Service \(SaaS\) applications for partners that are independent software vendors

        This pattern is meant for SAP partners enabling them to develop full-stack SaaS applications on the SAP BTP and to distribute these applications to their customers. Partners can easily onboard multiple customers \(tenants\) onto a single application with strictly separated data. This approach dramatically reduces the total cost of ownership at cloud scale.

        The Poetry Slam Manager partner reference application on GitHub provides a comprehensive example to build, deploy, and run such a scalable SaaS solution. See [Tutorials and Reference Sample for Full-Stack Multitenant SaaS Applications for Partners](tutorials-and-reference-sample-for-full-stack-multitenant-saas-applications-for-partners-11d9894.md) and [Partner Reference Application 'Poetry Slam Manager'](https://github.com/SAP-samples/partner-reference-application/).

    -   Tenant-specific extensions for partners and customers to add or modify features in multitenant SaaS solutions, such as the Poetry Slam Manager, without affecting the core product used by all tenants.

        The Partner Reference Application Extension "Catering Management" demonstrates a robust framework for delivering highly-tailored functionalities for specific customers and industries, using SAP BTP and CAP extensibility as a foundation. See [Tutorials and Reference Sample for Custom Extension of a Full-Stack Multitenant SaaS Applications for Partners](https://help.sap.com/docs/btp/btp-developers-guide/tutorials-and-reference-sample-for-full-stack-multitenant-saas-applications-for-partners?locale=en-US&state=PRODUCTION&version=Cloud) and [Partner Reference Application 'Catering Management'](https://github.com/SAP-samples/partner-reference-application-extension).





<a name="loio6bb733981248482e86559bc52a87aaff__section_qf2_bqh_1zb"/>

## CAP Design Principles

SAP Cloud Application Programming Model \(CAP\) focuses on the domain of the application, by capturing domain knowledge and intent instead of imperative coding. This means:

-   Close collaboration of developers and domain experts in domain modeling.

-   Out-of-the-box implementations for best practices and recurring tasks.

-   Platform-agnostic approach to avoid lock-ins, hence protecting investments.




<a name="loio6bb733981248482e86559bc52a87aaff__section_pgh_rsh_1zb"/>

## Agnostic Design

CAP avoids technology lock-ins through higher-level concepts and APIs, which abstract low-level platform features and protocols to a large extent. In particular, this applies to:

-   Platform-specific deployment approaches and techniques

-   Platform-specific identity providers and authentication strategies

-   Onboarding and offboarding of tenants in Software-as-a-Service \(SaaS\) solutions and tenant isolation

-   Synchronous protocols like REST, OData, or GraphQL

-   Asynchronous channels and brokers like SAP Event Mesh, Message Queue, or Kafka 

-   Different database technologies including SQL and NoSQL


These abstractions allow CAP to quickly adapt to new emerging technologies or platforms, without affecting the application code.



<a name="loio6bb733981248482e86559bc52a87aaff__section_lfp_ssh_1zb"/>

## Open and Opinionated Design

While CAP certainly gives opinionated guidance, it does this without sacrificing openness and flexibility. You as a developer stay in control of which tools or technologies to choose, or which architecture patterns to follow.

-   All abstractions follow a glass-box pattern that allows unrestricted access to lower-level things, if necessary.

-   Best Practices served out of the box with generic solutions for many recurring tasks.

-   Out-of-the-box support for SAP Fiori and SAP HANA.

-   Dedicated tools support provided in SAP Business Application Studio, and Visual Studio Code or Eclipse.




<a name="loio6bb733981248482e86559bc52a87aaff__section_tgs_wsh_1zb"/>

## Domain-Driven Design

CAP uses Core Data Services as its ubiquitous modelling language, with Core Data Service Aspects separating core domain aspects from generic aspects. Core Data Service's human-readable nature fosters collaboration of developers and domain experts.

As Core Data Service models are used to fuel generic providers — the database as well as application services — CAP ensures that the models are applied in the implementation. And as coding is minimized you can more easily refine and revise their models, without having to refactor large boilerplate code bases.



<a name="loio6bb733981248482e86559bc52a87aaff__section_r41_52c_dgc"/>

## Security Considerations in the Design Phase

In the design phase, you define the user experience and technical architecture of your application. This includes applying domain-driven design principles and following the best practices of the programming model you have chosen, CAP or ABAP Cloud, to create modular, user-centric solutions. Prioritizing security at this stage ensures your application is built on a resilient architecture that protects sensitive data and supports regulatory compliance.

Design decisions shape how users interact with your application and how its internal components communicate. For example, a retail company designing an e-commerce platform might implement a secure checkout process that enforces user authentication and encrypts payment data. By embedding security practices early—such as defining role-based access controls, securing APIs, and validating input—you reduce the risk of vulnerabilities being introduced into the system.

Proactively addressing security in the design phase not only streamlines compliance with regulations like the GDPR but also builds user trust and reduces the cost of future remediation.

The following table summarizes the security guidelines you need to be familiar with:

**Designing Secure Applications from the Ground Up**


<table>
<tr>
<th valign="top">

Security Guideline

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

Design Secure User Interfaces

</td>
<td valign="top">

Incorporate security features like secure authentication and input validation when designing the UI using SAP Fiori.

</td>
</tr>
<tr>
<td valign="top">

Define Access Control Models

</td>
<td valign="top">

Securely authenticate users and technical clients with methods such as OpenID Connect and OAuth. Design role-based access controls \(RBAC\) and attribute-based access control \(ABAC\) in domain models to restrict data access.

</td>
</tr>
<tr>
<td valign="top">

Secure API and Service Interactions

</td>
<td valign="top">

Design APIs with authentication \(for example, OAuth\) and encryption \(for example, TLS\) to protect data exchanges.

</td>
</tr>
<tr>
<td valign="top">

Plan for Secure Extensibility

</td>
<td valign="top">

Ensure extensions \(for example, custom logic\) are isolated and validated to prevent introducing vulnerabilities.

</td>
</tr>
<tr>
<td valign="top">

Validate Domain Models for Security

</td>
<td valign="top">

Review Core Data Services \(CDS\) models to ensure sensitive data is protected and access is restricted.

</td>
</tr>
</table>

These guidelines help you to implement an application that integrates security into its UI, architecture, and domain models, supporting the development of a compliant and trustworthy solution.

See:

-   [The Secure Software Development and Operations Lifecycle \(secure SDOL\) at SAP](https://www.sap.com/documents/2016/03/a248a699-627c-0010-82c7-eda71af511fa.html)
-   [SAP BTP Guidance Framework](https://help.sap.com/docs/sap-btp-guidance-framework/guidance-framework/what-is-sap-btp-guidance-framework?locale=en-US)


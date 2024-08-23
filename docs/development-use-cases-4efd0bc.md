<!-- loio4efd0bc86ade42c28bf4c4c8dbc4451b -->

# Development Use Cases



<a name="loio4efd0bc86ade42c28bf4c4c8dbc4451b__section_fvz_33k_bzb"/>

## Typical Development Use Case Patterns

The following use case patterns should always be implemented on the SAP BTP:

-   Automate processes across backend systems

    This pattern provides low code/no code capabilities to automate processes and is meant for business experts and developers.

-   Build web and mobile applications

    This pattern provides mobile-native and web development capabilities and is meant for business experts and developers.

-   Develop full-stack applications

    This pattern is meant for professional developers and has the following flavors:

    -   Full-stack single-tenant applications

        This pattern is meant for customers and implementation partners enabling them to develop full-stack applications on SAP BTP.

    -   Full-stack multitenant SaaS applications for partners that are independent software vendors

        This pattern is meant for SAP partners enabling them to develop full-stack SaaS applications on the SAP BTP and to distribute these applications to their customers. Partners can easily onboard multiple customers \(tenants\) onto a single application with strictly separated data. This approach dramatically reduces the total cost of ownership at cloud scale.

    -   Hub scenario integrating with several ERP systems and/or cloud services

        This pattern provides a central hub on SAP BTP to collect and distribute data from various systems.





<a name="loio4efd0bc86ade42c28bf4c4c8dbc4451b__section_tq3_ggk_bzb"/>

## Extensibility Options

Most development use cases address some sort of extension of SAP S/4HANA and SAP S/4HANA Cloud, public or private edition. Depending on the nature of the extension, different extensibility options are available. The extensibility options can be roughly divided into two categories:

-   On-stack extensibility

    A group of extensibility options that allows users to directly extend the software stack without any remote connection. The extensibility options are:

    -   Key user extensibility

    -   Developer extensibility

    -   Classic extensibility: not recommended; it's available only in private cloud and on-premise setups.


    For detailed explanation of the ABAP on-stack extensibility options, see [Extend SAP S/4HANA in the Cloud and On-Premise with ABAP-Based Extensions](https://www.sap.com/documents/2022/10/52e0cd9b-497e-0010-bca6-c68f7e60039b.html).

    In this document, you can also find decision tables when to use which extensibility option and how to combine these options in more complex scenarios.

-   Side-by-side extensibility

    An extensibility option that allows developers or key users to implement development projects, such as creating custom user interfaces or custom applications. The development projects are implemented on SAP BTP and integrated via released remote APIs.




<a name="loio4efd0bc86ade42c28bf4c4c8dbc4451b__section_dkh_5hk_bzb"/>

## Building Transactional, Analytical Applications and Integration Scenarios with ABAP Cloud

ABAP Cloud offers developers a programming model to design and implement transactional applications, analytical applications, and integration scenarios. Applications can be deployed as single tenant or multitenant SaaS applications.

ABAP Cloud defines the technological core of the ABAP Cloud development model and consists of technologies such as ABAP, ABAP RESTful Application Programming Model \(RAP\) and Core Data Services, reuse services and libraries to implement the programming model aspects. Built-in qualities define the common quality characteristics that all ABAP Cloud implementations fulfil such as extensibility or identity and access management.


<!-- loio9aaaf650d02e42afba0e4b09e2991d78 -->

# ABAP Cloud



<a name="loio9aaaf650d02e42afba0e4b09e2991d78__section_sgv_1hw_czb"/>

## Overview

The technological core of [ABAP Cloud](https://help.sap.com/docs/abap-cloud/abap-cloud/why-abap-cloud) defines the design-time and runtime architecture of all extensions, services, and applications. The main ABAP Cloud elements are:

-   ABAP Core Data Services \(CDS\) for the data model and for embedded analytics

-   The ABAP RESTful Application Programming Model \(RAP\)

-   The cloud-optimized ABAP language for the business logic

-   Mandatory public SAP APIs and extension points to allow automated cloud operations and lifecycle stable extensibility

-   ABAP Development Tools \(ADT\) in Eclipse as the ABAP integrated development environment


Building on these key elements, you can use ABAP Cloud to cover the following scenarios:

-   **Transactional \(OLTP\)**: With ABAP Cloud you can build business objects and expose them as services, to consume them in UIs and integration scenarios. All standard behavior is supported \(create, read, update, delete\).

-   **Analytical \(OLAP\)**: ABAP Cloud is equally equipped for creating services and UIs for data analysis, and for drilling down in multiple dimensions, like integrating the data in SAP Analytics Cloud.

-   **Integration**: Both previous aspects are complemented by strong data and application integration to cater to today’s service-oriented environments.


The development model has two additional two key differentiators:

-   The **reuse services and libraries** with core business services like number ranges, application jobs, an ABAP-integrated SAP Fiori launchpad, and UI repository to deploy SAPUI5 and SAP Fiori elements user interfaces.

-   The **built-in qualities** offering end-to-end extensibility in the programming model, major cloud qualities like scalability and upgrade stable APIs, and many more.




<a name="loio9aaaf650d02e42afba0e4b09e2991d78__section_rjg_xgw_czb"/>

## Use Cases for Developing with ABAP Cloud

With ABAP Cloud, you can cover a variety of use cases for different scenarios. The development path is structured according to the consumers: Either the consumer is a user or system, meaning either you want to create an app to manipulate or display data or you want to exchange data between systems with different protocols to create business processes with system-to-system communication.

With ABAP Cloud, you can develop transactional and analytical apps. Transactional applications have transactional characteristics to create, update or delete data records whereas analytical applications only read and display data in charts or dashboards.

All applications and services developed with ABAP Cloud are by default multitenant enabled. Partners can use the [SAP BTP, ABAP environment](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/abap-environment) Software-as-a-Service tooling to easily build, deploy, and operate Software-as-a-Service solutions on their own.

Integration services enable system-to-system communication for different protocols. In ABAP Cloud, integration services can be used for process integration or data integration. With process integration, the communication is structured along a predefined business process like, for example, order-to-cash. Data integration in contrast focuses on transferring raw data without any relation to a business process.

**Related Information**  


[Design](design-314ae3e.md "")

[Develop](develop-c8906e4.md "")

[Deploy](deploy-d7aec3c.md "")

[Operate](operate-f7f2977.md "")


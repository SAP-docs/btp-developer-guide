<!-- loioc1f21a47f38b467997436c13fe773513 -->

# Understanding Available Technology

To be able to build an application using what SAP BTP offers, you have to understand what are the recommended use case patterns and what services, tools, and integrations are available.

<a name="loio4efd0bc86ade42c28bf4c4c8dbc4451b"/>

<!-- loio4efd0bc86ade42c28bf4c4c8dbc4451b -->

## Development Use Cases



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

        The Poetry Slam Manager partner reference application on GitHub provides a comprehensive example to build, deploy, and run such a scalable SaaS solution. See [Tutorials and Reference Sample for Full-Stack Multitenant SaaS Applications for Partners](tutorials-and-reference-sample-for-full-stack-multitenant-saas-applications-for-partners-11d9894.md) and [Partner Reference Application 'Poetry Slam Manager'](https://github.com/SAP-samples/partner-reference-application/).

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

<a name="loiof3641a5635504edab2c6bb84fa86a42a"/>

<!-- loiof3641a5635504edab2c6bb84fa86a42a -->

## Business Application Services

SAP BTP Developer’s Guide has a comprehensive set of tools and services at your disposal that allow you to keep the pace and at the same time benefit from future investments in SAP BTP. The following graphic includes both ABAP and non-ABAP runtimes and provides an overview of the architecture you can use when designing and building your applications.

The overall suite of applications consists of multiple business modules that are either implemented for SAP Cloud Application Programming \(CAP\) or ABAP Cloud. Each business module consists of one or multiple self-contained services following a three-tier architecture with presentation, logic, and persistence layer. In both architecture styles, SAP Fiori and SAPUI5 is used to implement front end artifacts. These front end artifacts are consuming its data using OData for transactional and InA for analytical applications.

The application logic for CAP-based applications is implemented in Node.js, Java and Typescript and is deployed in SAP BTP, Cloud Foundry runtime or SAP BTP, Kyma runtime. The application logic for ABAP Cloud is implemented in ABAP and deployed in the SAP BTP, ABAP environment. In both cases, SAP HANA Cloud is used to store relational business data.

Additional enterprise qualities are reached by integrating the business modules with complementing SAP BTP application services such as SAP Build Work Zone as a central entry point, SAP Datasphere as a cross-application data warehouse or Identity Authentication for identity authentication among others.



This image is interactive. Hover over the image and click the highlighted areas so you are placed in the respective cell in the table.

![This diagram illustrates the architecture of the SAP Business Technology Platform, detailing its components like the SAP Build Work Zone with Kyma and ABAP runtimes, various application programming models, core data services, and connections to SAP HANA Cloud and SAP Datasphere. It also lists a comprehensive suite of SAP services available on the platform.](images/Technical_Architecture_251a03a.png)



****


<table>
<tr>
<th valign="top">

Capability

</th>
<th valign="top">

Cloud Application Programming

</th>
<th valign="top">

ABAP Cloud

</th>
</tr>
<tr>
<td valign="top" rowspan="2">

Development Tools

</td>
<td valign="top">

[SAP Business Application Studio](https://help.sap.com/docs/bas/sap-business-application-studio/what-is-sap-business-application-studio?version=Cloud)

Designed and optimized for business application development in SAP ecosystems, SAP Business Application Studio enhances productivity by offering specialized tools for various scenarios, including SAP Fiori application development, SAP HANA native extensions, full-stack and mobile application development, and more.

Central to the development environment is Code-OSS, the open-source foundation of Visual Studio Code, ensuring a familiar experience for developers when creating SAP-centric applications. SAP Business Application Studio streamlines the building, testing, and deployment of applications with integrated features for source control and testing. Furthermore, its Full-Stack Application Productivity Toolkit offers intuitive visual tools covering the entire development process, guaranteeing seamless integration with various SAP services and solutions.

</td>
<td valign="top" rowspan="2">

[ABAP Development Tools for Eclipse](https://tools.eu1.hana.ondemand.com/#abap)

[SAP Business Application Studio](https://help.sap.com/docs/bas/sap-business-application-studio/what-is-sap-business-application-studio?version=Cloud)

Use ABAP development tools for Eclipse to benefit from an efficient development environment for all ABAP-based development artifacts. Use the SAP Business Application Studio to develop the SAP Fiori parts of your ABAP-based applications.

</td>
</tr>
<tr>
<td valign="top">

[SAP Continuous Integration and Delivery](https://help.sap.com/docs/continuous-integration-and-delivery/sap-continuous-integration-and-delivery/what-is-sap-continuous-integration-and-delivery?version=Cloud)

The Continuous Integration & Continuous Delivery \(CI/CD\) service offers pre-configured pipelines that automate the building and testing of code changes developed in SAP Business Application Studio. These pipelines can be customized to meet your specific needs. By providing immediate feedback on the status of your code, the service helps to identify and fix issues early in the development process. This accelerates development and improves the quality of your code.

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Software Delivery

</td>
<td valign="top">

[SAP Continuous Integration and Delivery](https://help.sap.com/docs/continuous-integration-and-delivery/sap-continuous-integration-and-delivery/what-is-sap-continuous-integration-and-delivery?version=Cloud)

By enabling deployment, setting the deployment target, and optionally configuring the handover to SAP Cloud Transport Management, you can use SAP Continuous Integration and Delivery to automate your delivery process. This helps to accelerate your delivery cycles.

</td>
<td valign="top" rowspan="2">

[ABAP Lifecycle Management](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/abap-lifecycle-management)

-   For customers:

    Develop applications as software components and deliver them via the Manage Software Components application. See [Software Components](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/software-components).

    A hidden Git repository is automatically managed per software component using gCTS for transport management. This process can be automated with CI/CD pipelines including steps like test automation using ABAP Test Cockpit. See [Automate the Software Lifecycle Management Process](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/automate-software-lifecycle-management-process).

    SAP Cloud Transport Management can be used to optionally integrate with higher level change management processes. See [How to Export Using SAP Cloud Transport Management](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/how-to-export-using-sap-cloud-transport-management?q=cloud%20transport%20management).

-   For partners:

    In addition to the customer scenario, products can be built based on software components with the help of the Landscape Portal to set up multitenant SaaS applications or to offer installable products like SDKs for other customers and partners. See [Landscape Portal](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/landscape-portal).




</td>
</tr>
<tr>
<td valign="top">

[SAP Cloud Transport Management](https://help.sap.com/docs/cloud-transport-management/sap-cloud-transport-management/what-is-sap-cloud-transport-management?version=Cloud)

SAP Cloud Transport Management offers a standardized, enterprise-ready change management process. For changes in SAP BTP, Cloud Foundry runtime, the corresponding pipeline in SAP Continuous Integration and Delivery includes out-of-the-box transports in the Cloud Transport Management service.

While we strongly recommend using the Continuous Integration and Delivery service, you can also use SAP Cloud Transport Management to transport your changes without a pipeline.

</td>
</tr>
<tr>
<td valign="top">

Persistence

</td>
<td valign="top">

[SAP HANA Cloud](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-overview-guide/sap-hana-cloud-overview-guide)

Use SAP HANA Cloud service for a relational storage.

Use HANA Data Lake Files as Object Storage.

Consider compliance features like such as Audit Log, Cryptography or Customer Managed Keys that SAP HANA Cloud offers.

</td>
<td valign="top">

[SAP HANA Cloud](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-overview-guide/sap-hana-cloud-overview-guide)

SAP BTP, ABAP environment comes with an own ABAP-managed SAP HANA Cloud instance. Static resizing of the SAP HANA Cloud instance is supported. ABAP dictionary tables can be tagged to make use of the SAP HANA Native Storage Extensions; also, database indexes \(like unique secondary indexes and fuzzy search indexes\) and Dynamic View Caches can be defined. Furthermore, simple Database Partitioning based on primary keys is possible. Access to the SAP HANA instance data is only supported via the ABAP layer, for example, by using ABAP SQL, natively via ABAP-managed database procedures, and the ABAP SQL Service for external clients.

</td>
</tr>
<tr>
<td valign="top">

Programming Model

</td>
<td valign="top">

[SAP Cloud Application Programming Model \(CAP\)](https://cap.cloud.sap/docs/)

Use SAP Cloud Application Programming Model as programming model for non-ABAP applications.

Go-to frameworks for business application development. It supports the most widely adopted languages, which are: Java \(with Spring Boot\), JavaScript and TypeScript \(with Node.js\).

SAP Cloud Application Programming Model guarantees to run against specific versions of Node.js and Java. Remember to plan your application to run for at least 5 years if not more.

We recommend that you choose SAP BTP services over homegrown services.

</td>
<td valign="top">

[ABAP RESTful Application Programming Model \(RAP\)](https://help.sap.com/docs/btp/sap-abap-restful-application-programming-model/abap-restful-application-programming-model?version=Cloud)

Use ABAP RESTful Application Programming Model as a programming model within ABAP Cloud. With ABAP RESTful Application Programming Model, you can develop services for all types of SAP Fiori applications as well as publishing Web APIs.

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Runtime

</td>
<td valign="top">

[SAP BTP, Cloud Foundry Runtime](https://help.sap.com/docs/btp/sap-business-technology-platform/cloud-foundry-environment?version=Cloud)

Use SAP BTP, Cloud Foundry runtime as a runtime for CAP-based applications.

</td>
<td valign="top" rowspan="2">

[SAP BTP, ABAP Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/getting-started-with-customer-account-in-abap-environment?version=Cloud)

Use SAP BTP, ABAP environment for ABAP-based applications.

SAP BTP, ABAP environment delivers and enforces the ABAP Cloud development model and is based on Kubernetes. The abstraction of containers and clusters is managed by the SAP BTP, ABAP environment infrastructure.

</td>
</tr>
<tr>
<td valign="top">

[SAP BTP, Kyma Runtime](https://help.sap.com/docs/btp/sap-business-technology-platform/kyma-environment?version=Cloud)

Use SAP BTP, Kyma runtime as a runtime for CAP-based applications.

</td>
</tr>
<tr>
<td valign="top">

Client Library

</td>
<td valign="top">

[SAP Cloud SDK](https://help.sap.com/docs/SAP_CLOUD_SDK)

CAP is using SAP Cloud SDK behind the scenes.

SAP Cloud SDK provides client libraries for consuming OData/OpenAPI services, Destination service, and Connectivity service that extend SAP solutions and other OData/OpenAPI services on SAP Business Technology Platform. These clients allow you to concentrate on your unique business logic, simplifying development and ensuring seamless integration.

</td>
<td valign="top">

[Service Consumption Model](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/service-consumption-model)

Use the Service Consumption Model to generate local ABAP APIs to consume remote OData, SOAP and RFC services.

</td>
</tr>
<tr>
<td valign="top" rowspan="3">

Connectivity

</td>
<td valign="top">

[SAP Connectivity Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connectivity?version=Cloud)

Use Connectivity service to securely access on-premise systems and such hosted in virtual private cloud which are exposed via the Cloud Connector. Using the [service channels](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/16f63429a2344b8baec1c81cafe5d0fa.html) feature of the Cloud Connector, it is also possible to access cloud systems such as databases from on-premise and virtual private cloud networks. For Kubernetes-based workloads, you can utilize the Connectivity Proxy to ensure secure technical connectivity from the cloud to your on-premise and virtual private cloud systems. Within the Kyma runtime, the [Connectivity Proxy](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/e661713ef7d14373b57e3e26b0b03b86.html) comes as a managed offering.

</td>
<td valign="top">

[SAP Connectivity Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connectivity?version=Cloud)

The Connectivity service is automatically integrated with the BTP ABAP tenants to securely access on-premise systems and such hosted in virtual private cloud which are exposed via the Cloud Connector.

</td>
</tr>
<tr>
<td valign="top">

[SAP Destination Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/consuming-destination-service?version=Cloud)

Use Destination service to store and retrieve technical connection properties to the target systems. It automates the process of retrieving OAuth access tokens to the configured target systems. In addition, the Destination service generates and is able to renew X.509 client certificates issued by the SAP Cloud PKI.

</td>
<td valign="top" rowspan="2">

[Communication Management](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/communication-management)

SAP BTP, ABAP Environment provides a Communication Management to integrate the custom applications with other systems to enable data exchange.

An event consumption and event provisioning is also natively supported and integrated into the ABAP RESTful Application Programming Model \(RAP\).

In addition, the SAP Destination Service can also be used to re-use destinations for CAP applications. See [SAP Destination Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/consuming-destination-service?version=Cloud).

</td>
</tr>
<tr>
<td valign="top">

[Transparent Proxy for Kubernetes](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/transparent-proxy-for-kubernetes?version=Cloud)

Use transparent proxy to enhance developers' user experience and simplify the consumption of target systems by automating the retrieval of destinations from the Destination service, as well as integration with the connectivity proxy and authentication with target systems.

Within the SAP BTP, Kyma runtime, the transparent proxy comes as a managed offering.

</td>
</tr>
<tr>
<td valign="top">

Application Programming Interface

</td>
<td valign="top" colspan="2">

[SAP Business Accelerator Hub](https://api.sap.com/)

Follow API guidelines and use the SAP Business Accelerator Hub.

</td>
</tr>
<tr>
<td valign="top">

User Interface \(Web\)

</td>
<td valign="top" colspan="2">

[SAP Fiori Elements](https://experience.sap.com/fiori-design-web/smart-templates/)

[SAPUI5](https://sapui5.hana.ondemand.com/)

Use SAP Fiori elements for OData V4 to benefit from a presentation of a common UI and UX. For more flexibility, use SAP Fiori element’s Flexible Programming Model with or without SAPUI5 Freestyle. Personalization and theming are automatically supported.

SAP Fiori elements and SAPUI5 help you present one consistent solution experience to your customers, and you benefit from the upcoming designs and UX improvements automatically.

Remember that even the simplest UI components or more complex ones like geographic maps have compliance requirements like accessibility and theming.

</td>
</tr>
<tr>
<td valign="top">

User Interface \(Mobile\)

</td>
<td valign="top" colspan="2">

[SAP Mobile Development Kit](https://community.sap.com/topics/mobile-technology/mobile-development-kit)

[SAP BTP SDK for Android](https://help.sap.com/doc/f53c64b93e5140918d676b927a3cd65b/Cloud/en-US/docs-en/guides/getting-started/android/overview.html)

[SAP BTP SDK for iOS](https://help.sap.com/doc/f53c64b93e5140918d676b927a3cd65b/Cloud/en-US/docs-en/guides/getting-started/ios/introduction.html)

Use SAP MDK, BTP SDK for Android or BTP SDK for iOS for mobile applications.

These SDKs help you present one consistent solution experience to your customers.

Mobile application development is massively accelerated as SAP mobile services and its SDKs generate the complete synchronization and authentication layer. Additional supported features like logging, tracing, crash reporting bring extra value to you.

After deployment the Mobile services give administrators all the necessary tools and services to operate a mobile solution. Features like push, offline, mobile specific security and more simplify the operation.

</td>
</tr>
<tr>
<td valign="top">

Central Entry Point

</td>
<td valign="top">

[SAP Build Work Zone, standard edition](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/what-is-sap-build-work-zone-standard-edition)

[SAP Build Work Zone, advanced edition](https://help.sap.com/docs/build-work-zone-advanced-edition/sap-build-work-zone-advanced-edition/what-is-sap-build-work-zone-advanced-edition)

[SAP HTML5 Application Repository Service for SAP BTP](https://help.sap.com/docs/btp/sap-business-technology-platform/developing-html5-applications-in-cloud-foundry-environment)

Enable the central launchpad to offer a unified end-user experience.

Customers want to create a personalized view on the applications you produce. Make sure your application can be added to a central launchpad, regardless of where it runs.

</td>
<td valign="top">

[SAP Fiori Launchpad for SAP BTP, ABAP Environment](https://help.sap.com/docs/btp/sap-fiori-launchpad-for-sap-btp-abap-environment/sap-fiori-launchpad-user-guide?version=Cloud) 

[SAP Build Work Zone, standard edition](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/what-is-sap-build-work-zone-standard-edition)

[SAP Build Work Zone, advanced edition](https://help.sap.com/docs/build-work-zone-advanced-edition/sap-build-work-zone-advanced-edition/what-is-sap-build-work-zone-advanced-edition)

[SAP HTML5 Application Repository Service for SAP BTP](https://help.sap.com/docs/btp/sap-business-technology-platform/developing-html5-applications-in-cloud-foundry-environment)

SAP BTP, ABAP Environment comes with a dedicated central entry point the SAP Fiori launchpad for SAP BTP, ABAP Environment. This central entry point offers a unified end-user experience for ABAP-based applications. It is also used as the entry point for all SAP Fiori applications to administer the ABAP system.

SAP Build Work Zone, standard edition offers a unified end-user experience across several systems for federation scenarios.

</td>
</tr>
<tr>
<td valign="top" rowspan="4">

Integration

</td>
<td valign="top" colspan="2">

[SAP Event Mesh](https://help.sap.com/docs/event-mesh/event-mesh/what-is-sap-event-mesh?version=Cloud)

[SAP Cloud Application Event Hub](https://help.sap.com/docs/event-broker/event-broker-service-guide/what-is?locale=en-US%3Fversion%3DCloud&version=Cloud)

[SAP Integration Suite, advanced event mesh](https://help.sap.com/docs/SAP_ADVANCED_EVENT_MESH/649cec0ae9ac49059564a1870fb8a1b7/0d4bcd5a2be744688039160b9bb289ae.html?version=Cloud)

SAP Event Mesh can be used to distribute events between selected SAP cloud and on-premise applications and third-party applications.

SAP Integration Suite, advanced event mesh is currently not supported by CAP and ABAP Cloud.

SAP Cloud Application Event Hub allows CAP-based applications to consume business events from supported SAP cloud applications. Currently, SAP Cloud Application Event Hub is not supported by ABAP Cloud.

</td>
</tr>
<tr>
<td valign="top" colspan="2">

[SAP Master Data Integration](https://help.sap.com/docs/SAP_MASTER_DATA_INTEGRATION/c7713d6177ad479d9ea00958db9f2f81/dab76d5506a44c8e85f314fc3be30e13.html?version=CLOUD)

SAP Master Data Integration service acts as the central master data hub. It uses the integration models of SAP One Domain Model as the basis for master data replication. SAP will extend the support of SAP One Domain Model in all SAP cloud applications over time to integrate them. When out-of-the-box integration with SAP Master Data Integration is not available, SAP Integration Suite can be used to integrate with SAP ERP Central Component, SAP S/4HANA, and non-SAP applications.

</td>
</tr>
<tr>
<td valign="top" colspan="2">

[SAP Integration Suite](https://help.sap.com/docs/integration-suite/sap-integration-suite/what-is-sap-integration-suite?version=CLOUD)

Use the Cloud Integration capability of SAP Integration Suite for mediated data or process integration, especially if complex integration flows, transformations or dedicated protocols are required. Besides mediated application-to-application integration, Cloud Integration usage is recommended for business-to-business and business-to-governance processes.

The API Management capability of SAP Integration Suite allows you to easily enable your developer community with governed, secure, and policy-compliant access to all your APIs, events, and integrations.

Graph is a recent addition to the API Management capability of SAP Integration Suite. Graph is a powerful semantic API mediation, combining and exposing the data from diverse systems in a complex enterprise landscape as connected data graphs. The data graphs are accessed via a single, curated, and uniform data-as-a-service API and make API consumption much easier.

</td>
</tr>
<tr>
<td valign="top" colspan="2">

[Cloud Integration Automation](https://help.sap.com/docs/cloud-integration-automation/user-guide/overview)

Cloud Integration Automation service provides you a guided workflow to integrate SAP cloud solutions to on-premise and other SAP cloud solutions. The guided workflow contains instructions for manual and automated tasks to enable an easy and quick integration configuration setup.

</td>
</tr>
<tr>
<td valign="top" rowspan="3">

Observability

</td>
<td valign="top">

[SAP Cloud ALM](https://help.sap.com/docs/link-disclaimer?site=https%3A%2F%2Fsupport.sap.com%2Fen%2Falm%2Fsap-cloud-alm.html)

SAP Cloud ALM helps you to implement and operate intelligent cloud and hybrid business solutions.

For your CAP-based applications on SAP BTP, SAP Cloud ALM provides a central, personalized and unified operations user experience. Specifically for Java and Node.js custom-built applications in SAP BTP, Cloud Foundry runtime, there are the Data Collection Instrumentation Libraries based on Open Telemetry designed to enable the data collection infrastructure in SAP Cloud ALM. With these libraries, you can collect data for many observability use cases, such as:

-   Real User Monitoring

-   Real User Monitoring

-   Health Monitoring

-   Integration and Exception Monitoring




</td>
<td valign="top" rowspan="3">

[SAP Cloud ALM](https://help.sap.com/docs/link-disclaimer?site=https%3A%2F%2Fsupport.sap.com%2Fen%2Falm%2Fsap-cloud-alm.html)

All ABAP cloud applications are supported by SAP Cloud ALM for central observability. SAP Cloud ALM provides the following use cases:

-   Real User Monitoring

-   Health Monitoring

-   Synthetic User Monitoring

-   Integration Monitoring

-   Job and Automation Monitoring

-   Data Forwarding to SAP Focused RUN


For Health Monitoring, you could extend the delivered content with your own custom metrics.

SAP BTP, ABAP Environment strictly distinguishes between platform monitoring and application monitoring. The platform monitoring, like availability monitoring, is ensured by the service itself.

For application monitoring, which is in your responsibility, respective tools are offered. Use the Technical Monitoring Cockpit to analyze and optimize the application on-stack:

-   System workload

-   Resource consumption and capacity

-   Detailed statistics captured for single requests

-   Outbound communication

-   SQL statements




</td>
</tr>
<tr>
<td valign="top">

[SAP Alert Notification service for SAP BTP](https://help.sap.com/docs/alert-notification/sap-alert-notification-for-sap-btp/what-is-sap-alert-notification-service-for-sap-btp?version=Cloud)

Local expert tool that allows you to subscribe to events from the platform – such as from used services, from your custom-built apps, or from the infrastructure – and to consume them via your channel of choice \(such as by receiving notifications via email or in your preferred chat application\). Can be integrated into central alerting of SAP Cloud ALM.

</td>
</tr>
<tr>
<td valign="top">

[SAP Cloud Logging](https://help.sap.com/docs/cloud-logging/cloud-logging/what-is-sap-cloud-logging?version=Cloud)

SAP Cloud Logging allows you to analyze your SAP BTP workloads in great detail regarding performance, errors, usage, and other characteristics.

It covers processing of logs, metrics, traces across SAP BTP, Cloud Foundry runtime and SAP BTP, Kyma runtime with flexible storage, alerting, and dashboarding.

</td>
</tr>
<tr>
<td valign="top">

Customer Landscape Discovery

</td>
<td valign="top">

[Unified Customer Landscape](https://help.sap.com/docs/btp/sap-business-technology-platform/maintaining-unified-customer-landscape?version=Cloud)

Use Unified Customer Landscape service for customer landscape management.

There are different ways to add systems to the *System Landscape* page in the SAP BTP cockpit: manually or automatically. If a system of your solution is associated with your global account or through a subscription in SAP BTP cockpit associated with a given subaccount, it will appear in the list automatically. Otherwise, you have to add your system manually. Systems are added to the list in one of the following ways:

-   Auto-Discovered

    An auto-discovered system is a system \(associated with the given global account\) that has been discovered and added automatically to the list based on information of the existing system landscape. Any SAP system of the supported system types that is associated with the same customer ID, with which your global account in SAP BTP is associated, will be added automatically in the system landscape list.

-   Subaccount/<my-subaccount\>

    Specifies that the system has been added through a subscription in SAP BTP cockpit associated with a given subaccount. The subscription has been discovered and added automatically through the subaccount.

-   Manually-Added

    Specifies that the system has been added to the list manually by the global account administrator, using the *Add System* button and completing the wizard. The system has been associated with the global account in SAP BTP.




</td>
<td valign="top">

[Landscape Portal](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/landscape-portal)

Landscape Portal is offered to manage all the systems within your global account in SAP BTP. It shows the list of the ABAP systems, it enables the control of system hibernation to reduce costs and it offers features to control the system lifecycle, for example, to nominate systems for the pre-upgrade prior to the standard upgrade of a quarterly ABAP platform release.

</td>
</tr>
<tr>
<td valign="top">

Extensibility and Integration

</td>
<td valign="top">

Side-by-Side Extensibility with Unified Customer Landscape:

-   [Register Systems](https://help.sap.com/docs/btp/sap-business-technology-platform/registering-sap-system?version=Cloud)

-   [Create Formations](https://help.sap.com/docs/btp/sap-business-technology-platform/including-sap-systems-in-formation?version=Cloud)

-   [SAP SuccessFactors Extensibility Service](https://help.sap.com/docs/btp/sap-business-technology-platform/extending-sap-successfactors-in-cloud-foundry-and-kyma-environment?version=Cloud)

-   [SAP S/4HANA Cloud Extensibility Service](https://help.sap.com/docs/btp/sap-business-technology-platform/extending-sap-s-4hana-cloud-in-cloud-foundry-and-kyma-environment?version=Cloud)


Use Unified Customer Landscape service that offers customer landscape management capabilities for your SAP S/4HANA, SAP Ariba, SAP SuccessFactors, and other SAP and third-party systems in one single experience.

In the SAP BTP cockpit, you get a comprehensive overview of all your systems associated with your customer ID. These systems can be registered or auto discovered. They are conveniently listed as a record in the *Systems* list in the *System Landscape* page in the SAP BTP cockpit. Moreover, Unified Customer Landscape lets you integrate one or more systems in a common business case by including these systems in a formation.

</td>
<td valign="top">

[On-Stack Extensibility by Extending SaaS Applications](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/extending-saas-applications)

In addition to the standard side-by-side approach for core applications such as SAP S/4HANA, SAP BTP, ABAP Environment also offers two extensibility options within the product itself:

-   With developer extensibility, you can extend partner solutions which are installed in your customer system, for example by adding custom fields, custom nodes and business logic.

-   With key user extensibility, you can extend a multitenancy SaaS application offered by a partner. The supported extensibility features to extend SaaS applications are UI adaptations, custom fields and custom logic \(implement Business Add-Ins\).


You can create business configuration objects. See [Business Configuration](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/development-business-configuration).

You can create and set up integration scenarios by maintaining communication arrangements.

</td>
</tr>
<tr>
<td valign="top">

Data Privacy

</td>
<td valign="top" colspan="2">

[SAP Data Privacy Integration](https://help.sap.com/docs/data-privacy-integration/development/data-privacy-integration?version=Cloud)

Use Data Privacy Integration service to make your SAP BTP application compliant with the corporate Data Privacy and Protection standards. Integrate with the Data Privacy Integration service to support cross consumable Data Privacy and Protection features for our customers and support cross Data Privacy and Protection compliance in end-to-end processes.

</td>
</tr>
<tr>
<td valign="top">

Workflow

</td>
<td valign="top" colspan="2">

[SAP Task Center](https://help.sap.com/docs/task-center/sap-task-center/what-is-sap-task-center?version=Cloud)

SAP Task Center service enables integration with SAP applications to provide a single entry point for end users to access all their assigned tasks. The tasks can be accessed by end users through the SAP Task Center Web application.SAP Task Center helps you integrate tasks into a central solution.

Use SAP Task Center as a unified inbox for tasks across multiple applications with integrated user experience. Tasks from multiple SAP solutions are gathered in one list and ready to be processed in just one click, shortening the completion time for business-critical tasks. For example, business users can process all their tasks from the connected systems, without the need to switch and log in separately into different inboxes.

[SAP Build Process Automation](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/what-is-sap-build-process-automation?version=Cloud)

SAP Build Process Automation provides a simpler and faster way to adapt, improve, and innovate business processes with drag-and-drop simplicity.

The solution combines workflow management, SAP Intelligent Robotic Process Automation \(SAP Intelligent RPA\) functionality, decision management, process visibility, and embedded AI capabilities into one intuitive low-code experience.

You can jumpstart automation projects with hundreds of process content packages, SAP Intelligent RPA bots and connectors designed specifically to enhance the capabilities of the SAP solutions you are using. It provides a unified development experience for users of all skill levels enabling fusion teams of business experts and developers to work together and solve challenges faster.

</td>
</tr>
<tr>
<td valign="top">

Job Scheduling

</td>
<td valign="top">

[SAP Job Scheduling Service](https://help.sap.com/docs/job-scheduling/sap-job-scheduling-service/what-is-sap-job-scheduling-service?version=Cloud)

SAP Job Scheduling service allows you to define and manage jobs that run once or on a recurring schedule. Use this runtime-agnostic service to schedule action endpoints in your application or long-running processes using Cloud Foundry tasks. Use REST APIs to schedule jobs, including long-running jobs asynchronously, and create multiple schedule formats for simple and complex recurring schedules. Manage jobs and tasks and manage schedules with a web-based user interface.

</td>
<td valign="top">

[Application Jobs](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/application-jobs)

Job scheduling is integrated into the product. Application Jobs can be defined, implemented and monitored.

</td>
</tr>
<tr>
<td valign="top">

Application Logs

</td>
<td valign="top">



</td>
<td valign="top">

[Application Logs](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/application-logs)

SAP Task Center helps you integrate tasks into a central Application Logging is integrated into the product. Application Logs can be defined, implemented, and monitored.

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Analytics

</td>
<td valign="top">

[SAP Analytics Cloud](https://help.sap.com/docs/SAP_ANALYTICS_CLOUD)

Use embedded analytics scenarios in your application including dashboards, multi-dimensional reports and KPIs.

</td>
<td valign="top">

[SAP Analytics Cloud](https://help.sap.com/docs/SAP_ANALYTICS_CLOUD)

Use SAP Analytics Cloud on top of InA-enabled Core Data Service analytical models. Furthermore, Dragonfly-based multi-dimensional reporting can be used to integrate Embedded Analytics functionality in a component-based and SAP Fiori-native way.

</td>
</tr>
<tr>
<td valign="top">

[SAP Datasphere](https://help.sap.com/docs/SAP_DATASPHERE)

For analytics across applications use SAP Datasphere.

</td>
<td valign="top">

[SAP Datasphere](https://help.sap.com/docs/SAP_DATASPHERE)

Via the ABAP SQL Service it is possible to integrate with SAP Datasphere. Furthermore, the ABAP SQL Service in combination with ABAP ODBC Driver or the SAP HANA Cloud ABAP SDA Adapter allows data federation via external clients respectively via SAP HANA Cloud-based SAP BTP applications.

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Document Management

</td>
<td valign="top" colspan="2">

[SAP Document Management Service](https://help.sap.com/docs/document-management-service/sap-document-management-service/what-is-document-management-service?version=Cloud)

Document Management Service, Integration Option lets you build document management capabilities for your business applications using the integration component or the easy-to-use, reusable UI component.

Document Management Service, Application Option is a standalone, ready-to-use web application that provides document management capabilities for your enterprise content.

</td>
</tr>
<tr>
<td valign="top">

[Object Store on SAP BTP](https://help.sap.com/docs/object-store/object-store-service-on-sap-btp/what-is-object-store)

Object Store service on SAP BTP lets you store and manage objects, which involves creation, upload, download, and deletion. This service is specific to the Infrastructure-as-a-Service layer such as Azure Blob Storage, Amazon Web Services, and Google Cloud Platform.

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Low Code/No Code

</td>
<td valign="top" colspan="2">

[SAP Build](https://help.sap.com/docs/SAP%20Build/9d385a1842594230993661ca78dce150/7e50fa5e724c49d1a4352848275fd3cc.html?version=Cloud)

SAP Build is a low-code offering to accelerate development and automation. It enables you to create enterprise apps \(SAP Build Apps\), automate processes \(SAP Build Process Automation\), and design business sites \(SAP Build Work Zone\) without writing code. Accelerate development with prebuilt connectors and business content for SAP and third-party systems to integrate seamlessly. SAP Build fosters collaboration between business and development teams with built-in governance and lifecycle management.

</td>
</tr>
<tr>
<td valign="top">

Service Management

</td>
<td valign="top">

[SAP Service Manager](https://help.sap.com/docs/service-manager/sap-service-manager/sap-service-manager?version=Cloud)

SAP Service Manager service allows you to consume platform services in any connected runtime environment, track the creation and management of service instances, and share services and service instances between different environments.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Authentication

</td>
<td valign="top">

[SAP Authentication and Trust Management Service](https://help.sap.com/docs/btp/sap-business-technology-platform/sap-authorization-and-trust-management-service-in-cloud-foundry-environment?version=Cloud)

The SAP Authentication and Trust Management service lets you manage user authorizations and trust to identity providers. Identity providers are the user base for applications.

We recommend that you use an Identity Authentication tenant, an SAP on-premise system, or a custom corporate identity provider. User authorizations are managed using technical roles at the application level, which can be aggregated into business-level role collections for large-scale cloud scenarios.

</td>
<td valign="top">

[Access Management](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/access-management)

User authorizations are managed and can be aggregated into business roles locally in SAP BTP, ABAP environment.

</td>
</tr>
<tr>
<td valign="top">

[Identity Authentication](https://help.sap.com/docs/identity-authentication/identity-authentication/what-is-identity-authentication?version=Cloud)

The Identity Authentication service provides you with controlled cloud-based access to business processes, applications, and data. It simplifies your user experience through authentication mechanisms, single sign-on, on-premise integration, and convenient self-service options.

</td>
<td valign="top">

[Identity Authentication](https://help.sap.com/docs/identity-authentication/identity-authentication/what-is-identity-authentication?version=Cloud)

The Identity Authentication service provides you with controlled cloud-based access to business processes, applications, and data. It simplifies your user experience through authentication mechanisms, single sign-on, on-premise integration, and convenient self-service options.

Technical users for system-to-system communication are managed locally in the SAP BTP, ABAP environment. SAP BTP, ABAP environment supports mTLS and basic authentication as authentication options for technical users.

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Audit Logging

</td>
<td valign="top" rowspan="2">

[SAP Audit Log Service](https://help.sap.com/docs/btp/sap-business-technology-platform/audit-logging-in-cloud-foundry-environment?version=Cloud)

SAP Audit Log is a core, security, and compliance-based SAP BTP service to provide means for audit purposes. The default and advanced capabilities of Audit Log Service are available for SAP BTP applications and services.

</td>
<td valign="top">

[Manage Security Audit Log](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/manage-security-audit-log)

Security audit logging is provided automatically by the SAP BTP, ABAP Environment. It can be configured by the Manage Security Audit Log administration application.

</td>
</tr>
<tr>
<td valign="top">

[Read Access Logging](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/read-access-logging)

Read Access Logging \(RAL\) is used to monitor and log read access to sensitive data. This data may be categorized as sensitive by law, by external company policy, or by internal company policy.

</td>
</tr>
<tr>
<td valign="top">

Security

</td>
<td valign="top">

[SAP Credential Store](https://help.sap.com/docs/credential-store/sap-credential-store/what-is-sap-credential-store)

SAP Credential Store service provides a repository for passwords, keys and keyrings for applications that are running on SAP BTP. It enables the applications to retrieve credentials and use them for authentication to external services, or to perform cryptographic operations and TLS communication. SAP Credential Store is exposed to the applications via a REST API.

</td>
<td valign="top">

[Communication Management](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/communication-management)

The ABAP environment offers its Communication Management. It contains a credentials store which allows the applications to perform outbound communication using the credentials for authentication to external services and TLS communication.

</td>
</tr>
<tr>
<td valign="top">

Identity Management

</td>
<td valign="top">

[Identity Provisioning](https://help.sap.com/docs/identity-provisioning/identity-provisioning/what-is-identity-provisioning?version=Cloud)

The Identity Provisioning service automates identity lifecycle processes. It helps you provision identities and their authorizations to various cloud and on-premise business applications.

</td>
<td valign="top">

[Identity Provisioning](https://help.sap.com/docs/identity-provisioning/identity-provisioning/what-is-identity-provisioning?version=Cloud)

The Identity Provisioning service automates identity lifecycle processes. SAP BTP, ABAP environment supports the Identity provisioning service to provision business users and their assignment to business roles.

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Technical Оps Аutomation

</td>
<td valign="top">

[Terraform Provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest/docs)

The Terraform provider for SAP BTP enables you to automate the provisioning, management, and configuration of resources on SAP BTP.

</td>
<td valign="top">



</td>
</tr>
<tr>
<td valign="top">

[SAP Automation Pilot](https://discovery-center.cloud.sap/serviceCatalog/automation-pilot?region=all)

SAP Automation Pilot allows to reduce operational efforts to run your cloud applications on SAP BTP by automating them. For this, it brings catalogs of automated commands, such as around database and application lifecycle management tasks for the different runtimes of SAP BTP. Use these commands to model and run your custom scenarios, optionally combined with custom scripts. Also, you can describe your needs to let the included Generative AI feature come up with a command for you. The created commands can be triggered manually, via scheduling or externally, such as from SAP Cloud ALM.

</td>
<td valign="top">



</td>
</tr>
</table>
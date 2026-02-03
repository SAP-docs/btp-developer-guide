<!-- loiof19c8e9650a341aca72c4e4f4726b17d -->

# Data Persistence Using SAP HANA Cloud

SAP HANA Cloud is a cloud-native Database-as-a-Service that forms the database management foundation of the SAP Business Technology Platform \(SAP BTP\). It provides a single, scalable, and highly performant database environment for both transactional and analytical workloads, supporting multiple data models like relational, document, geospatial, and vector data. SAP HANA Cloud enables you to build modern, intelligent applications that leverage real-time enterprise data, generative AI, and flexible data integration- all without the administrative overhead of managing hardware or backups. It seamlessly integrates with other SAP BTP services and external systems, empowering developers to innovate with secure, elastic, and fully managed data services within the broader SAP BTP ecosystem.

In the overall developer context for SAP HANA Cloud serves as the core data layer, enabling data-driven application development, analytics, and intelligent business processes, while providing cloud scalability and multi-model flexibility essential for modern enterprise application development.

See [SAP HANA Cloud, SAP HANA Database](https://help.sap.com/docs/hana-cloud-database?version=2025_3_QRC&locale=en-US).



<a name="loiof19c8e9650a341aca72c4e4f4726b17d__section_wfh_njz_ygc"/>

## SAP HANA Cloud Helps Reduce the Total Cost of Ownership

SAP HANA Cloud can help with reducing the total cost of ownership \(TCO\) when following these best practices:

1.  [Native Storage Extension \(NSE\)](https://help.sap.com/docs/hana-cloud-database/sap-hana-cloud-sap-hana-database-administration-guide/sap-hana-native-storage-extension?locale=en-US)reduces the memory size of your SAP HANA Cloud instance. It is possible to keep data on disks, which are not frequently accessed. The Native Storage Extension advisor provides you recommendations for data being managed in-memory or in Native Storage Extension.

    SAP HANA Cloud advisors create data-driven recommendations that support database administrators in optimizing system performance and efficiency. The [NSE Advisor](https://help.sap.com/docs/hana-cloud-database/sap-hana-cloud-sap-hana-database-administration-guide/understanding-sap-hana-nse-advisor?locale=en-US) provides a flexible interface to act on individual recommended objects to convert from column-loadable to page-loadable, or vice versa.

2.  [Elastic Compute Nodes \(ECN\)](https://help.sap.com/docs/hana-cloud-database/sap-hana-cloud-sap-hana-database-administration-guide/sap-hana-cloud-elastic-compute-node?locale=en-US)enable adding on demand computation power to your SAP HANA Cloud instance in situations with high workload, for example, for analytics and planning, where you see a high CPU-utilization and performance degradation. Elastic Compute Nodes can be disabled at any time after the high-workload phase. The Elastic Compute Nodes enabling or disabling can even be scheduled and automated, for example with the SAP Automation Pilot. We recommend the [SAP-sample GitHub](https://github.com/SAP-samples/automation-pilot-examples/tree/main/hana-ecn-other)repository a ready to use command for Elastic Compute Nodes in SAP Automation Pilot.

    The usage monitoring with [ECN Advisors](https://help.sap.com/docs/hana-cloud-database/sap-hana-cloud-sap-hana-database-administration-guide/elastic-compute-node-advisor?locale=en-US) is an intelligent SAP HANA Cloud component that collects statistics about the usage that is provided to the user, developer, or administrator.

3.  [Table Partitioning](https://help.sap.com/docs/hana-cloud-database/sap-hana-cloud-sap-hana-database-administration-guide/table-partitioning?locale=en-US) helps you to optimize the query performance in your SAP HANA Cloud instance. Tables are split into different parts \(partitions\) that simplify and accelerate the data operations on large tables. Partitioning is typically used in multiple-host systems, but it may also be beneficial in single-host systems.

4.  [Native Multi-Tenancy](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-multitenancy/sap-hana-cloud-multitenancy?locale=en-US) allows you to develop and operate a SaaS application that serves many customers at the same time within a single instance. Customer data is isolated by default and can be managed independently from each other. SAP HANA Cloud allows up to 1000 native database tenants, which sizes can vary from a few kilobytes up to terabytes.

5.  SAP HANA Cloud is already available at 16GB memory in the BTP Free Tier Offering. You can use free tier to get started and are not limited to a trial period. You can also seamlessly upgrade your free tier instance to a full productive SAP HANA Cloud instance. Note that with the free tier license there are some limitations. See [SAP HANA Database License](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/sap-hana-database-license?locale=en-US).

6.  [Mutli-model capabilities](http://developers.sap.com/group.hana-cloud-smart-multi-model-data.html)of SAP HANA Cloud enable organizations to manage and analyze diverse types of data in a single, unified database platform. This approach simplifies the architecture, enhances the analytics, and supports AI-powered applications by integrating specialized engines and data models.




<a name="loiof19c8e9650a341aca72c4e4f4726b17d__section_qdr_xlz_ygc"/>

## CAP Specifics in Supporting SAP HANA Cloud

SAP Cloud Application Programming Model \(CAP\) supports SAP HANA Cloud in local and hybrid development on SAP BTP by providing a standardized framework that facilitates consistent development of cloud-native applications. CAP uses Core Data Services \(CDS\) to define domain models and automatically generates the corresponding database artifacts for SAP HANA Cloud, enabling developers to build, test, and run applications locally or in a hybrid mode before deploying to the cloud environment.

With CAP, you can leverage seamless integration with SAP HANA Cloud including multitenancy, schema evolution, and SAP HANA Infrastructure Services-based deployment artifacts. CAP supports Node.js and Java and auto-configures the SAP HANA Cloud data source based on the available service bindings when deployed on SAP BTP. This allows unified development experience across local development setups \(for example, SAP Business Application Studio or VS Code\) and hybrid cloud scenarios where parts of the application or data reside on-premises or in other cloud environments.

Key features include:

-   CAP abstracts the complexities of database deployment, service provisioning, and service bindings for SAP HANA Cloud.

-   Local development with CAP can generate and emulate database artifacts before pushing to SAP HANA Cloud.

-   SAP HANA Infrastructure Services artifacts required for SAP HANA Cloud are automatically generated by CAP build tools.

-   CAP handles multi-target application configurations, enabling hybrid development workflows that integrate on-premise and cloud resources.


Overall, CAP acts as a developer-friendly layer that simplifies building, testing, and deploying SAP HANA Cloud applications on SAP Business Technology Platform locally, in hybrid settings, or fully cloud-native.



<a name="loiof19c8e9650a341aca72c4e4f4726b17d__section_kns_cmz_ygc"/>

## ABAP Specifics in Supporting SAP HANA Cloud

ABAP supports SAP HANA Cloud within the SAP BTP through the SAP BTP ABAP environment. This is a cloud-optimized ABAP development and runtime environment based on SAP HANA Cloud, designed for building modern cloud applications and cloud extensions, especially for SAP S/4HANA Cloud and other SAP solutions.

Key points about ABAP's role in SAP HANA Cloud on SAP BTP:

-   The ABAP environment provides a cloud-native platform for developing, running, and extending ABAP applications using the ABAP RESTful Application Programming Model, optimized for SAP HANA Cloud.

-   Developers can create side-by-side extensions that run on SAP BTP, keeping the core SAP systems clean by decoupling custom code and enabling independent release cycles.

-   The ABAP environment supports seamless integration with SAP solutions including SAP S/4HANA Cloud, allowing ABAP extensions to access SAP HANA Cloud databases and services.

-   Modern development tooling like ABAP Development Tools \(ADT\) in Eclipse and the SAP Build lobby enhance productivity, including AI-assisted coding support via Joule for generating code, documentation, and testing.

-   The ABAP environment leverages the power of SAP HANA Cloud for in-memory data processing, real-time analytics, and scalable cloud-native application development.

-   The ABAP environment supports secure APIs and integration patterns for communication within SAP landscapes and external systems, enabling hybrid and cloud extension scenarios.


The SAP BTP ABAP environment with SAP HANA Cloud enables you to build intelligent, cloud-ready applications and extensions while leveraging existing ABAP knowledge and integrating tightly with SAP's cloud ecosystem.


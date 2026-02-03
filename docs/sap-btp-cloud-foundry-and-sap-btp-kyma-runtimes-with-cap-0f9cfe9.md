<!-- loio0f9cfe9c18654cd6bec5daa7b3188149 -->

# SAP BTP, Cloud Foundry and SAP BTP, Kyma Runtimes with CAP



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_yq2_mw3_jgc"/>

## Profiles in CAP: Development, Hybrid, and Production

CAP applications are design agnostic, and developers could focus on domain modeling and services without writing custom code. The development profile enables developers to design and test application prototypes with minimal setup. The mock variants of platform services and data enable developers to test without deploying CAP applications to SAP BTP. This helps customers to realize application prototypes in shorter cycles with low cost and later switch to hybrid/production profile by incrementally adding the required service bindings.

CAP's core strength lies in its focus on domain modeling. It allows developers to define business objects and their relationships using standardized data models, which can then be translated into services and applications.

See:

-   [Developing with CAP in the SAP BTP, Cloud Foundry and SAP BTP, Kyma Runtimes](developing-with-cap-in-the-sap-btp-cloud-foundry-and-sap-btp-kyma-runtimes-696ec23.md)
-   [CAP documentation: Domain Modeling](https://cap.cloud.sap/docs/guides/domain-modeling)



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_ubl_mw3_jgc"/>

## Multiple IDEs and Runtimes

CAP applications supports custom code development using Node.js or Java. You can choose Node.js or Java as a programming language and develop applications and use your preferred development environment such as:

-   [CDS Command Line Interface \(CLI\)](https://pages.github.tools.sap/cap/docs/tools/cds-cli)
-   [CDS Editors and IDEs](https://pages.github.tools.sap/cap/docs/tools/cds-editors)
    -   SAP Business Application Studio
    -   Visual Studio Code
    -   IntelliJ




<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_qqp_mw3_jgc"/>

## Integration with SAP BTP Services

CAP applications benefit out of the box integration to platform services and SAP BTP application services in the SAP Build portfolio, enabling developers to focus on application logic without spending additional effort on integration. Through simple configuration and service bindings, CAP applications seamlessly consume SAP HANA Cloud for persistence, SAP Authorization and Trust Management service for identity and authorization, and the Destination and Connectivity services for calling SAP and third‑party systems.

On the experience side, CAP services and SAP Fiori UIs are easily surfaced in SAP Build Work Zone, exposed as OData/REST APIs that SAP Build Apps can consume, and can trigger or drive SAP Build Process Automation workflows.

See:

-   [CAP Plugins and Enhancements](https://cap.cloud.sap/docs/plugins/)
-   [CAP: cds add command](https://cap.cloud.sap/docs/tools/cds-cli#cds-add)



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_exq_mw3_jgc"/>

## Microservice Development

CAP supports micro-service development and deployment to the SAP BTP, Cloud Foundry or SAP BTP, Kyma runtimes. You can develop loosely coupled microservices with separate lifecycles and different runtimes to achieve specific scalability requirements. Have in mind that microservices are not suitable for all use cases. Even though they have a lot of benefits, they are accompanied by complexity and performance losses. To decide whether to use microservices or not, see [CAP: Late-Cut Microservices](https://cap.cloud.sap/docs/guides/deployment/microservices#late-cut-microservices).

To deploy your CAP application as microservices, see [Microservices in CAP](https://cap.cloud.sap/docs/guides/deployment/microservices).



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_zvr_mw3_jgc"/>

## Consume Services as REST/OData/BAPI

CAP applications can consume data from other services or external sources:

-   OData and REST/OpenAPI services \(import definitions, mock locally, bind in hybrid/production\)
    -   Using services: [https://cap.cloud.sap/docs/guides/using-services/](https://cap.cloud.sap/docs/guides/using-services/)
    -   OpenAPI guide: [https://cap.cloud.sap/docs/guides/openapi/](https://cap.cloud.sap/docs/guides/openapi/)

-   SAP Cloud SDK \(Java/JavaScript\) for calling SAP solutions \(SAP S/4HANA, SAP SuccessFactors, and others\). See [https://sap.github.io/cloud-sdk/](https://sap.github.io/cloud-sdk/).
-   SAP API Business Hub for API definitions. See [https://api.sap.com/](https://api.sap.com/).



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_bqy_k2b_qgc"/>

## Multitenancy

Multitenancy in CAP is about building one Software-as-a-Service \(SaaS\) application \(provider\) that securely serves many customer accounts \(tenants\) on SAP BTP, while keeping each tenant’s identity, configuration, and data isolated. CAP provides standardized patterns and tooling that eliminate the need to build typical SaaS integration and operational components by hand.

See [CAP: Multitenancy](https://cap.cloud.sap/docs/guides/multitenancy/).



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_kjc_m2b_qgc"/>

## Extensibility

Extensibility in CAP is the ability to adapt and enhance a CAP application’s data model, service APIs, and behavior without forking or modifying the core solution. It supports both provider-controlled extensions \(delivered by the application team or partner\) and tenant-specific extensions in SaaS scenarios.

See [CAP: Extensibility](https://cap.cloud.sap/docs/guides/extensibility/).



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_z5s_mw3_jgc"/>

## Community

CAP applications benefit from large ecosystem of developers and community contribution. The large pool of developers with the required skills and packages from npm/Maven will accelerate development and reduce development costs. See:

-   [CAP Community in GitHub](https://github.com/cap-js-community)
-   [CAP in SAP Community](https://pages.community.sap.com/topics/cloud-application-programming)



<a name="loio0f9cfe9c18654cd6bec5daa7b3188149__section_mrh_nw3_jgc"/>

## Multiple Databases

CAP supports multiple databases, and customers can choose PostgreSQL or SAP HANA Cloud for persistence. CAP supports SQLite and H2 for development, which can be later replaced with PostgreSQL or SAP HANA Cloud by changing the development profile to production.

-   Official: SQLite \(development profile\) and SAP HANA/SAP HANA Cloud \(hybrid and production profiles\). See [https://cap.cloud.sap/docs/guides/databases/](https://cap.cloud.sap/docs/guides/databases/).
-   Community adapters exist for other SQL databases \(for example PostgreSQL\). See [CAP Community in GitHub](https://github.com/cap-js-community).


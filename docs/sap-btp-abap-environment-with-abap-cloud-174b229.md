<!-- loio174b2299be2941358c6e7dd64163aec3 -->

# SAP BTP ABAP Environment with ABAP Cloud

SAP BTP ABAP environment is a modern cloud offering for side-by-side extensions that uses the ABAP Cloud development model for cloud-ready extensions.



<a name="loio174b2299be2941358c6e7dd64163aec3__section_qmq_wt3_jgc"/>

## Aligned Development Model

The ABAP Cloud development model is used both in SAP BTP ABAP environment and natively within SAP S/4HANA. This enables a consistent development experience across side-by-side and on-stack extensions, allowing you to use the same tools, patterns, and lifecycle processes.

See [ABAP Cloud Development Model](https://help.sap.com/docs/abap-cloud/abap-cloud/abap-cloud-in-nutshell).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_mjm_m53_jgc"/>

## Reuse of Existing ABAP Code

Existing ABAP logic from legacy or on-premise systems can be adapted and reused in the SAP BTP ABAP environment using tools such as the Custom Code Migration App and the ABAP Test Cockpit \(ATC\). This reduces redevelopment effort and accelerates cloud adoption.

-   The Custom Code Migration App analyzes legacy code, identifies non-compliant elements such as unreleased APIs or obsolete statements, and helps prioritize necessary adaptations. See [Custom Code Analysis](https://help.sap.com/docs/btp/sap-business-technology-platform/custom-code-migration?version=Cloud).

-   The ABAP Test Cockpit validates the refactored code against ABAP Cloud rules to ensure code quality. See [ABAP Test Cockpit](https://help.sap.com/docs/btp/sap-business-technology-platform/abap-test-cockpit?version=Cloud).


Typical use cases include migrating stable custom logic, refactoring extensions to released APIs, and reusing business logic while modernizing UIs or integrations. See [ABAP Integration and Connectivity](https://help.sap.com/docs/abap-cloud/abap-integration-connectivity/abap-integration-and-connectivity).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_kc3_5t3_jgc"/>

## Seamless SAP S/4HANA Cloud Integration

SAP BTP ABAP Environment follows the same identity, access, and connectivity concepts as SAP S/4HANA Cloud, including SAP Identity Authentication Service, OData, and RFC. This ensures seamless interoperability and simplifies user, role, and permission management across systems.

ABAP Cloud provides a unified integration approach: connections are configured the same way regardless of the target system \(SAP BTP services, SAP S/4HANA Cloud, or approved external APIs\). Using the service consumption model, ABAP automatically generates client code and data structures from service definitions, allowing developers to focus on core business logic.

The environment also includes numerous pre-built communication scenarios—connectors to SAP BTP services and SAP S/4HANA Cloud APIs—to accelerate setup and follow cloud-compliant integration practices.

See [Integrating the ABAP Environment with SAP S/4HANA Cloud](https://help.sap.com/docs/btp/sap-business-technology-platform/integrating-abap-environment-with-sap-s-4hana-cloud?version=Cloud).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_k35_2wx_wgc"/>

## Partner Deployment Options



### Mutitenancy

Multitenancy in the ABAP environment enables application providers to develop and operate ABAP solutions in a software-as-a-service \(SaaS\) model on SAP BTP. Multiple consumers can be provisioned within the same ABAP system. The application provider is responsible for operating the solution and covering the required SAP BTP resources, while consumers use the software-as-a-service.

See [Multitenancy in the ABAP Environment](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/multitenancy-in-abap-environment?version=Cloud).



### Add-On Product as an On-Stack Option

An add-on product is a newly available software delivery option that allows partners to provide their solution as a software offering rather than a service. It is installed and operated directly in the customer’s own SAP BTP ABAP environment, giving the customer full control over lifecycle management, operations, and data governance. This option is particularly suited for scenarios where customers want to run the solution in their own environment or need to perform comprehensive enhancements using both developer extensibility and key user extensibility. The add-on product is made available to customers through the SAP Store, and partners must have a valid SAP PartnerEdge, Build contract to deliver their solution as an add-on product.

Customers using SAP BTP ABAP environment can browse for available add-on products in the SAP Store, register for the solution, and deploy it directly into their system using the Landscape Portal.

Both multitenant SaaS and add-on products options are fully supported and can be selected based on the customer’s and partner’s specific needs.



<a name="loio174b2299be2941358c6e7dd64163aec3__section_ejb_s53_jgc"/>

## Tool Support for Partners via Landscape Portal

The Landscape Portal acts as the central cockpit for partners to manage ABAP systems, tenants, and SaaS and add-on product operations. It offers system overviews, product and version lifecycle management, deployment pipelines, and monitoring functions. The portal also supports multitenant SaaS scenarios, enabling efficient administration across landscapes.

The Landscape Portal provides integrated tooling for partners to build, test, and deploy their products, making it a key enabler for delivering both SaaS and add-on products offerings.

See [Landscape Portal](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/landscape-portal?version=Cloud).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_inh_w53_jgc"/>

## Reuse Services

In ABAP, reuse services are standard, cross-application building blocks you can call \(via function modules, classes, or frameworks\) instead of reinventing common functionality. Common services like application jobs, logging, forms, emails, change documents, and workflow are provided out of the box, enabling rapid development and standardization.

These services are designed to be reused across applications, ensuring consistency, reliability, and reduced development effort.

See [Released Components and Objects](https://help.sap.com/docs/btp/sap-business-technology-platform/released-components-and-objects?version=Cloud) and [Understanding Available Technology](understanding-available-technology-c1f21a4.md).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_fqc_y53_jgc"/>

## Stability Checks Before the Upgrade

The SAP BTP ABAP environment provides a pre-upgrade option that enables customers and partners to verify the stability of their custom applications up to four weeks before the standard release upgrade. This helps detect potential regressions and ensures compatibility in a controlled environment.

The pre-upgrade option is executed on nominated non-production systems during a planned downtime. It mirrors the standard upgrade process, including hotfixes. To use this option, the relevant systems must be registered in the Landscape Portal.

See [Landscape Portal](https://help.sap.com/docs/sap-btp-abap-environment/landscape-portal/landscape-portal).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_g4k_fv3_jgc"/>

## SAP Fiori Launchpad Integration

The SAP Fiori launchpad is fully integrated with SAP BTP ABAP Environment, enabling you to run and expose UI applications without deploying a separate front-end server. Users can launch applications directly from the same system that hosts your ABAP code, providing a single, consistent entry point.

The launchpad offers role-based access, navigation, and personalization features, allowing users to organize applications according to their workflow. Predefined groups and catalogs help structure applications, while deep linking and parameterized launches ensure smooth navigation across multiple applications.

This integration simplifies development and deployment, reduces operational complexity, and provides a seamless user experience across the ABAP environment.

See [SAP Fiori Launchpad for SAP BTP ABAP Environment](https://help.sap.com/docs/btp/sap-fiori-launchpad-for-sap-btp-abap-environment/sap-fiori-launchpad-user-guide?version=Cloud).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_bnj_2ln_jgc"/>

## Code Quality and Security Compliance

High-quality ABAP Cloud code is ensured using ABAP Unit for dynamic tests and ABAP Test Cockpit \(ATC\) for static analysis.

ABAP Unit allows developers to write automated tests to verify functional correctness and prevent regressions. Test coverage should be measured before releasing transports, with high coverage helping to identify issues and improve robustness.

ABAP Test Cockpit checks code for syntax, performance, standards adherence, and ABAP Unit results. The default check variant `ABAP_CLOUD_DEVELOPMENT_DEFAULT` includes recommended checks for ABAP Cloud and executes unit tests. Variants can be customized, and ABAP Test Cockpit can be run manually or scheduled.

ABAP Test Cockpit integrates with transports, blocking release for high-priority findings. Exemptions can be requested for planned corrections or false positives.

The ABAP Test Cockpit Configurator app allows setting default variants, adjusting priorities, and defining handling of pseudo comments or pragmas.

See [Tips and Tricks \(ABAP Core\)](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/tips-and-tricks-abap-core-tools) and [Assuring Quality of ABAP Code](https://help.sap.com/docs/btp/sap-business-technology-platform/assuring-quality-of-abap-code?version=Cloud).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_ikb_hv3_jgc"/>

## Integrated Technical Monitoring Tools

The SAP BTP ABAP environment offers advanced monitoring capabilities to track system and application health, performance, and resource usage. It integrates seamlessly with CI/CD pipelines, enabling automated deployment, quality checks, and proactive issue detection. This ensures smooth operations and supports both developers and administrators in maintaining reliable applications.

See [https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/technical-monitoring](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/technical-monitoring).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_zrz_kgn_jgc"/>

## Security

Security in SAP BTP ABAP environment is natively aligned with SAP roles, authentication mechanisms, and governance models. Built-in controls and standards support secure development and operations, protecting applications and data while simplifying user and role management.

See [ABAP Development Tools for Eclipse: Security Guide](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/security-guide).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_ipn_3v3_jgc"/>

## Analytics and Core Data Services Support

SAP BTP ABAP environment leverages Core Data Services \(CDS\) to enable semantic data modeling and advanced analytics. As a developer, you can create high-performance analytical applications directly within the ABAP environment, using CDS views, annotations, and built-in analytical features without leaving the platform.

See [Integrating SAP Analytics Cloud](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/integrating-sap-analytics-cloud).



<a name="loio174b2299be2941358c6e7dd64163aec3__section_fzb_qv3_jgc"/>

## Full Transport and Lifecycle Management

In the SAP BTP ABAP environment, ABAP code can be transported and versioned using gCTS and abapGit:

-   gCTS is the modern, recommended mechanism for moving objects between ABAP systems within a global account and runs under the hood of the Manage Software Components application.
-   abapGit is an open-source Git client, supports use cases such as migrating on-premise code to the cloud, transferring code between cloud systems or to on-premise, exporting code when a system is decommissioned, and enabling distributed development or testing scenarios.

Both tools help maintain code quality, track changes, and support collaborative development across ABAP landscapes.

See [Transport Mechanisms](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/transport-mechanisms).


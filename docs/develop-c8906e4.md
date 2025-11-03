<!-- loioc8906e424aff42e2924a54ac46c5a10f -->

# Develop

There are certain requirements and key considerations for the develop phase across the main programming model aspects you have to take into account: building new applications and services, integrating with external systems, extending existing solutions, localizing content, and documenting outcomes.



<a name="loioc8906e424aff42e2924a54ac46c5a10f__section_v5v_nfs_dzb"/>

## Develop Applications, Extensions and Services with ABAP Cloud

You can build new applications and services from scratch or extend existing SAP or custom services in an upgrade-safe way. To create a new application or service, implement the domain-specific model and business logic that fit your selected use case. Domain-specific data models based on the [RAP architecture](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/development-business-configuration) blueprint bring extensibility as a built-in quality. Extensibility follows an opt-in approach: the original data model or service must explicitly enable each extensibility option.



<a name="loioc8906e424aff42e2924a54ac46c5a10f__section_cnt_3rw_vgc"/>

## Develop an Application from Scratch

Once you select the use case, transactional, analytical, or integration, implement the domain model and logic step by step:

1.  Model the domain: Define the domain-specific data model and its relationships. Align with the RAP architecture blueprint to enable upgrade-safe extensibility and consistent semantics.
2.  Implement business behavior: Add the domain-specific logic for validations, determinations, actions, and consistency management according to your transactional or analytical use case.
3.  Expose services: Define and bind services to make your domain capabilities consumable \(for example, via OData\). Ensure the service contract reflects your use case and performance needs.
4.  Secure access: Configure authorization and access control for services and data. Assign the proper scopes and roles to restrict access according to business and compliance needs.
5.  Build the UI: Develop SAP Fiori applications that consume your services. Use metadata-driven annotations to rapidly produce UIs and support navigation, search, and value helps.
6.  Ensure quality: Add automated tests and static checks to maintain quality throughout development and delivery.



<a name="loioc8906e424aff42e2924a54ac46c5a10f__section_kzc_ctw_vgc"/>

## Developing a Sustainable Test Strategy

Automated software testing is essential to ensure reliability, stability, and quality. It helps detect defects early and prevents regressions, allowing you to add features with confidence that existing functionality remains intact.

-   Test levels supported by ABAP Cloud: Unit tests, integration tests, and end-to-end validations to guarantee quality throughout the development process.
-   Test-driven development \(TDD\): ABAP Cloud supports test-driven development, enabling you to validate functional correctness in all stages of development.
-   Built-in capabilities: Use ABAP Unit to write executable tests for data models, behavior, and business events; use the ABAP Test Cockpit \(ATC\) to enforce coding standards and detect quality issues.



<a name="loioc8906e424aff42e2924a54ac46c5a10f__section_wxz_kcy_ygc"/>

## Develop SAP S/4HANA Cloud Extension Applications

When developing extensions for SAP S/4HANA Cloud, there are two fundamental extensibility options: on-stack and side-by-side.

On-stack extensibility refers to extensions that run directly within the SAP S/4HANA Cloud system – sharing the same database, system, and lifecycle. In this area:

-   Key-User Extensibility \(Low-Code\): Field extensions or simple custom logic created directly in SAP S/4HANA Cloud using ABAP Cloud and in-app tools.

-   Developer Extensibility \(Pro-Code\): Custom development directly in SAP S/4HANA Cloud using ABAP Cloud, which is cloud-ready and clean core compliant by design – this is technically ensured by the ABAP Cloud development model. In on-premise and private cloud systems, classic ABAP can still be used, but it is not clean core by default and therefore not recommended for new extensions.


Side-by-side extensibility uses SAP BTP where you deploy your extension applications. These extension applications run decoupled from the core system, with a separate runtime, lifecycle, and data center. This approach is ideal for:

-   Loosely coupled customer extensions and applications

-   Partner solutions, especially multitenant SaaS solutions or add-on product


You usually choose side-by-side development when:

-   Extensions need to be decoupled from the SAP S/4HANA Cloud lifecycle

-   New or external user groups require access without touching the core system

-   Independent workload and scalability are required

-   Extensions integrate multiple backend systems, also called hub scenarios

-   Partners aim to deliver multitenant SaaS or add-on product solutions


On-stack extensions remain relevant for deeply integrated SAP S/4HANA Cloud scenarios.



<a name="loioc8906e424aff42e2924a54ac46c5a10f__section_mml_35h_zgc"/>

## Recommendations

We recommend that you:

-   Connect your ABAP Cloud system to Eclipse with ABAP Development Tools \(ADT\).

-   Build OData services using RAP optimized for SAP HANA Cloud.

-   Perform static code analysis with ABAP Test Cloud, including Code Vulnerability Analyzer \(CVA\) security checks, without additional licensing fees.

-   Use central ABAP Test Cloud on SAP BTP to govern custom code across side-by-side developments, private cloud, and on-premise systems.

-   Leverage the Analyze Custom Code application for side-by-side code inspection, custom code migration, or clean core initiatives.


**Related Information**  


[ABAP Cloud: Background Concepts and Overview: Develop](https://help.sap.com/docs/abap-cloud/abap-cloud/abap-cloud-programming-model)

[ABAP Cloud: Background Concepts and Overview: Test](https://help.sap.com/docs/abap-cloud/abap-cloud/test)


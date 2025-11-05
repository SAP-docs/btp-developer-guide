<!-- loio210db8e7832b44359dd426dec11e5888 -->

# Build and Run ABAP Applications for Partners Who Are Independent Software Vendors



<a name="loio210db8e7832b44359dd426dec11e5888__section_bnr_tg2_zgc"/>

## Partner Deployment Options

As a partner, you can choose between multitenant SaaS and add-on product options for deploying your application. See the dedicated section at [SAP BTP ABAP Environment with ABAP Cloud](sap-btp-abap-environment-with-abap-cloud-174b229.md).



<a name="loio210db8e7832b44359dd426dec11e5888__section_jf4_hhz_ygc"/>

## Landscape Portal for Partners

The Landscape Portal is the central tool for partners to manage, deploy, and operate their solutions in SAP BTP ABAP environment. It supports both multitenant SaaS applications and add-on deployment options and provides all the necessary features for lifecycle management and product delivery.

Key functions and considerations:

-   Product building and deployment:

    -   To offer a solution in another global account in SAP BTP, whether it’s a different account you own \(for example, DEV vs. PROD\) or a customer account—a Product must be built using the Landscape Portal.

    -   The Product serves as the deployment unit and allows controlled installation and lifecycle management.

    -   Familiarity with the Landscape Portal features is essential for managing all deployment steps, including smaller intermediate steps that may be required for registration, building, and publishing.


-   Lifecycle management:

    -   abapGit is only recommended for importing development objects from on-premise systems to BTP or for backup purposes. It is not supported for transporting objects between BTP systems.

    -   For system-to-system transports within BTP \(for example, DEV → TEST\), use the Manage Software Components app, which relies on gCTS.

    -   Lifecycle management and tenant strategy \(multitenant vs. single tenant\) are independent decisions that must be defined separately.


-   Technical requirements and dependencies:

    -   At least one Software Component is required as a deployment unit for any solution.

    -   A registered ABAP namespace is mandatory for all objects in a Product; using Y\* or Z\* objects is only allowed if the solution remains within the same global account in SAP BTP and only the Manage Software Components app is used.

    -   Multiple global accounts in SAP BTP require building an add-on product to ensure proper deployment.



By consolidating all partner-related operations in the Landscape Portal, partners can efficiently manage solution delivery, maintain lifecycle governance, and ensure smooth deployment across multiple accounts and tenants.

**Related Information**  


[SAP BTP ABAP Environment with ABAP Cloud](sap-btp-abap-environment-with-abap-cloud-174b229.md "")

[Partner Reference Application 'Music Festival Manager'](https://github.com/SAP-samples/abap-partner-reference-application)

[SAP Community: Building Partner Products on SAP BTP ABAP Environment](https://community.sap.com/t5/devtoberfest/building-partner-products-on-sap-btp-abap-environment/ev-p/13804921)


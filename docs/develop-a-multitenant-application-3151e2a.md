<!-- loio3151e2a4f6554d5192f2227c138388ee -->

# Develop a Multitenant Application

Multitenancy in the SAP BTP, ABAP environment enables independent software vendors or partners, which are the application providers, to develop and operate ABAP solutions as software as a service \(SaaS\). It leverages the SAP BTP infrastructure while hosting several consumers on the same ABAP system. The resources on SAP BTP consumed by the solution are paid for by the application provider.

Application consumers, which are the end customers of the provider, subscribe to a provider’s multitenant application and use it in a specific consumer subaccount, which is called tenant. Consumers access the provider’s SaaS application via a consumer-specific URL. Consumers cannot see the data of other consumers and Identity and Access Management is kept isolated between different tenants.

The multitenant application is deployed to the provider subaccount and serves as the entry point for the consumer-specific URLs, so that requests are routed to the corresponding consumer tenant in the ABAP system. Only after the multitenant application has been deployed, the application will be available for subscription to consumers. See [Developing Multitenant Applications in the ABAP Environment](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/developing-multitenant-applications-in-abap-environment).

The ABAP system used to serve the application to the consumers is provisioned in the provider subaccount during the first subscription. See [Creating an ABAP System](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/creating-abap-system).

Different tenants are created as separate clients in the system. Tenants in the ABAP system have different capabilities represented by the tenant business type and a lifecycle status. The ABAP system contains by default a tenant used by the application provider \(client 100\) for system-level operations like the import of software components to the system. For each subscription to the multitenant application, a tenant used by the consumer \(client \>= 200\) is created. If any consumer tenants still exist in the ABAP system, the system cannot be deleted.

The Landscape Portal functions as a central plane for tenant management that allows providers to perform lifecycle management operations such as add-on updates, creating test tenants or support users and more. For more information on how to access and use the Landscape Portal, see [Landscape Portal](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/landscape-portal).

Multitenancy in the SAP BTP, ABAP environment is technically based on client-dependent database tables. Developers need to make sure to define their custom database tables with the CLIENT field and the respective delivery class. The ABAP SQL access takes the current CLIENT of the logged-on user automatically into consideration. See [Multitenancy Development Guideline](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/multitenancy-development-guideline).


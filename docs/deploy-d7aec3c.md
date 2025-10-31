<!-- loiod7aec3cb76c24cc8b4f1869633bfdfe7 -->

# Deploy

After you have developed your application or service and have written the necessary tests, it's time to deploy and transport them to SAP BTP ABAP environment using proven ABAP lifecycle management. CI/CD, git integration, and a dedicated transport environment for key users on the SAP Fiori launchpad are supported out of the box.



<a name="loiod7aec3cb76c24cc8b4f1869633bfdfe7__section_alv_mtw_bzb"/>

## Common Setup

The basic deployment unit is the software component, managed via the Manage Software Components administration application. Each software component has an automatically managed git repository via gCTS for transport management. You can import software components into test and production systems.

This common setup is sufficient for customers operating their own applications.

For more information, see:

-   [Software Components](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/software-components)

-   [Manage Software Components](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/manage-software-components)




<a name="loiod7aec3cb76c24cc8b4f1869633bfdfe7__section_xj3_ntw_bzb"/>

## Additional Considerations for Partners

Partners can offer and deploy their solutions in two different ways within the SAP BTP ABAP environment:

-   Multitenant SaaS solution

    -   You offer your solution as a **cloud service** operated in your own global accout in SAP BTP

    -   Each customer **subscribes** to your service

    -   You are responsible for **development, operations, monitoring**, and **infrastructure costs**

    -   Customers can adapt the solution using **key-user extensibility** \(tenant-aware adaptations such as custom fields and logic\)


-   Add-on product

    -   You offer your solution as an **add-on product**

    -   Your customers must have their **own instance of the SAP BTP ABAP environment**

    -   The **installation and lifecycle management** \(upgrades, patches\) are in the **customer’s responsibility**

    -   The installation is performed by the customer **via the Landscape Portal**, which is part of the SAP BTP ABAP environment

    -   Customers can **enhance and extend** your product using **ABAP Development Tools \(ADT\)** and **developer extensibility**



For both delivery models, partners build their solutions based on **software components** and manage them through the **Landscape Portal**. The Landscape Portal provides a unified environment to:

-   Build, register, and publish partner products,

-   Manage software lifecycles such as installation, upgrades, and patches, and

-   Support the setup of **multitenant SaaS** solutions or **add-on products** for customers and other partners.


For more information about managing partner solutions, see [Landscape Portal](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/landscape-portal).

**Related Information**  


[ABAP Cloud: Background Concepts and Overview: Deploy](https://help.sap.com/docs/abap-cloud/abap-cloud/lifecycle-management)


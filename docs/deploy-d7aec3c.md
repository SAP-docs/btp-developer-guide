<!-- loiod7aec3cb76c24cc8b4f1869633bfdfe7 -->

# Deploy



<a name="loiod7aec3cb76c24cc8b4f1869633bfdfe7__section_alv_mtw_bzb"/>

## Common Setup

The deployment of developed ABAP Cloud objects and entire applications is supported by administration apps delivered with SAP BTP, ABAP environment. The respective ABAP systems run on Gardener or Kubernetes-based infrastructure, but such technical details are hidden for developers and administrators. The important part of the deployment strategy is the definition and setup of the respective System Landscape. A typical system landscape consists of three ABAP systems for development, test and productive use. See [System Landscape/Account Model](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/concepts#loio4ca756395fc24e56a42b77632a6bd862).

The basic entity for the deployment are software components. Software components are maintained with the administrators app Manage Software Components. A hidden Git repo is automatically managed per software component based on gCTS for transport management. Software components can be imported into test and productive systems. This process can be automated via Piper pipelines including steps like automated test using ABAP Test Cockpit \(ATC\). You can also use SAP Cloud Transport Management to handle the propagation of your changes in SAP BTP, ABAP environment.

The common setup is sufficient for customers to run their own applications.

For more information, see:

-   [Software Components](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/software-components)

-   [Manage Software Components](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/manage-software-components)

-   [ABAP Environment Pipeline](https://www.project-piper.io/pipelines/abapEnvironment/introduction/)




<a name="loiod7aec3cb76c24cc8b4f1869633bfdfe7__section_xj3_ntw_bzb"/>

## Additional Considerations for Partners

There are two different models for offering and deploying your solution.

1.  As a multitenant SaaS solution:

    -   You offer a cloud service

    -   Your customers can subscribe to your service and get an own tenant in your central provider system

    -   The application monitoring is in your responsibility and so is managing the infrastructure costs

    -   Even for this scenario, Field Extensibility and Custom Logic is offered for key users on customer side \(tenant-aware\)


2.  As an installable product:

    -   You offer the product as an Add-on; the product can also be an SDK

    -   Your customers need to have an own SAP BTP, ABAP environment instance

    -   The installation of the product and patches is in the responsibility of your customers

    -   The installation will be possible via Landscape Portal on customer side

    -   The customer can extend your product via ADT. See the developer extensibility option in the [Development Use Cases](understanding-available-technology-c1f21a4.md#loio4efd0bc86ade42c28bf4c4c8dbc4451b) page.



For both models, partners can build solutions based on software components with the help of the Landscape Portal to set up multitenant SaaS solutions or to offer installable products like SDKs for other customers and partners.

The Landscape Portal is a collection of administrator apps and is part of the SAP BTP, ABAP environment. See [Landscape Portal](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/landscape-portal).


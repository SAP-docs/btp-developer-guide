<!-- loioeb7420a2c752457687fb39ed01509ef5 -->

# Tutorials for SAP Cloud Application Programming Model

The business scenario of the Incident Management application helps a company like ACME, a company dealing with electronics, that hires call center support representatives to process and manage customer incidents. A call center support representative, called a processor, receives a phone call from an existing customer and creates a new incident on behalf of the customer. The newly created incident is based on the customer complaint received during the phone call so the call center support representative also adds the conversation with the customer to the incident.

This application enables the interaction between the members of the support team who are working on the customer's incident. The application is designed to allow support team memebers to initiate incident reports which are then processed by other support team members.

The tutorials are built using the Incident Management application. Where applicable, these tutorials use the free plans of the respective services.

Before you start using the services or runtimes, you need to manage your entitlements and add quotas to your subaccounts. See [Entitlements and Quotas](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/00aa2c23479d42568b18882b1ca90d79.html "When you purchase an enterprise account, you’re entitled to use a specific set of resources, such as the amount of memory that can be allocated to your applications.") :arrow_upper_right:.

Note that if you want to try out services for free, you need to select free tier service plan, if available. For a list of free services, check the Service Catalog at [SAP Discovery Center](https://discovery-center.cloud.sap/servicessearch/Free%20Tier/).

> ### Note:  
> There is also a free plan for the SAP BTP, Cloud Foundry runtime and SAP BTP, Kyma runtime. To use the free plan of the runtimes, you have to configure the entitlements in the SAP BTP cockpit. You have one free plan for each runtime per global account and you can assign it to one subaccount at a time.

The tutorials are organized in the following way.

-   Basic groups of tutorials for the Incident Management application. See:

    -   [Develop a Full-Stack CAP Application](https://developers.sap.com/group.cap-application-full-stack.html)

    -   [Deploy a Full-Stack CAP Application in SAP BTP, Cloud Foundry Runtime](https://developers.sap.com/group.deploy-full-stack-cap-application.html)

    -   [Deploy a Full-Stack CAP Application in SAP BTP, Kyma Runtime](https://developers.sap.com/group.deploy-full-stack-cap-kyma-runtime.html)


-   Separate tutorials for the additional modules based on the Incident Management application.

-   All these tutorials are grouped together in the [Develop a Full-Stack CAP Application Following the SAP BTP Developer’s Guide](https://discovery-center.cloud.sap/missiondetail/4327/4608/) mission in the SAP Discovery Center.




<a name="loioeb7420a2c752457687fb39ed01509ef5__section_w5q_vjl_2zb"/>

## Develop a Full-Stack CAP Application

The [Develop a Full-Stack CAP Application](https://developers.sap.com/group.cap-application-full-stack.html) group of tutorials covers the following steps for developing the Incident Management sample application:

-   Setting up the development environment. See [Set Up SAP Business Application Studio](https://developers.sap.com/tutorials/set-up-bas.html).

-   Building a CAP application with SAP Fiori elements user interface and a custom logic. See:

    -   [Build a CAP Application](https://developers.sap.com/tutorials/build-cap-app.html)

    -   [Add SAP Fiori Elements UIs](https://developers.sap.com/tutorials/add-fiori-elements-uis.html)

    -   [Add Custom Logic](https://developers.sap.com/tutorials/add-custom-logic.html)


-   Adding local launchpad, authorization, tests for local development and preparing for production. See:

    -   [Use a Local Launch Page](https://developers.sap.com/tutorials/use-local-launch-page.html)

    -   [Add Authorization](https://developers.sap.com/tutorials/add-authorization.html)

    -   [Add Test Cases](https://developers.sap.com/tutorials/add-test-cases.html)

    -   [Prepare for Production](https://developers.sap.com/tutorials/prep-for-prod.html)





<a name="loioeb7420a2c752457687fb39ed01509ef5__section_lgt_2kl_2zb"/>

## Deploy a Full-Stack CAP Application in SAP BTP, Cloud Foundry Runtime

The [Deploy a Full-Stack CAP Application in SAP BTP, Cloud Foundry Runtime](https://developers.sap.com/group.deploy-full-stack-cap-application.html) group of tutorials covers the following steps for deploying the Incident Management application in the SAP BTP, Cloud Foundry runtime:

-   Deploying the application in a productive account in SAP BTP, Cloud Foundry runtime. See

    -   [Prepare for Deployment in the SAP BTP, Cloud Foundry Runtime](https://developers.sap.com/tutorials/prepare-btp-cf.html)

    -   [Deploy in SAP BTP, Cloud Foundry Runtime](https://developers.sap.com/tutorials/deploy-to-cf.html)

    -   [Assign the User Roles](https://developers.sap.com/tutorials/user-role-assignment.html)


-   Using SAP Build Work Zone, standard edition. See [Integrate Your Application with SAP Build Work Zone, Standard Edition](https://developers.sap.com/tutorials/integrate-with-work-zone.html).

-   Setting up continuous integration and delivery pipeline in SAP BTP. See [Set Up a CI/CD Pipeline](https://developers.sap.com/tutorials/set-up-cicd.html).




<a name="loioeb7420a2c752457687fb39ed01509ef5__section_kvs_3lj_hzb"/>

## Deploy a Full-Stack CAP Application in SAP BTP, Kyma Runtime

The [Deploy a Full-Stack CAP Application in SAP BTP, Kyma Runtime](https://developers.sap.com/group.deploy-full-stack-cap-kyma-runtime.html) group of tutorials covers the following steps for deploying the Incident Management application in the SAP BTP, Kyma runtime:

-   Deploying the application in a productive account in SAP BTP, Kyma runtime. See

    -   [Prepare for Deployment in the SAP BTP, Kyma Runtime](https://developers.sap.com/tutorials/prepare-btp-kyma.html)

    -   [Deploy in SAP BTP, Kyma Runtime](https://developers.sap.com/tutorials/deploy-to-kyma.html)

    -   [Assign the User Roles](https://developers.sap.com/tutorials/user-role-assignment.html)


-   Using SAP Build Work Zone, standard edition. See [Integrate Your Application with SAP Build Work Zone, Standard Edition](https://developers.sap.com/tutorials/integrate-with-work-zone.html).

-   Setting up continuous integration and delivery pipeline in SAP BTP. See [Set Up a CI/CD Pipeline for SAP BTP, Kyma Runtime](https://developers.sap.com/tutorials/set-up-cicd-kyma.html).




<a name="loioeb7420a2c752457687fb39ed01509ef5__section_ud1_vjl_2zb"/>

## Additional Modules

The tutorials for the additional modules are built on top of the basic groups of tutorials. Depending on what you need, you can pick up different modules. For each of these modules, the basic groups of tutorials is a prerequisite. The modules are:

-   [Connect to a Remote Service Using the SAP Destination Service](https://github.com/SAP-samples/btp-developer-guide-cap/blob/main/documentation/remote-service/README.md).

-   [Set Up Eventing Using the SAP Event Mesh Service](https://github.com/SAP-samples/btp-developer-guide-cap/blob/main/documentation/eventing/README.md).

-   [Set Up Audit Logging Using the SAP Audit Log Service](https://github.com/SAP-samples/btp-developer-guide-cap/blob/main/documentation/auditlog/readme.md).

-   [Configure Authorization and Authentication Using the Authorization Management Service and the Identity Authentication Service](https://github.com/SAP-samples/btp-developer-guide-cap/blob/main/documentation/xsuaa-to-ams/README.md).

-   [Implement Change Tracking](https://github.com/SAP-samples/btp-developer-guide-cap/blob/main/documentation/change-tracking/README.md).



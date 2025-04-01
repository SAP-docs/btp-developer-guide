<!-- loio41184aabb5d04839b8bd29564aa850e5 -->

# Using Multitarget Applications to Manage Dependencies

One challenge of moving into the cloud is deploying applications that consist of multiple interconnected components.

In Cloud Foundry, we recommend that you develop multitarget applications that let you package those components into one bundle, and deploy and manage them all at once. Cloud applications often come with a lot of heterogeneity, which is one of the key strengths of cloud development, allowing for agility, resilience, and the rapid development of new features. However, it also increases the complexity of cloud applications, which:

-   Usually consist of multiple interdependent software modules
-   Are written in different programming languages using multiple development tools
-   Might involve different products
-   May be deployed to multiple target runtimes

A combined lifecycle lets you deploy all parts together, automatically, and in the right order, and manage the configuration of the complete solution. You can achieve such a combined lifecycle by developing multitarget applications. Each multitarget application has the following characteristics:

-   One archive file that includes all modules and a description of the dependencies
-   Can be delivered, transported, linked to SAP software components, and deployed
-   The process can be automated in a continuous integration pipeline

The multitarget application archive contains all required application types and configurations, as well as a deployment descriptor file. It is intended to be used as a generic artifact that can be deployed and managed on several SAP BTP subaccounts. For example, you can use one multitarget application archive in your development subaccount and reuse it in your production subaccounts.

As all interdependencies are part of the archive file, it's easy to pass multitarget applications from development to operations. All required information for deployment is provided during the development process. Due to the benefits provided by applying the multitarget application approach, it is also part of the SAP Cloud Application Programming Model.

![](images/sap_cp_lm_mta_926ef9d.png)

> ### Recommendation:  
> The approach isn't mandatory for applications that are running on SAP BTP – you can also develop without applying it. Without the multitarget application approach, you'll need to manually deploy your application artifacts, for example by triggering the deployment from SAP Business Application Studio or manually uploading artifacts via SAP BTP cockpit.
> 
> We recommend that you use multitarget applications in the following cases:
> 
> -   You're developing a business application composed of several different parts – apps, services, content, and others – that you want to manage as a single unit.
> 
> -   Your business application has dependencies to external resources, such as backing services \(database, messaging, and so on\), APIs, and configurations from other applications.
> 
> -   Your business application has a certain default configuration, for example memory, disk, number of individual app instances, environment variables, service plans, and others.

For more conceptual information about multitarget applications and detailed step-by-step instructions, see [Multitarget Applications in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/d04fc0e2ad894545aebfd7126384307c.html "A Multitarget application (MTA) is essentially a single application that consists of multiple parts. These parts are created using various technologies and share the same lifecycle.") :arrow_upper_right:.

There are several options to create multitarget application archives:

-   If you use SAP Business Application Studio, see [MTA Development](https://help.sap.com/docs/bas/sap-business-application-studio/mta-development).

-   If you use SAP Web IDE Full-Stack, you can use multitarget application templates for Cloud Foundry applications, where the descriptor file is maintained automatically, for example, whenever you add a new module in the SAP Web IDE.

-   If you have development modules from other sources, you can use the multitarget application archive builder, a Java-based command-line tool that builds modules and packages them into a deployable multitarget application archive, together with a deployment descriptor. It is available for download from SAP Development Tools \(see [https://tools.hana.ondemand.com/\#cloud](https://tools.hana.ondemand.com/#cloud)\).

-   If you use Continuous Integration and Delivery \(CI/CD\), you can let the pipeline perform an automated build of your changes pushed to your central source code repository. The outcome can also be an MTA archive. For more information, see [Delivering Applications](https://help.sap.com/viewer/df50977d8bfa4c9a8a063ddb37113c43/Cloud/en-US/b39bae31d35d4d039431973116363d57.html#loiob39bae31d35d4d039431973116363d57 "In enterprise environments, use a managed and automated delivery approach – because it is less error-prone and creates repeatable outcomes. Furthermore, you can apply governance and central control of the propagation of your changes towards your production environment.") :arrow_upper_right:.



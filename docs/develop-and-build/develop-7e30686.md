<!-- loio7e306865dadb4473a4d66d81b7d83004 -->

# Develop

SAP BTP offers various tools and programming languages for application development. You might also want to consider to integrate your application with other solutions.

Depending on your use case and the skill set of your developers, you can choose the runtime of your choice:

**Environment options**


<table>
<tr>
<th valign="top">

 

</th>
<th valign="top">

Cloud Foundry

</th>
<th valign="top">

Kyma

</th>
<th valign="top">

ABAP

</th>
</tr>
<tr>
<td valign="top">

**Benefits**

</td>
<td valign="top">

-   Simplified developer experience for business application development
-   Large choice of programming languages
-   Intuitive “code-to-container” packaging and deployment, managed by the platform
-   Platform-managed application security patching and updates
-   Automatic application routing, load balancing, health checks, and multilevel self-healing
-   Support for CAP – an opinionated business app development framework



</td>
<td valign="top">

-   Take full advantage of the advanced features and rich ecosystem of Kubernetes
-   Free choice of programming languages and models \(containerized deployments\)
-   Combines microservices and serverless functions
-   Built-in, managed service mesh based on Istio, and other cloud-native open-source modules to reduce the development effort
-   Built-in, managed event mesh
-   Managed infrastructure: day-2 operations, security patches, and updates
-   Full administrator access
-   Refined horizontal and vertical automatic scalability
-   Dedicated application runtime
-   Zero downtime infrastructure setup by default
-   Support for CAP – an opinionated business app development framework
-   Support for on-premise connectivity



</td>
<td valign="top">

-   ABAP programming language
-   Fast prototyping with ABAP RESTful Programming Model \(RAP\)
-   Integrated development lifecycle
-   Reuse existing on-prem ABAP assets



</td>
</tr>
<tr>
<td valign="top">

**Additional Information**

</td>
<td valign="top">

[Comparison: SAP BTP, Kyma Runtime and SAP BTP, Cloud Foundry Runtime](https://help.sap.com/docs/btp/comparison-btp-runtimes/runtime-comparison?version=Cloud)

</td>
<td valign="top">

[Comparison: SAP BTP, Kyma Runtime and SAP BTP, Cloud Foundry Runtime](https://help.sap.com/docs/btp/comparison-btp-runtimes/runtime-comparison?version=Cloud)

</td>
<td valign="top">

[Development in the ABAP Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/development-in-abap-environment?version=Cloud)

</td>
</tr>
<tr>
<td valign="top">

**Shared Benefits**

</td>
<td valign="top" colspan="3">

-   No infrastructure vendor lock-in

-   Build scalable multitenancy business applications \(SaaS\)

-   Out-of-the-box consumption of SAP and hyperscaler services

-   Built on industry standards and open technology




</td>
</tr>
<tr>
<td valign="top">

**Good For**

</td>
<td valign="top">

-   Managed build-on approach
-   Enterprise-grade business applications and services
-   Cloud-native web applications and services
-   Scalable, microservice-based applications
-   Small to medium extensions built with CAP/low-code tooling



</td>
<td valign="top">

-   Open build-on approach
-   Enterprise-grade applications
-   Cloud-native development of apps and services
-   Low latency infra-services communication
-   Reduced infrastructure management effort
-   Highly scalable, microservice-based applications
-   Applications built with CAP



</td>
<td valign="top">

-   User-centric process extensions
-   Robust, transactional cloud applications
-   Migrating and adapting add-ons to the cloud
-   Reusing existing on-premise ABAP code
-   Enabling ABAP developers to go to the cloud



</td>
</tr>
<tr>
<td valign="top">

**Skills**

</td>
<td valign="top">

-   Any major programming languages
-   SAP Fiori/UI5 and SAP HANA



</td>
<td valign="top">

-   Kubernetes knowledge
-   Docker
-   NodeJS or Python for serverless functions
-   Any major programming language
-   SAP Fiori/UI5 and SAP HANA



</td>
<td valign="top">

-   Ability to write modern ABAP code
-   Core data services
-   SAP Fiori/UI5 and SAP HANA



</td>
</tr>
</table>



Metering:

-   Cloud Foundry runtime: Metering starts when you start using the runtime memory, for example, when you deploy an application.

    If your global account uses the consumption-based commercial model and you want to understand how the consumption of SAP BTP, Cloud Foundry runtime is calculated, see[Consumption Monitoring](https://help.sap.com/docs/cf-runtime/cloud-foundry-runtime/monitoring-and-troubleshooting?version=Cloud) in the SAP BTP, Cloud Foundry runtime documentation.

-   Kyma runtime: Metering starts when you enable the Kyma runtime. This triggers the creation of a dedicated Kubernetes cluster, and the cluster is metered from the start, before you have deployed any applications.




For Cloud Foundry , we recommend that you create multitarget applications for managing dependencies more easily. For more information, see [Using Multitarget Applications to Manage Dependencies](using-multitarget-applications-to-manage-dependencies-41184aa.md).

For best practices, guidelines and step-by-step instructions, see [Development](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/c2fec62b49fa43b8bd945c85ecc2e5bd.html "Develop and run business applications on SAP Business Technology Platform (SAP BTP) using our cloud application programming model, APIs, services, tools, and capabilities.") :arrow_upper_right:.



<a name="loio7e306865dadb4473a4d66d81b7d83004__section_fnv_kb3_r2b"/>

## Defining Development Guidelines

To ensure consistency and foster collaboration between developers, we recommend that you define guidelines that include standards for programming principles, code styles, and naming conventions.

SAP provides the following official guidelines:

-   [SAPUI5 Guidelines](https://sapui5.netweaver.ondemand.com/sdk/#/topic)

-   [SAP Fiori Design Guidelines](https://experience.sap.com/fiori-design/)




<a name="loio7e306865dadb4473a4d66d81b7d83004__section_lbt_hjp_dcc"/>

## SAP BTP and Third-Party Cookies

The deprecation of third-party cookies by browser manufacturers might impact applications running on SAP BTP. For example, logon scenarios in your application might fail due to session management and authentication issues.

Third-party cookies are set by domains other than the one a user is directly visiting. They are commonly used for online advertising and tracking user behavior across multiple websites. In SAP BTP, SAP uses third-party cookies for service management and single sign-on.

Prepare your applications for the third-party cookie deprecation and test them. See [Preparing and Testing Your Solution for Third-Party Cookie Deprecation](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/70d545de1931484c9efbc2cda6519fa7.html).

All the available solutions are listed in the SAP Note [3409306 - Removal of Third-Party Cookies in Google Chrome and Microsoft Edge Browser](https://me.sap.com/notes/3409306).


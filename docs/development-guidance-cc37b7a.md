<!-- loiocc37b7a428164c5fa619fd6f21080e3f -->

# Development Guidance

In SAP BTP, you have the choice between several runtimes. If you want to run ABAP, you'll choose the [SAP BTP, ABAP environment](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/abap-environment).

The non-ABAP runtime options are SAP BTP, Cloud Foundry runtime and SAP BTP, Kyma runtime. Both runtimes can be used to host and run your custom code, while at the same time being connected to SAP BTP Multi-Cloud Services and your on-premise systems. Depending on your use case and the skill set of your developers, choose the runtime that fits your needs. See [Comparison: SAP BTP, Kyma Runtime and SAP BTP, Cloud Foundry Runtime](https://help.sap.com/docs/btp/comparison-kyma-runtime-and-cloud-foundry-runtime/runtime-comparison?version=Cloud).



<a name="loiocc37b7a428164c5fa619fd6f21080e3f__section_lbt_hjp_dcc"/>

## SAP BTP and Third-Party Cookies

The deprecation of third-party cookies by browser manufacturers might impact applications running on SAP BTP. For example, logon scenarios in your application might fail due to session management and authentication issues.

Third-party cookies are set by domains other than the one a user is directly visiting. They are commonly used for online advertising and tracking user behavior across multiple websites. In SAP BTP, SAP uses third-party cookies for service management and single sign-on.

Prepare your applications for the third-party cookie deprecation and test them. See [Preparing and Testing Your Solution for Third-Party Cookie Deprecation](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/70d545de1931484c9efbc2cda6519fa7.html).

All the available solutions are listed in the SAP Note [3409306 - Removal of Third-Party Cookies in Google Chrome and Microsoft Edge Browser](https://me.sap.com/notes/3409306).



<a name="loiocc37b7a428164c5fa619fd6f21080e3f__section_jtn_x2p_czb"/>

## ABAP Cloud

ABAP Cloud is designed to develop applications and services with a standardized architecture on an enterprise scale. The technological core of ABAP Cloud provides the frameworks, design time, and runtime architecture to develop and run ABAP Cloud applications, services, and extensions in all products that support ABAP Cloud with out-of-the-box qualities like scalability, multitenancy, extensibility, and upgrade stability. See [ABAP Cloud](abap-cloud-9aaaf65.md).



<a name="loiocc37b7a428164c5fa619fd6f21080e3f__section_anx_x2p_czb"/>

## SAP Cloud Application Programming Model

The SAP Cloud Application Programming Model \(CAP\) is a framework of languages, libraries, and tools for building enterprise-grade services and applications. It guides developers along a path of proven best practices and a great wealth of out-of-the-box solutions to recurring tasks. See [SAP Cloud Application Programming Model](sap-cloud-application-programming-model-696ec23.md).


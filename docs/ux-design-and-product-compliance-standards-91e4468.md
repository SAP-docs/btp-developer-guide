<!-- loio91e44681019d4e499a2c173672a05f78 -->

# UX Design and Product Compliance Standards

Applications built on SAP BTP need to provide a consistent and compliant user experience across runtimes, while giving developers flexibility to address diverse business requirements. The SAP Fiori design language is the standard for achieving this goal.

From a development perspective, there are three main recommendations for creating user interfaces:

-   SAP Fiori elements
-   Flexible Programming Model
-   Freestyle SAPUI5

![](images/User_Interface_116cf74.png)



<a name="loio91e44681019d4e499a2c173672a05f78__section_bjn_qrz_wgc"/>

## SAP Fiori Elements

SAP Fiori elements is a framework on top of SAPUI5 that accelerates the development of SAP Fiori applications by providing predefined templates and patterns based on OData services, ensuring consistent UI design and functionality without extensive coding. Provides the fastest development speed, lowest total cost of ownership, and out-of-the-box compliance with SAP Fiori design guidelines.



### Floorplans

Floorplans in SAP Fiori elements are standardized UX design templates that guide the layout and behavior of applications. They include variations like List Report, Object Page, and Overview Page, each serving specific business needs and ensuring a cohesive user experience across SAP applications.



### Building Blocks

Building blocks in SAP Fiori Elements are reusable UI components that encapsulate common functionalities, such as data visualization or form entry. They streamline development by enabling consistent application behavior and enhancing modular design within SAP Fiori applications.



<a name="loio91e44681019d4e499a2c173672a05f78__section_swt_1sz_wgc"/>

## Flexible Programming Model

A hybrid approach that extends SAP Fiori elements with custom UI logic where needed. Recommended for applications that follow standard floorplans but require selective flexibility \(for example, custom actions, advanced visualizations\). Balances reuse of compliant templates with targeted freedom for developers.



### Extensions

Standard templates offer multiple extension points, allowing you to enhance them with custom elements.



### Custom Pages

When developing custom pages, leveraging the SAP Fiori elements base component enables the use of building blocks and additional features like routing, all readily accessible.



<a name="loio91e44681019d4e499a2c173672a05f78__section_xsk_3sz_wgc"/>

## Freestyle SAPUI5

Full control over UI logic and layout using SAPUI5 as a UI framework. Recommended only when business scenarios demand highly customized interfaces that cannot be covered by SAP Fiori elements or the flexible programming model. Requires higher development and maintenance effort but still benefits from the Horizon theme and SAP Fiori guidelines.



### SAP Fiori Tools

SAP Fiori tools provide many capabilities to increase the efficiency of developing SAP Fiori applications using either SAP Fiori elements or the freestyle SAPUI5 approach. SAP Fiori tools, together with SAP Fiori elements, reduce development time, maintenance costs, and leverage the advantages of a metadata-driven UI. SAP Fiori tools include the following:

-   Application Wizard for the initial creation of an application.
-   Service modeler for viewing the data model.
-   \(SAP Fiori elements only\) XML and form-based editor for maintaining of annotations.
-   \(SAP Fiori elements only\) Application page structure and ability to configure the SAPUI5 flexibility settings.
-   \(SAP Fiori elements only\) Guided development for implementing features.



<a name="loio91e44681019d4e499a2c173672a05f78__section_hls_ftz_wgc"/>

## Compliance Standard

Applications designed with the recommended UX approaches automatically inherit a broad set of SAP product compliance standards. These ensure that applications are enterprise-ready without requiring developers to implement them from scratch.



### Out-of-the-Box Compliance

By using SAP Fiori elements or the flexible programming model on top of SAPUI5 with Horizon theme, applications automatically comply with:

-   Accessibility \(WCAG 2.2\) – support for screen readers, ARIA roles, keyboard navigation.
-   SAP Fiori design guidelines – consistent floorplans, navigation, and semantics.
-   Responsive design – adaptive layouts for desktop, tablet, and mobile.
-   Performance best practices – SAPUI5 optimizations for data loading and rendering.
-   Security standards – built-in protection \(XSRF, CSRF tokens\), secure authentication with Identity Authentication service/SAP Authorization and Trust Management service.

To be fully compliant, applications must also:

-   Expose OData V4 services \(CAP, ABAP Cloud, or Node.js\) with proper annotations.
-   Enable internationalization \(i18n\) for texts and labels.
-   Respect SAP Fiori design guidelines when customizing UI \(colors, icons, navigation\).


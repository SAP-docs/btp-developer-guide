<!-- loio6d2cbe949ab84e13ba8999fe98c2f43e -->

# Mission: Develop a Multitenant CAP Application

SAP BTP provides a multitenant functionality that allows application providers to own, deploy, and operate tenant-aware applications for multiple consumers, with reduced costs. For example, the application provider upgrades the application for all your consumers instead of performing each update individually, or share resources across multiple consumers. The application consumers launch the applications using consumer-specific URLs, and configure certain application features.

With tenant-aware applications, you can:

-   Separate data securely for each tenant

-   Save resources by sharing them among tenants

-   Update applications efficiently, in a single step


A business solution is typically a multitenant application that consists of UI modules, business logic and a connection to a database. Unlike other applications that are integrated into SAP Build Work Zone, it also contains the site design-time definitions such as tiles, roles, spaces, and pages, and the site entity that wraps in all together. You can develop business solutions to easily share them with consumers. There are two types of business solutions you can choose from: a central or local entry point. These are the main differences between the central and local entry point:

**Key Differences Between the Approaches Supporting Multitenancy in SAP Build Work Zone**


<table>
<tr>
<th valign="top">

Feature

</th>
<th valign="top">

Central Entry Point

</th>
<th valign="top">

Local Entry Point

</th>
</tr>
<tr>
<td valign="top">

Consumer-side SAP Build Work Zone service instance

</td>
<td valign="top">

Required: standard or advanced service plan

</td>
<td valign="top">

Not required

</td>
</tr>
<tr>
<td valign="top">

App router management

</td>
<td valign="top">

Managed app router: you get it out of the box

</td>
<td valign="top">

Standalone app router: extensible

</td>
</tr>
<tr>
<td valign="top">

Site administration

</td>
<td valign="top">

Administered by the consumer: full SAP Build Work Zone service instance in the consumer subaccount

</td>
<td valign="top">

Provider-managed: not administered by the consumer

</td>
</tr>
<tr>
<td valign="top">

Layout customization

</td>
<td valign="top">

Customizable by the consumers: the administrator defines the spaces/pages with federated business application

</td>
<td valign="top">

Layout is fixed by the provider, groups are not supported

</td>
</tr>
</table>

You can find a detailed comparison between central and local entry point at [Creating Business Solutions](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/creating-business-solutions).

To try out the multitenant functionality on the Incident Management sample application, see [Develop a Multitenant CAP Application Following the SAP BTP Developer's Guide](https://discovery-center.cloud.sap/protected/index.html#/missiondetail/4502/4789/).



This image is interactive. Click the highlighted areas so you open the respective tutorial or mission.

![A flowchart that visually outlines the process for developing a
							multitenant CAP application. The steps start from initial development
							and enabling multitenancy, through deployment on either SAP BTP, Cloud
							Foundry or SAP BTP, Kyma runtimes using central or local entry point, to
							subscribing to the application. A legend distinguishes between missions,
							GitHub repositories, and tutorials based on box color.](images/Mission_Develop_a_Multitenant_CAP_Application_1f4feba.png)


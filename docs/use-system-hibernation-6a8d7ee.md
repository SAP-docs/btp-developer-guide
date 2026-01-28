<!-- loio6a8d7ee4ed184dc0bbd15014278bd355 -->

# Use System Hibernation

System hibernation in SAP BTP ABAP environment allows you to temporarily stop and restart a system without deleting the corresponding SAP HANA Cloud instance. This helps reduce costs for systems that are not in use, such as development, test, or analysis systems.

The key points are:

-   Cost reduction:

    -   Stopped systems do not consume ABAP Compute Units \(ACUs\) and only minimal HANA Compute Units \(HCUs\) for storage.

    -   For consumption-based contracts, total costs can drop to less than 5%.


-   Availability: SAP operations automatically start stopped systems for lifecycle management events like upgrades or hotfix imports.

-   Access: Accessing a stopped system via SAP Fiori Launchpad will not start it automatically; the system must be restarted through the Landscape Portal – Manage System Hibernation application.

-   Scheduling: You can manually stop/start or schedule system hibernation using the app. Free tier systems are stopped automatically each night, and scheduled start/stop is not supported.


System hibernation is a simple and effective way to save costs while keeping your SAP BTP ABAP environment up to date and ready for productive use.

See:

-   [Blog Post: SAP BTP ABAP Environment – Manage System Hibernation](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-btp-abap-environment-manage-system-hibernation/ba-p/13566169) 
-   [Blog Post: Optimize Your SAP BTP ABAP Environment Budget: A Detailed Cost Analysis for Customers](https://community.sap.com/t5/technology-blog-posts-by-sap/optimize-your-sap-btp-abap-environment-budget-a-detailed-cost-analysis-for/ba-p/13574333)


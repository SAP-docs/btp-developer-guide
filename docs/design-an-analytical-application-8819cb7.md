<!-- loio8819cb79b82c4489a422a4dff6b6fa56 -->

# Design an Analytical Application

Analytical Applications implement use cases where multi-dimensional data models are queried to analyze business data and derive business KPIs. The main focus is on creating data models to analyze business data in embedded or cross-system setups and to visualize the data in dashboards or as part of apps.

The following graphic gives you an overview of the main parts of the analytical architecture:

![](images/Design_an_Analytical_Application_80e21cc.png)

Analytical data models are CDS-based. The analytical provider consists of a reusable star or snowflake schema \(based on cubes, dimensions, and hierarchies\) and scenario-specific analytical projections \(analytical queries\).

ABAP Cloud enables you to develop Information Access \(InA\)-based services for multidimensional user apps. The InA services are either consumed in SAP Fiori UIs or by SAP Analytics Cloud.


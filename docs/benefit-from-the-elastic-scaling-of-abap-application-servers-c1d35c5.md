<!-- loioc1d35c53d5944b3b8d72d1ff6c69a21b -->

# Benefit from the Elastic Scaling of ABAP Application Servers

SAP BTP ABAP environment allows dynamic adaptation of ABAP application server capacity to changing workloads. This is achieved by elastic scaling, which automatically adjusts the number of application servers based on system load.

The key points are:

-   Manual scaling: ABAP Compute Units \(ACUs\) and HANA Compute Units \(HCUs\) can be increased or decreased manually via the SAP BTP Cockpit. ABAP Compute Units scale quickly with minimal downtime, while HCU adjustments are near-zero-downtime but may take longer depending on database size.

-   Elastic scaling: When enabled \(parameter elastic = true\), the system automatically scales between 1 ACU \(minimum\) and the configured maximum ABAP Compute Units. Scaling is done by adding or removing application servers in increments of 0.5 ABAP Compute Units. Vertical scaling of a single server beyond 0.5 ABAP Compute Unit is not supported.

-   Load metrics: Scaling decisions are based on CPU and memory utilization, as well as ABAP-specific metrics like the number of active work processes.

-   Cost efficiency: Elastic scaling optimizes resource consumption, reducing costs for periods of low usage while still handling peaks.


See:

-   [Updating an ABAP System](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/updating-abap-system)
-   [Blog Post: SAP BTP ABAP Environment – Elastic Scaling of Application Servers](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-btp-abap-environment-elastic-scaling-of-application-servers/ba-p/13614903)


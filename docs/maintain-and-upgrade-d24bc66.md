<!-- loiod24bc66275df41af92c68155e0fb4a84 -->

# Maintain and Upgrade

SAP BTP ABAP environment provides an always up-to-date cloud system. Planned maintenance windows and major upgrades are announced in advance, and contractual Service Level Agreements \(SLAs\) ensure minimal disruption.



<a name="loiod24bc66275df41af92c68155e0fb4a84__section_n5h_1z4_1hc"/>

## Downtime-Optimized Upgrades and Hotfix Collection Imports

The new downtime-optimized upgrade process splits the upgrade in three phases:

-   Preparation: The new release is installed in a shadow layer while the system remains available. Certain lifecycle operations, such as transport imports or tenant lifecycle events, may be temporarily blocked.

-   Takeover: The system switches to the new release, inducing a short downtime \(typically 10–40 minutes for upgrades; about 1 minute for hotfix collection imports\). Running ABAP applications are temporarily shut down.

-   Postprocessing: Finalization and cleanup occur in the background while the system is fully available. Restrictions on transports and lifecycle operations are lifted.


See:

-   [Blog Post: SAP BTP ABAP Environment – Pre-Upgrade Option](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-btp-abap-environment-pre-upgrade-option-for-release-2511/ba-p/14219621)
-   [Blog Post: SAP BTP ABAP Environment – Maintenance Windows and Major Upgrade Windows](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-btp-abap-environment-maintenance-windows-and-major-upgrade-windows-in/ba-p/13920833)



<a name="loiod24bc66275df41af92c68155e0fb4a84__section_wb2_2xp_1hc"/>

## Pre-Upgrade Option

To ensure smooth adoption of new releases, customers and partners can nominate non-development systems for a pre-upgrade prior to the standard upgrade. This allows early regression testing of custom-built applications on the new release. Take into account the following key points:

-   Only non-development systems are recommended for pre-upgrade.

-   Issues detected during regression tests should be reported promptly using SAP support channels.

-   Pre-upgrades do not provide early access to new features; their purpose is to validate existing custom applications.

-   The pre-upgrade system receives hotfix collection imports in phases, mirroring the standard upgrade.


Nomination and management of pre-upgrade systems are done via the Landscape Portal, eliminating the need for manual requests. Exceptional processes exist for handling unresolved critical issues, ensuring minimal impact on productive environments.

We recommend to:

-   Perform regression testing on pre-upgraded test systems to detect potential issues before the standard upgrade.

-   Use the downtime-optimized upgrade process for non-development systems to minimize business impact.

-   Monitor upgrade announcements, schedules, and hotfix collection imports to plan testing and validations efficiently.


See [Blog Post: SAP BTP ABAP Environment – Pre-Upgrade Option](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-btp-abap-environment-pre-upgrade-option-for-release-2511/ba-p/14219621).


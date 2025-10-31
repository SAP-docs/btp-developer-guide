<!-- loio551e0d6754db425fa3dbfd20ed229918 -->

# Manage Full Transport and Lifecycle

In SAP BTP ABAP environment, ABAP objects can be transported and versioned using gCTS and abapGit, enabling robust lifecycle management and collaborative development.

gCTS is the evolution of the classical Change and Transport System \(CTS\) and is the recommended approach for transporting objects between ABAP systems within the same global account in SAP BTP. It is fully integrated into the Manage Software Components app in the SAP Fiori launchpad, allowing for controlled transport, versioning, and lifecycle management of software components across development, test, and productive systems.

abapGit is an open-source Git client for ABAP, designed to handle scenarios such as:

-   Migrating on-premise ABAP code to the cloud.

-   Exporting or importing code when a system is decommissioned.

-   Enabling distributed development and testing in isolated development or test systems.

-   Transferring code between cloud systems, for example from a partner account to a customer account.


abapGit is ideal for cases where lightweight or distributed transport is needed, but it is not recommended as a replacement for standard transport workflows between production-aligned systems.

We recommend that you use:

-   gCTS for all transports between development, test, and productive systems within the same global account in SAP BTP.

-   abapGit for migration, backup, or sharing code between independent systems or accounts.

-   Products in the Landscape Portal as the delivery unit for partner or multi-account scenarios.


gCTS and abapGit help maintain code quality, track changes, and enable scalable development and testing practices across ABAP landscapes.

See [Transport Mechanisms](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/transport-mechanisms?q=Transport&version=Cloud).


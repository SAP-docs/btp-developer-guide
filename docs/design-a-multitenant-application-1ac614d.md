<!-- loio1ac614dd9c2a4f05957096e86de4931c -->

# Design a Multitenant Application

You can use the multiclient architecture of the ABAP system for multitenancy enablement and list the design principles to reach multitenancy.

-   Store tenant-related data in client-dependent tables of type A, C, or L.

-   Store system-related data in client-independent tables of type S.

-   Always add the selection of the client to ABAP database procedures \(AMDPs\).


Make sure consumers cannot modify the client parameter or any other part of the AMDP using the application or by tampering requests.

-   Don't generate development objects or other client-independent data system-locally in the provider system.

-   Don't evaluate the actual value of the 3-digit client field \(IF sy-mandt = ‘nnn’. …. ENDIF\).


You have to classify database tables according to their content. There are the following types:

-   Tenant Content \(client-dependent\)

    -   Tenant configuration data – tables with delivery class “C”

    -   Tenant application data – tables with delivery class “A”

    -   Tenant temporary data – tables with delivery class “L”


    Database tables for tenant content must be client-dependent. This means that the first field of the table must be of datatype “CLNT”. We recommend using the inline declaration „abap.clnt“.

    Only the content of client-dependent “C” and “A” tables is considered during tenant copy and tenant move. Content of client-independent tables which are not delivered from the development system and “L” tables are lost during tenant lifecycle processes such as tenant move.

    During tenant delete, the content of all client-dependent tables is removed.

    The delivery class must be “C”, “A”, or “L”.

    The delivery classes “E”, “G” and “W” are not supported in the ABAP environment at all.

-   System Content \(client-independent\): System configuration data – tables with delivery class “S”

    Store data that is defined by the service provider and not specific for any tenant in a client-independent “S” table. Define the content in the respective development system and export it as TABU entries via a development transport request. The content is considered as code and imported like other development artifacts into subsequent systems such as the provider system.

    Access to tables and all further ABAP Cloud Syntax is by default tenant aware.


See [Multitenancy Development Guideline](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/multitenancy-development-guideline).


<!-- loio1edc97f98ee74f23a9d106fd0e8bfa65 -->

# Connecting to Remote Systems in ABAP



<a name="loio1edc97f98ee74f23a9d106fd0e8bfa65__section_bnq_sdf_gdc"/>

## Overview

The connectivity in SAP BTP provides robust features with which you can establish reliable communication channels, ensuring data flows smoothly and securely across different environments. This capability is essential for enterprise applications, typically complex and needing to consume or push data to a variety of sources or destinations, including systems that are directly accessible, hosted in public or private clouds, or located on customer premises. This connectivity empowers businesses to extend, innovate, and optimize their digital landscapes effectively.



### Services and Components

**Cloud Connector**

The Cloud Connector serves as a secure link between cloud applications and on-premise systems, allowing controlled access to them. It functions as a reverse invoke proxy within a secured network, providing fine-grained control over both accessible on-premise resources and cloud applications that use it.

The Cloud Connector serves as a secure link between cloud applications and systems hosted in public or private clouds, allowing controlled access to them. It functions as a reverse invoke proxy within a secured network, providing fine-grained control over both accessible on-premise or private cloud resources and cloud applications using it. As а distributed and integral part of the Connectivity service, it pairs with a region in SAP BTP. The SAP BTP domain model \(subaccounts\) and the optional Cloud Connector Location ID are used to identify a particular Cloud Connector.

**SAP Destination Service**

The Destination service lets you find the technical information that is required to access a remote service or system from your cloud application. Use the Destination service to:

-   Manage routing and authentication details, as well as custom scenario-specific parameters. This information is maintained as a destination.

-   Perform authentication flows based on the configured details, and return the result to the consumer of the service as part of the regular look-up request, that is the **Find a Destination** REST API.

-   Connect to an on-premise or private cloud system. In this case, the Destination service goes in combination with the Connectivity service.

-   Connect to any other remote application, service or system. In this case, the Destination service goes without the Connectivity service.




<a name="loio1edc97f98ee74f23a9d106fd0e8bfa65__section_kj3_tdf_gdc"/>

## Recommendations

-   Use the Destination service to store and manage your connection configuration data \(including credentials, certificates, URL, headers, queries, and so on\) at design time, and automate the access token retrieval process at runtime for your application.

-   Use the Connectivity service, more specifically Cloud Connector and the connectivity proxy, to establish a secure connection between cloud applications and on-premise or private cloud systems.




<a name="loio1edc97f98ee74f23a9d106fd0e8bfa65__section_k3j_tdf_gdc"/>

## Use Cases

The connectivity use cases include but are not limited to:



### On-Premise to Cloud \(Service Channels\)

You can connect to a cloud service from your on-premise or private cloud network using service channels of the Cloud Connector. For example, you can configure an RFC connection from your on-premise or private cloud system to SAP S/4HANA Cloud.

For scenarios that need to connect from on-premise or private cloud systems to the SAP BTP ABAP environment using RFC, you can establish a connection to an ABAP Cloud tenant host.

**Related Information**  


[Consuming the Destination Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/consuming-destination-service)

[Cloud Connector](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/cloud-connector?version=Cloud)

[Connect DB Tools to SAP HANA via Service Channels](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connect-db-tools-to-sap-hana-via-service-channels?version=Cloud)

[Configure a Service Channel for RFC](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/configure-service-channel-for-rfc?version=Cloud)


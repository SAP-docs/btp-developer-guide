<!-- loiod61a5fc6d5f04d8da2a8142f625632ac -->

# Connecting to Remote Systems



<a name="loiod61a5fc6d5f04d8da2a8142f625632ac__section_bnq_sdf_gdc"/>

## Overview

The connectivity in SAP BTP provides robust features with which you can establish reliable communication channels, ensuring data flows smoothly and securely across different environments. This capability is essential for enterprise applications, typically complex and needing to consume or push data to a variety of sources or destinations, including systems that are directly accessible, hosted in public or private clouds, or located on customer premises. This connectivity empowers businesses to extend, innovate, and optimize their digital landscapes effectively.

For Kubernetes setups, the SAP BTP transparent proxy serves as the entry point to leverage central and secure connection configuration management \(SAP Destination service\) along with hybrid technical connectivity \(SAP Connectivity service\). It provides a unified and seamless connection experience to target systems.



### Services and Components

**SAP Connectivity Service**

The Connectivity service offers a set of services and software components which enable:

-   Cloud applications to make secure connections to systems hosted on premise or in the private cloud.

-   The establishment of secure communication channels from the customer's on-premise or private cloud network to cloud applications, keeping full control and auditability of the resources are exposed to the cloud.


The secure exposure of the private systems is ensured by the Cloud Connector. This way, no network ports need to be exposed on the on-premise or private cloud side. On the side of the cloud applications, the secure interconnectivity is ensured by the connectivity proxy, offered as Software-as-a-Service or Software-as-a-Product, depending on the application hosting environment.

Various communication protocols towards the target system are supported.

**Cloud Connector**

The Cloud Connector serves as a secure link between cloud applications and on-premise systems, allowing controlled access to them. It functions as a reverse invoke proxy within a secured network, providing fine-grained control over both accessible on-premise resources and cloud applications that use it.

The Cloud Connector serves as a secure link between cloud applications and systems hosted in public or private clouds, allowing controlled access to them. It functions as a reverse invoke proxy within a secured network, providing fine-grained control over both accessible on-premise or private cloud resources and cloud applications using it. As а distributed and integral part of the Connectivity service, it pairs with a region in SAP BTP. The SAP BTP domain model \(subaccounts\) and the optional Cloud Connector Location ID are used to identify a particular Cloud Connector.

**Connectivity Proxy**

The connectivity proxy serves as a cloud counterpart to which a Cloud Connector technically establishes a secure link. The connectivity proxy is designed to support various runtimes, ensuring secure connectivity.

-   In SAP BTP, Cloud Foundry runtime, the connectivity proxy is offered as a central and shared feature as part of the [Connectivity service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connectivity?version=Cloud).

-   In the [SAP BTP, Kyma runtime](https://help.sap.com/docs/btp/sap-business-technology-platform/kyma-environment?version=Cloud), it's offered as a naively-integrated [Kyma Module](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connectivity-proxy-in-kyma-environment), simplifying the deployment and configuration.

-   In native Kubernetes environments, the connectivity proxy is offered as a Kubernetes component. The connectivity proxy, as а distributed and integral part of Connectivity service, must be paired with a subaccount in SAP BTP to grant access to the Cloud Connectors paired with that subaccount. See [Connectivity Proxy for Kubernetes](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connectivity-proxy-for-kubernetes?version=Cloud).

-   In [SAP BTP, ABAP environment](https://help.sap.com/docs/btp/sap-business-technology-platform/abap-environment?version=Cloud), as well as SAP S/4HANA Cloud and SAP Integrated Business Planning systems, it's offered as a local integrated service within the respective product.


**SAP Destination Service**

The Destination service lets you find the technical information that is required to access a remote service or system from your cloud application. Use the Destination service to:

-   Manage routing and authentication details, as well as custom scenario-specific parameters. This information is maintained as a destination.

-   Perform authentication flows based on the configured details, and return the result to the consumer of the service as part of the regular look-up request, that is the **Find a Destination** REST API.

-   Connect to an on-premise or private cloud system. In this case, the Destination service goes in combination with the Connectivity service.

-   Connect to any other remote application, service or system. In this case, the Destination service goes without the Connectivity service.


**SAP BTP Transparent Proxy**

The [transparent proxy](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/transparent-proxy-for-kubernetes?version=Cloud) streamlines how your Kubernetes workloads connect to remote systems using destinations in SAP BTP. It simplifies the authentication process, while ensuring effective user propagation and seamless integration with the connectivity proxy.

By leveraging Kubernetes services, the transparent proxy exposes target systems directly on the local network, allowing easy, secure, and unified access to solutions, applications, or systems that are remotely accessible via the Internet, as well as to private systems that are securely exposed using the Cloud Connector, with access provided through the connectivity proxy.

In the [SAP BTP, Kyma runtime](https://help.sap.com/docs/btp/sap-business-technology-platform/kyma-environment?version=Cloud), the transparent proxy is available as a natively integrated [Kyma Module](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/transparent-proxy-in-kyma-environment?version=Cloud).



<a name="loiod61a5fc6d5f04d8da2a8142f625632ac__section_kj3_tdf_gdc"/>

## Recommendations

-   Use the transparent proxy to simplify and streamline your Kubernetes workloads' connectivity with remote systems using destinations in SAP BTP. It enhances developer experience by simplifying authentication and automating destination retrieval, while ensuring seamless, secure integration with the connectivity proxy.

-   Use the Destination service to store and manage your connection configuration data \(including credentials, certificates, URL, headers, queries, and so on\) at design time, and automate the access token retrieval process at runtime for your application.

-   Use the Connectivity service, more specifically Cloud Connector and the connectivity proxy, to establish a secure connection between cloud applications and on-premise or private cloud systems.




<a name="loiod61a5fc6d5f04d8da2a8142f625632ac__section_k3j_tdf_gdc"/>

## Use Cases

The connectivity use cases include but are not limited to:



### Cloud to Cloud

**Connecting Kubernetes Applications to Cloud Systems**

You can connect to a cloud service or system from your Kubernetes environment. For example:

-   Developing an application that requires consumption of an SAP HANA database.

-   Adding new functionality that requires the consumption of an SAP BTP service.

-   Creating new user interfaces that require consumption of an ODаtа service.

-   Adding new functionality that requires integration with third-party APIs.

-   An application requires data exchange or service consumption via a RESTful API.




### Cloud to On- Premise or Private Cloud

**Connecting Cloud Foundry, Kyma, or Kubernetes Applications to On-Premise or Private Cloud Systems**

You can connect to an on-premise or private cloud system from your SAP BTP, Cloud Foundry runtime, SAP BTP, Kyma runtime, or any other Kubernetes environment. For example:

-   Creating new user interfaces that require consumption of an ODаtа service.

-   Developing an application that requires data exchange or service consumption via a RESTful API.

-   Extending an application that requires consumption of APIs in an ABAP system via RFC.

-   Developing an application that requires interaction with a mail server for e-mail operations.

-   Developing an application that requires interaction with a relational or non-relational database \(for example, SAP HANA, MySQL, PostgreSQL, MongoDB\).

-   Implementing a new functionality in an application that requires user authentication and directory services integration using an [LDAP server](https://help.sap.com/docs/SAP_ASE/aa939a27edb34f019f71cc47b9c0fd9a/a743ad4cbc2b1014b114dd2c557f4065.html).

-   Developing an application that needs to transfer files to and from an FTP server.

-   Enabling single sign-on \(SSO\) by forwarding the identity of cloud users to a remote system or service \(user propagation\).




### On-Premise to Cloud \(Service Channels\)

You can connect to a cloud service from your on-premise or private cloud network using service channels of the Cloud Connector. For example:

-   Configure an RFC connection from your on-premise or private cloud system to SAP S/4HANA Cloud.

    For scenarios that need to connect from on-premise or private cloud systems to the SAP BTP, ABAP environment using RFC, you can establish a connection to an ABAP Cloud tenant host.

-   Configure a connection to a service in a Kubernetes cluster.

    Create a service channel to establish a connection to a service in a Kubernetes cluster that is not directly exposed to external access.


**Related Information**  


[Consuming the Connectivity Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/consuming-connectivity-service)

[Consuming the Destination Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/consuming-destination-service)

[Transparent Proxy for Kubernetes](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/transparent-proxy-for-kubernetes?version=Cloud)

[Connectivity Proxy for Kubernetes](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connectivity-proxy-for-kubernetes?version=Cloud)

[Cloud Connector](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/cloud-connector?version=Cloud)

[Using the Transparent Proxy](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/using-transparent-proxy?version=Cloud)

[Connect DB Tools to SAP HANA via Service Channels](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connect-db-tools-to-sap-hana-via-service-channels?version=Cloud)

[Configure a Service Channel for RFC](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/configure-service-channel-for-rfc?version=Cloud)

[Configure a Service Channel for a Kubernetes Cluster](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/configure-service-channel-for-kubernetes-cluster?version=Cloud)


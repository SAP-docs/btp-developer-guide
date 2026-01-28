<!-- loiofcb51b54380943fda8c54c64aa7bf4aa -->

# Run and Scale

There are two things you have to take into account to ensure your application is working properly, and bringing value:

-   Get constant feedback from your users and optimize the application based on this feedback.

-   Monitor and operate the application using the services and capabilities SAP BTP offers.

    See [Establish End-to-End Observability](establish-end-to-end-observability-34065a4.md).




<a name="loiofcb51b54380943fda8c54c64aa7bf4aa__section_dns_5hd_dgc"/>

## **Security Considerations in the Run and Scale Phase**

In the run and scale phase, you operate, monitor, and scale your application to ensure high availability, performance, and adaptability to growing user demands. Integrating security at this stage is essential to protect against evolving threats, maintain regulatory compliance, and support secure, scalable operations.

This phase ensures your application remains responsive and resilient as usage increases. For example, a retail company operating an e-commerce platform must defend against runtime threats such as unauthorized access or suspicious activity, while also ensuring secure auto-scaling during peak shopping periods.

By leveraging built-in security features of the SAP Cloud Application Programming Model \(CAP\) and ABAP Cloud, you can significantly strengthen your application defenses. Key practices include:

-   **Continuous threat monitoring** using SAP BTP observability tools to detect and respond to anomalies in real time.
-   Applicable for CAP: **Secure auto-scaling** with CAP mechanisms that dynamically manage resources while preserving tenant isolation and enforcing security policies.

Implementing these practices helps you mitigate operational risks, comply with standards like GDPR and PCI DSS, and deliver a secure, reliable user experience at scale.

The following table summarizes the security guidelines you need to be familiar with:

**Secure Operations at Scale**


<table>
<tr>
<th valign="top">

Security Guideline

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

Implement Continuous Threat Monitoring

</td>
<td valign="top">

Set up monitoring tools to detect and respond to runtime threats, such as unauthorized access or anomalies. See:

-   [Discovering Observability and Monitoring in SAP BTP, Cloud Foundry](https://learning.sap.com/learning-journeys/developing-applications-on-sap-btp-cloud-foundry-runtime/discovering-observability-and-monitoring-in-sap-btp-cloud-foundry-runtime)
-   [SAP Discovery Center Mission - Implement Observability in a Full-Stack CAP Application Following SAP BTP Developer’s Guide](https://discovery-center.cloud.sap/missiondetail/4432/4718/?tab=projectboard)



</td>
</tr>
<tr>
<td valign="top">

Manage Security Patches and Updates

</td>
<td valign="top">

Regularly apply security patches to client applications and dependencies that integrate with SAP BTP to address vulnerabilities.

</td>
</tr>
<tr>
<td valign="top">

Secure Auto-Scaling Mechanisms

</td>
<td valign="top">

The CAP ensures secure multitenancy and supports secure auto-scaling mechanisms for multitenant SaaS applications by providing robust tenant isolation and resource management out of the box. See:

-   [Secure Multitenancy | capire](https://cap.cloud.sap/docs/guides/security/aspects#secure-multitenancy)
-   [What Is Application Autoscaler? | SAP Help Portal](https://help.sap.com/docs/application-autoscaler/application-autoscaler/what-is-application-autoscaler)



</td>
</tr>
<tr>
<td valign="top">

Conduct Periodic Security Audits

</td>
<td valign="top">

Perform audits to verify compliance and identify gaps in security configurations or policies.

</td>
</tr>
<tr>
<td valign="top">

Protect User-Generated Data Securely

</td>
<td valign="top">

Securely collect and store all forms of user-generated data—whether it originates from surveys, in-app feedback forms, comments, uploads, or integrated systems like ticketing and support platforms, to protect sensitive information and ensure consistent compliance with privacy laws across all data collection points.

</td>
</tr>
</table>

Through adopting these guidelines, you significantly strengthen the security, compliance, and resilience of your SAP BTP application as it operates and scales in production. For more resources, see [SAP BTP Security Recommendations | SAP Help Portal](https://help.sap.com/docs/btp/sap-btp-security-recommendations-c8a9bb59fe624f0981efa0eff2497d7d/sap-btp-security-recommendations).


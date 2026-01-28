<!-- loioa73f6fff77634faab60241c7ea719f90 -->

# Security Considerations for Applications

When building applications, use the security features of SAP BTP, such as protection from web attacks. We recommend that your developers configure and deploy application-based security artifacts containing authorizations, and administrators assign these authorizations using the cockpit. SAP BTP offers platform roles that help you ensure a segregation of duties, such as between app development and administration.

It's likely that data protection and privacy influence your architecture and the functions of your application. Consider any implications as early as possible in your development process. Security monitoring is done with audit logging. SAP BTP writes logs for security-relevant events and the written log files are digitally signed to ensure their integrity.

See the following for more information about security best practices:

-   [CAP Security Guide](https://cap.cloud.sap/docs/guides/security/)

-   [Giving Access Rights to Platform Users](https://help.sap.com/viewer/df50977d8bfa4c9a8a063ddb37113c43/Cloud/en-US/a03d08e4038b46d480c410395593bbd2.html "If you've set up a staged development environment using different subaccounts or spaces, such as for development, testing, and production, grant the Cloud Development Team access to development subaccounts and environments. Only grant the Platform Engineering Team or Center of Expertise (CoE) access to the testing and production subaccounts or environments.") :arrow_upper_right:

-   [SAP BTP Security Recommendations](https://help.sap.com/docs/btp/sap-btp-security-recommendations-c8a9bb59fe624f0981efa0eff2497d7d/sap-btp-security-recommendations?version=Cloud)


You implement, deploy, and validate your application to ensure it meets both functional and performance requirements. Prioritizing secure deployment and configuration at this stage helps you launch your application with strong protections in place—minimizing vulnerabilities and aligning with enterprise-grade security standards.

Delivering your application marks the transition from development to production, where your application becomes accessible to users. This is a critical point for enforcing security controls. For example, a retail company deploying an e-commerce application must ensure secure payment processing and defend against runtime threats such as:

-   SQL injection
-   Cross-site scripting \(XSS\)
-   Cross-Site Request Forgery \(CSRF\)

By applying secure deployment practices—such as hardening configurations, validating inputs, and enabling runtime protection—you reduce the risk of exploitation and ensure compliance with data protection regulations like the GDPR.

By implementing built-in security features offered by the SAP Cloud Application Programming Model \(CAP\), you can significantly enhance your application defense. This includes leveraging:

-   Parameterized queries \(for example, cds.select, .where\) to prevent SQL injection.
-   CDS constraints \(for exampe, @assert.format\) for robust input validation.
-   CSRF protection for UI applications, such as checkout forms.

Furthermore, CAP’s built-in authentication and authorization mechanisms protect user access. Together, these practices help reduce vulnerabilities, support GDPR compliance, and keep user trust.

The following table summarizes the security guidelines you need to be familiar with:

**Delivering Secure Applications Deployed to SAP BTP**


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

Secure Environment Configuration

</td>
<td valign="top">

Configure the SAP BTP runtimes \(for example, SAP BTP, Cloud Foundry runtime, SAP BTP, Kyma runtime with secure settings, such as restricted network access. See:

-   [SAP BTP Cloud Foundry Runtime](https://help.sap.com/docs/cf-runtime/cloud-foundry-runtime/security?version=Cloud)
-   [Secure Development in the Kyma Environment | SAP Help Portal](https://help.sap.com/docs/btp/sap-business-technology-platform/secure-development-in-kyma-environment?version=Cloud)



</td>
</tr>
<tr>
<td valign="top">

Validate Security During Testing

</td>
<td valign="top">

Conduct security tests \(for example, penetration testing\) during validation to identify and fix vulnerabilities before go-live.

</td>
</tr>
<tr>
<td valign="top">

Implement Secure Deployment Pipelines

</td>
<td valign="top">

Use CI/CD pipelines with security checks \(for example, code scanning, dependency validation\) to ensure safe deployments. See:

-   [Introducing Continuous Integration and Delivery \(CI/CD\)](introducing-continuous-integration-and-delivery-ci-cd-8ee5353.md)
-   [Get Started with an SAP Cloud Application Programming Model Project in SAP Continuous Integration and Delivery | SAP Tutorials](https://developers.sap.com/tutorials/cicd-start-cap.html)



</td>
</tr>
<tr>
<td valign="top">

Secure Application Secrets Management

</td>
<td valign="top">

Use SAP Credential Store to securely manage secrets like API keys or database credentials. See [SAP Credential Store](https://help.sap.com/docs/credential-store/sap-credential-store/sap-credential-store?version=Cloud&locale=en-US).

</td>
</tr>
</table>

Following these guidelines will significantly improve the deployment of your application to SAP BTP and enable rigorous validation processes. This approach is critical for safeguarding against potential threats, mitigating vulnerabilities, and ensuring compliance with rule-based standards. For more practical examples on how to implement security in CAP, see [CAP Security Guide | capire](https://cap.cloud.sap/docs/guides/security/).


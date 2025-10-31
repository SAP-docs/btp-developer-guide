<!-- loio7eae38223238424db496ab7ede47cf67 -->

# Discover

Now that the business opportunity has been identified by the explore phase, you can start to discover the concrete needs of your users as well as getting an understanding of the available technology for your landscape.



<a name="loio7eae38223238424db496ab7ede47cf67__section_scz_r55_xcc"/>

## Identifying Required Use Cases

Once you have an understanding of the business opportunity you want to address, you next will need to understand in detail what your end user’s tasks and challenges are. You need a holistic view of the business roles of your application’s users, their jobs to be done, the information they need to get them done, along with their needs and wishes.

To get the relevant insights, you will need to visit your customers onsite or remotely, speak to everyone involved, and if onsite, observe users doing their daily work. You should gain a clear understanding of all the business roles involved, their typical tasks and pain points, and the sequence of activities.

The goal of the discover phase is to gain a thorough understanding of the user’s needs, independent of any existing application or technology. In other words, which information do they need? When do they need it? What business outcomes do they need to achieve?

By the end of the discover phase, you should know what needs to be achieved – without knowing how you want to achieve it, that is addressed in the design phase.

For more information about user research during the Discover phase, have a look at the [User Research Resources](https://experience.sap.com/fiori-design-web/user-research-resources/). The methods outlined there contain the most commonly practiced user research methods at SAP.



<a name="loio7eae38223238424db496ab7ede47cf67__section_dkc_mkc_dgc"/>

## **Security Considerations in the Discover Phase**

Addressing security during the discover phase—when you're gathering detailed requirements and exploring technical options—ensures that protection is a core part of your application's foundation. This phase is about understanding user needs, assessing feasibility, and building early prototypes, making it the ideal time to identify potential risks and plan for secure implementation.

At this stage, you define your application's features and technical requirements. For example, a retail company planning an e-commerce application must ensure secure payment APIs are in place to protect transaction data—an early decision that directly impacts the system's architecture. By evaluating third-party components, identifying data flows, and conducting early security testing on prototypes, you can uncover vulnerabilities before development begins. This proactive approach saves time, reduces cost, and supports compliance with regulations like the GDPR.

The following table summarizes the security guidelines you need to be familiar with:

**Security in the Discover Phase: From Requirements to Risk Reduction**


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

Map Data Flows for Security

</td>
<td valign="top">

Identify and document how sensitive data moves through the system, including user inputs, API calls, and database interactions, to identify potential security risks. You can use [OWASP Threat Dragon](https://owasp.org/www-project-threat-dragon/) to create data flow diagrams for this purpose.

</td>
</tr>
<tr>
<td valign="top">

Establish Secure Architecture Principles

</td>
<td valign="top">

Define architectural guidelines to help ensure that the system is built with security in mind, such as microservice isolation, the principle of least privilege, and multi-layered security approach \(defense-in-depth\).

</td>
</tr>
<tr>
<td valign="top">

Validate Third-Party Service Security

</td>
<td valign="top">

Review the security certifications and practices of third-party services \(for example, APIs, libraries\) you integrate, and align with SAP BTP Security recommendations.

</td>
</tr>
<tr>
<td valign="top">

Incorporate Security in Prototypes

</td>
<td valign="top">

Include basic security features, like input sanitization or mock authentication, in your prototypes to test their effectiveness early.

</td>
</tr>
<tr>
<td valign="top">

Plan for Data Security During User Research

</td>
<td valign="top">

Protect user data collected during research \(for example, interviews, observations\) by anonymizing inputs and securing storage.

</td>
</tr>
<tr>
<td valign="top">

Understand Boundary Conditions

</td>
<td valign="top">

Understand boundary conditions for the new application, like integration into the existing system landscape \(regarding IAM, Audit log\).

</td>
</tr>
</table>

By implementing these guidelines in the discover phase, you improve the security of your application, laying the groundwork for a resilient and compliant application. See [Setting Up Your Security and Compliance Model](https://help.sap.com/docs/btp/btp-admin-guide/setting-up-your-security-and-compliance-model).


<!-- loioa73f6fff77634faab60241c7ea719f90 -->

# Security Considerations for Applications

When building applications, use the security features of SAP BTP, such as protection from web attacks. We recommend that your developers configure and deploy application-based security artifacts containing authorizations, and administrators assign these authorizations using the cockpit. SAP BTP offers platform roles that help you ensure a segregation of duties, such as between app development and administration.

It's likely that data protection and privacy influence your architecture and the functions of your application. Consider any implications as early as possible in your development process. Security monitoring is done with audit logging. SAP BTP writes logs for security-relevant events and the written log files are digitally signed to ensure their integrity.

See the following for more information about security best practices:

-   [CAP Security Guide](https://cap.cloud.sap/docs/guides/security/)

-   [Giving Access Rights to Platform Users](https://help.sap.com/viewer/df50977d8bfa4c9a8a063ddb37113c43/Validation/en-US/a03d08e4038b46d480c410395593bbd2.html "If you've set up a staged development environment using different subaccounts or spaces, such as for development, testing, and production, grant the Cloud Development Team access to development subaccounts and environments. Only grant the Platform Engineering Team or Center of Expertise (CoE) access to the testing and production subaccounts or environments.") :arrow_upper_right:

-   [SAP BTP Security Recommendations](https://help.sap.com/docs/btp/sap-btp-security-recommendations-c8a9bb59fe624f0981efa0eff2497d7d/sap-btp-security-recommendations?version=Cloud)



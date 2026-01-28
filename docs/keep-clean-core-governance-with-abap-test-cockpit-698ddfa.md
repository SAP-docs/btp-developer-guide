<!-- loio698ddfa7ddda491894427e289a9896ca -->

# Keep Clean Core Governance with ABAP Test Cockpit

Maintaining a clean core in your ABAP custom code is essential for long-term maintainability and upgrade stability. In SAP BTP ABAP environment, you can use the ABAP Test Cockpit \(ATC\) to govern your side-by-side developments and gradually transform your code to a clean core.

With clean core you can:

-   Build upgrade-safe ABAP extensions
-   Reduce technical debt when integrating classic ABAP code
-   Ensure consistent governance across development branches
-   Gain insights into API usage and custom enhancements

The ABAP Test Cockpit \(ATC\) is set on SAP BTP and provides a central, cloud-based solution to analyze, monitor, and govern ABAP development:

-   Central ABAP Test Cockpit \(ATC\) check system

    -   Create a central ABAP Test Cockpit \(ATC\) system in your SAP BTP ABAP environment.

    -   Connect it to all development systems \(DEV, QAS\) for consistent governance.


-   Blocking Mode

    -   Configure ABAP Test Cockpit \(ATC\) blocking mode in DEV systems to enforce compliance for Priority 1 and 2 findings.

    -   Ensure that critical issues are resolved before transports reach higher environments.



To support clean core governance in SAP BTP ABAP environment, we recommend including the following checks in your ABAP Test Cockpit \(ATC\) check variant:

-   Allowed SAP enhancement technologies – ensures only approved enhancement approaches are used.

-   Usage of APIs – governs usage of SAP classic APIs and prevents use of unauthorized internal objects.

-   Critical statements – checks critical ABAP statements that may impact stability or upgrade safety.

-   Code Vulnerability Analyzer \(CVA\) – optional security checks \(requires Code Vulnerability Analyzer \(CVA\) license\).


> ### Note:  
> The default ABAP Test Cockpit \(ATC\) variant ABAP\_CLOUD\_DEVELOPMENT\_DEFAULT can be copied and extended with the clean core checks.

To analyze custom code in SAP BTP ABAP environment, you have to:

-   Use the Analyze Custom Code App in SAP BTP ABAP environment

-   Apply your clean core ABAP Test Cockpit \(ATC\) variant to identify non-compliant objects

-   Filter findings by object type, application component, or severity to prioritize remediation

-   Transform the classic ABAP to clean core standards step by step


To do that, we recommend following these steps:

1.  Set up a central ABAP Test Cockpit \(ATC\) system in SAP BTP ABAP environment.
2.  Create a clean core ABAP Test Cockpit \(ATC\) variant with the recommended checks
3.  Analyze existing custom code using Analyze Custom Code App
4.  Apply exemptions or baselines for legacy code
5.  Enforce clean core practices for all new side-by-side developments

See [Blog Post: ABAP Test Cockpit \(ATC\) Recommendations for Governance of Clean Core ABAP Development](https://community.sap.com/t5/technology-blog-posts-by-sap/abap-test-cockpit-atc-recommendations-for-governance-of-clean-core-abap/ba-p/14186130).


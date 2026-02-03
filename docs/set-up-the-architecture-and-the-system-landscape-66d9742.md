<!-- loio66d97421868d405e935b3dc30dcd478d -->

# Set Up the Architecture and the System Landscape



<a name="loio66d97421868d405e935b3dc30dcd478d__section_dnh_z4h_zgc"/>

## Recommended System Landscapes

When setting up the SAP BTP ABAP environment, it’s best to begin with only the systems you currently need — typically the development system \(DEV\).

You don’t have to provision the entire landscape upfront. Additional systems like test \(QAS\) or production \(PRD\) can be added later as your development and release processes evolve.

This incremental setup approach provides better transparency, flexibility, and helps optimize costs.

Two standard landscape options are available:

-   3-system landscape \(DEV, QAS, PRD\): Recommended for most projects, especially when development is occasional or release cycles are less frequent. Enables testing outside the development system and verification of application behavior before go-live.

-   5-system landscape \(DEV, COR, TST, QAS, PRD\): Suitable for larger teams and continuous development scenarios. Enables parallel correction handling and uninterrupted development activities.


Use system hibernation to reduce costs by stopping development \(DEV\), correction \(COR\), and test \(TST\) systems when they are not in active use. See [Use System Hibernation](use-system-hibernation-6a8d7ee.md).

See [Setting Up and Working with Your Landscape](https://help.sap.com/docs/sap-btp-abap-environment/abap-environment/setting-up-and-working-with-your-landscape?version=Cloud).



<a name="loio66d97421868d405e935b3dc30dcd478d__section_avz_3ph_zgc"/>

## Sizing

For productive systems, even a single ABAP Compute Unit \(ACU\) can serve up to 1,000 active business users per day, showing that minimal configurations are already powerful. The recommended minimum starting point is:

-   1 ABAP Compute Unit \(ACU\) – 16 GB

-   2 HANA Compute Units \(HCU\) – 16 GB each


Both ABAP Compute Units and HANA Compute Units can be scaled up or down manually via the SAP BTP cockpit to match changing workload requirements.

With release 2402, SAP BTP ABAP environment introduces automatic runtime scaling, which dynamically adjusts ABAP Compute Units based on actual application server usage.

> ### Note:  
> This feature requires a consumption-based contract.


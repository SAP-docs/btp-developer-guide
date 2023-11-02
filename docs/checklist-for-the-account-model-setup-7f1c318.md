<!-- loio7f1c318292934e088e5cd119271f0b1e -->

# Checklist for the Account Model Setup

Independent of the account model you choose, we recommend going through the following steps and defining guidelines for your development teams.



<a name="loio7f1c318292934e088e5cd119271f0b1e__section_mzm_ctn_fyb"/>

## 1. Fulfill Prerequisites

1.  Before you set up your account model and assign users, read [Onboard to SAP Cloud Identity Services](https://help.sap.com/viewer/df50977d8bfa4c9a8a063ddb37113c43/Cloud/en-US/9c897ee8df014b3b8d7c67bab16f385c.html "When setting up accounts, you need to assign users. While we provide you with your first users to get you started, your organization has identity providers that you want to integrate.") :arrow_upper_right:.

2.  Evaluate your business and technical needs and define an account model that fits the requirements of your company. Ensure that the account model is suitable for all areas in your company.

3.  Define account hierarchy and guidelines and roll them out to a few pilot project managers to get their feedback.




## 2. Define Account Standards and Rules

1.  Ensure each hierarchy \(Global Account, directories, subaccounts, spaces/namespaces/packages\) is owned by a team that takes responsibility; for example:

    -   The global account should be owned by the Platform Engineering Team/Center of Excellence.

    -   Directories and subaccounts can be operated by dedicated account owners, which have been upskilled by the Platform Engineering Team/Center of Excellence.

    -   Spaces/namespaces/packages \(depending on the runtime\) can be owned by the respective development units.


2.  Optionally, create a template for new directories. See [Template for New Directories](checklist-for-the-account-model-setup-7f1c318.md#loio7f1c318292934e088e5cd119271f0b1e__section_template_for_directories) and [Account Model With Directories and Subaccounts](account-model-with-directories-and-subaccounts-b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd).

3.  Define naming conventions, for example:

    -   To ensure that there are no conflicts with special characters, we recommend sticking with lower-case letters and hyphens, and not to use spaces in names.

    -   Give the directory a descriptive name that starts with your company or global account name.

    -   There's a 1:1 relationship between a subaccount and Cloud Foundry org/Kyma cluster, so you should give them identical names.

    -   Because there's no connection between spaces/namespaces in different subaccounts, we recommend giving identical names to the dev, test, and prod versions of projects and spacess/namespaces.


4.  Define labels and values according to the reports you want to create.

5.  Define rules for quota limitations.




<a name="loio7f1c318292934e088e5cd119271f0b1e__section_template_for_directories"/>

## Template for New Directories

We recommend that you create a process for the creation of new directories. You can use the following example template or adapt it to meet your requirements:


<table>
<tr>
<th valign="top" colspan="2">

New Directory

</th>
</tr>
<tr>
<td valign="top">

Name

</td>
<td valign="top">

Refer to your naming guidelines.

</td>
</tr>
<tr>
<td valign="top">

Owners

</td>
<td valign="top">

We recommend appointing at least two owners.

</td>
</tr>
<tr>
<td valign="top">

Description

</td>
<td valign="top">

Describe the developer audience, which LoB or department do they belong to, what types of applications will be developed, which environments should be used, subscriptions that will be used.

</td>
</tr>
<tr>
<td valign="top">

Cost center

</td>
<td valign="top">

Define accounting requirements.

</td>
</tr>
<tr>
<td valign="top">

Enrollment

</td>
<td valign="top">

Describe how projects can enroll in your directory.

</td>
</tr>
</table>

**Related Information**  


[Labels \[Feature Set B\]](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loioe8663c08ead648faa673b0d63c5b478e "Labels are user-defined words or phrases that you can assign to various entities in SAP BTP to categorize them in your global account, to identify them more easily.") :arrow_upper_right:


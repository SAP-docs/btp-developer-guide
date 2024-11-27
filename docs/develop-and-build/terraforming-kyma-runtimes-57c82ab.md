<!-- loio57c82ab6c4e144cdbd0997ea0358c27c -->

# Terraforming Kyma Runtimes

By integrating the Terraform module into CI/CD pipelines, development teams can automate the provisioning of resources needed to create a Kyma cluster, deploy applications, run tests, and tear down the resources when they are no longer required. As there is no need to have resources running continuously, this approach reduces operational costs.

The Terraform module uses the Terraform provider for SAP BTP. Terraform provider for SAP BTP helps you to manage automatically the required SAP BTP resources for creating and using the SAP BTP, Kyma runtime in a continuous integration scenario. For this purpose, we recommend you to use:

-   [Terraform provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest/docs)

-   [The Terraform module for Kyma](https://github.com/kyma-project/terraform-module/)


> ### Caution:  
> It is important to distinguish the Terraform module from the [Kyma modules](https://help.sap.com/docs/btp/sap-business-technology-platform/kyma-modules). The Terraform module is a development tool. The word ["module"](https://developer.hashicorp.com/terraform/language/modules) in this context comes from the Terraform provider for SAP BTP naming convention.



<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_cgq_jlt_xcc"/>

## Prerequisites

-   The continuous integration worker agent must have the Terraform provider for SAP BTP command line interface \(CLI\) installed. See [Install Terraform and the Terraform CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli).

-   The development team must have admin access at the subaccount level or SAP BTP global account level.




<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_hsk_frt_xcc"/>

## Access to SAP BTP in the Continuous Integration Scenario

The Terraform module communicates with SAP BTP using the [Terraform provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest/docs).

There are two use cases that must be taken into account:

-   Suppose the development team has administrative access at the subaccount level only \(but not at the global account\). In that case, the custom Identity Authentication tenant must be trusted on the subaccount level, and the technical user must be given a subaccount admin role in the target subaccount. In such a setup, the module can create SAP BTP resources within the given target subaccount. See an [example](https://github.com/kyma-project/terraform-module/tree/main/examples/kyma-on-btp-reuse-sa) in GitHub.

-   If the development team has administrative access at the global account level, then the custom Identity Authentication tenant could be trusted at the global account level, and the technical user could be given a global account admin role in the target global account. In such a setup, the module can create SAP BTP resources in the new subaccount. The subaccount then belongs to the resources managed by the module. See an [example](https://github.com/kyma-project/terraform-module/tree/main/examples/kyma-on-btp-new-sa) in GitHub.




<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_grc_vyz_3dc"/>

## Procedure

The module requires a set of [input parameters](https://github.com/kyma-project/terraform-module/?tab=readme-ov-file#input-variables-tf-vars) among which a technical user's credentials must be provided. Using a credential management system, such as [HashiCorp Vault](https://developer.hashicorp.com/vault/docs/what-is-vault), is highly recommended.

The result is a set of [outputs](https://github.com/kyma-project/terraform-module/blob/main/README.md#outputs) that provide information such as kubeconfig, subaccount ID, service instance ID, cluster ID, and domain.

1.  To use the Terraform module for Kyma, create a dedicated folder in your project repository \(for example, `tf`\), a main Terraform \(`main.tf`\) file, and a `.tfvars` file. This is the so-called root Terraform module, where the module can be used as a child module.

2.  In the `.tfvars` file, provide the required input parameters, for example:

    ```
    BTP_BOT_USER = "..."
    BTP_BOT_PASSWORD = "..."
    BTP_GLOBAL_ACCOUNT = "..."
    BTP_BACKEND_URL = "https://cpcli.cf.sap.hana.ondemand.com"
    BTP_CUSTOM_IAS_TENANT = "my-tenant"
    BTP_NEW_SUBACCOUNT_NAME = "kyma-runtime-subaccount"
    BTP_NEW_SUBACCOUNT_REGION = "eu21"
    BTP_KYMA_PLAN = "azure"
    BTP_KYMA_REGION = "westeurope"
    ```

    > ### Note:  
    > Check the [.tfvars-template](https://github.com/kyma-project/terraform-module/blob/main/examples/kyma-on-btp-new-sa/.tfvars-template) for reference.

3.  In `main.tf,` add the required providers, such as `SAP/btp`, `massdriver-cloud/jq`, or`hashicorp/http,` and include the Kyma module for Terraform as a child module:

    ```
    terraform {
      required_providers {
        btp = {
          source  = "SAP/btp"
        }
        http = {
          source = "hashicorp/http"
        }
        http-full = {
          source = "salrashid123/http-full"
        } 
      }
    }
    provider "http-full" {}
    provider "http" {}
    provider "btp" {
      globalaccount = var.BTP_GLOBAL_ACCOUNT
      cli_server_url = var.BTP_BACKEND_URL
      idp            = var.BTP_CUSTOM_IAS_TENANT
      username = var.BTP_BOT_USER
      password = var.BTP_BOT_PASSWORD
    }
    
    module "kyma" {
      source = "git::https://github.com/kyma-project/terraform-module.git?ref=v0.3.1"
      BTP_KYMA_PLAN = var.BTP_KYMA_PLAN
      BTP_KYMA_REGION = var.BTP_KYMA_REGION
      BTP_NEW_SUBACCOUNT_NAME = var.BTP_NEW_SUBACCOUNT_NAME
      BTP_NEW_SUBACCOUNT_REGION = var.BTP_NEW_SUBACCOUNT_REGION
    }
    
    //Use the outputs of the Kyma module as you wish.
    //Here it is forwarded as outputs of the root module.
    output "subaccount_id" {
      value = module.kyma.subaccount_id
    }
    
    output "service_instance_id" {
      value = module.kyma.service_instance_id
    }
    
    output "cluster_id" {
      value = module.kyma.cluster_id
    }
    
    output "domain" {
      value = module.kyma.domain
    }
    
    ```

4.  Run Terraform in your root \(`tf`\) module folder:

    ```
    cd tf
    terraform init
    terraform apply -var-file=.tfvars -auto-approve
    ```




<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_v5g_mzz_3dc"/>

## Result

You should see a new `kubeconfig.yaml` file in the root module folder, providing you access to the newly created Kyma runtime.



<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_xfr_nzz_3dc"/>

## Next Steps

-   To read the output value, use the `terraform output` command, for example:

    ```
    terraform output -raw cluster_id
    ```

-   To destroy all resources, call the `destroy` command:

    ```
    terraform destroy -var-file=.tfvars -auto-approve
    ```



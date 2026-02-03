<!-- loio57c82ab6c4e144cdbd0997ea0358c27c -->

# Terraforming Kyma Runtimes

By integrating the Terraform module into CI/CD pipelines, you can automate the provisioning of SAP BTP resources required to create a Kyma cluster and tear them down when no longer required. Such an approach helps you reduce operational costs.

For this purpose, we recommend you to use the [Terraform module for Kyma](https://github.com/kyma-project/terraform-btp-kyma-environment), which helps you to automatically manage the required SAP BTP resources for creating and using the SAP BTP, Kyma runtime in a continuous integration scenario.

-   [Terraform provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest/docs)

-   [The Terraform module for Kyma](https://github.com/kyma-project/terraform-btp-kyma-environment)


> ### Caution:  
> It is important to distinguish the Terraform module from the [Kyma modules](https://help.sap.com/docs/btp/sap-business-technology-platform/kyma-modules). The Terraform module is a development tool. The word ["module"](https://developer.hashicorp.com/terraform/language/modules) in this context comes from the Terraform provider for SAP BTP naming convention.



<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_cgq_jlt_xcc"/>

## Prerequisites

-   The CI/CD pipeline must have access to the Terraform or OpenTofu command line interface \(CLI\). See [Install Terraform and the Terraform CLI](https://help.sap.com/docs/link-disclaimer?site=https%3A%2F%2Fdeveloper.hashicorp.com%2Fterraform%2Ftutorials%2Faws-get-started%2Finstall-cli).

-   The administrative access to SAP BTP global account or subaccount, depending on the scenario.


> ### Note:  
> It is recommended to have a technical user in place for the CI/CD pipeline. It is required that the technical user is recognized as a platform user. It must be invited to a custom SAP Cloud Identity Services tenant that is trusted on the SAP BTP global account level. The technical user must have the appropriate role collection assigned for the module to work. See the following section for more details.



<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_hsk_frt_xcc"/>

## Supported Scenarios

There are two main use cases that are supported by the Terraform module:

-   Deploying Kyma runtime in an existing subaccount. This requires that the technical user executing the Terraform script in the CI/CD pipeline has the *Subaccount Administrator* role collection assigned in the targeted subaccount. The module creates all required resources in the given subaccount. See an [example in GitHub](https://github.com/kyma-project/terraform-btp-kyma-environment/tree/main/examples/kyma-on-btp-reuse-sa).

-   Deploying Kyma runtime into a new subaccount. This requires that the technical user executing the Terraform script in the CI/CD pipeline has the *Global Account Administrator* role collection assigned in the targeted SAP BTP global account. The module creates all required resources, including a new subaccount. See an [example in GitHub](https://github.com/kyma-project/terraform-btp-kyma-environment/tree/main/examples/kyma-on-btp-new-sa).




<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_grc_vyz_3dc"/>

## Procedure

The module requires a set of [input parameters](https://github.com/kyma-project/terraform-btp-kyma-environment?tab=readme-ov-file#inputs), among which a technical user's credentials must be provided. Using a credential management system, such as [HashiCorp Vault](https://developer.hashicorp.com/vault/docs/what-is-vault), is highly recommended.

The module produces a set of [outputs](https://github.com/kyma-project/terraform-btp-kyma-environment/blob/main/README.md#outputs) that provide information about the created Kyma runtime, such as subaccount ID, environment instance ID, and API server URL.

Provided that the *<store\_kubeconfig\_locally\>* and *<store\_cacert\_locally\>* variables are set to \`true\`, the module may also produce the following additional sensitive files, useful for accessing Kyma runtime using kubectl:

-   `kubeconfig.yaml`

-   `CA.crt`


1.  To use the module, create a dedicated folder in your project repository, for example, `tf`, create the `*.tf` files to define main resources, variables, providers, and outputs, following the naming convention for clarity, and `terraform.tfvars` files for passing variables. The structure should look like this:

    ```
    +-- tf
    |   +-- main.tf
    |   +-- terraform.tfvars
    |   +-- provider.tf
    |   +-- variables.tf
    |   +-- outputs.tf
    ```

2.  In `variables.tf`, define the inputs needed for the resources defined in `main.tf` and providers defined in `provider.tf`.

    ```
    ###
    # SAP BTP provider configuration
    ###
    variable "BTP_GLOBAL_ACCOUNT" {
      type        = string
      description = "Subdomain of the SAP BTP global account"
    }
    
    variable "BTP_BOT_USER" {
      type        = string
      description = "Technical username"
    }
    
    variable "BTP_BOT_PASSWORD" {
      type        = string
      description = "Technical user password"
      sensitive   = true
    }
    
    variable "BTP_CUSTOM_IAS_TENANT" {
      type        = string
      description = "Custom IAS tenant"
      default     = "custom-tenant"
    }
    
    variable "BTP_BACKEND_URL" {
      type        = string
      description = "BTP backend URL"
      default     = "https://cli.btp.cloud.sap"
    }
    
    ###
    # Kyma module
    ###
    variable "BTP_NEW_SUBACCOUNT_NAME" {
      type        = string
      description = "Name of the subaccount to be created"
      default     = null
    }
    
    variable "BTP_NEW_SUBACCOUNT_REGION" {
      type        = string
      description = "Subaccount region name"
      default     = null
    }
    
    variable "BTP_KYMA_PLAN" {
      type        = string
      description = "Kyma plan name"
      default     = "azure"
    }
    
    variable "BTP_KYMA_REGION" {
      type        = string
      description = "Kyma region"
      default     = "westeurope"
    }
    
    variable "BTP_KYMA_CUSTOM_ADMINISTRATORS" {
      type    = list(string)
      default = []
    }
    ```

3.  In the `terraform.tfvars` file, provide [values for the variables](https://github.com/kyma-project/terraform-btp-kyma-environment/blob/main/README.md#inputs) that are necessary for the `Kyma` module. For example:

    ```
    BTP_NEW_SUBACCOUNT_NAME        = "my-subaccount"
    BTP_NEW_SUBACCOUNT_REGION      = "..." # for example 'eu20'
    BTP_GLOBAL_ACCOUNT             = "..."
    BTP_BOT_USER                   = "..."
    BTP_BOT_PASSWORD               = "..."
    BTP_BACKEND_URL                = "..." # for example 'https://cli.btp.cloud.sap'
    BTP_CUSTOM_IAS_TENANT          = "..."
    BTP_KYMA_PLAN                  = "..." # for example 'azure'
    BTP_KYMA_REGION                = "westeurope"
    BTP_KYMA_CUSTOM_ADMINISTRATORS = ["..."] # list of emails of users that should be gransted `cluster-admin` role  
    ```

    > ### Note:  
    > Check the [.terraform.tfvars.example](https://github.com/kyma-project/terraform-btp-kyma-environment/blob/main/examples/kyma-on-btp-new-sa/terraform.tfvars.example) for reference.

4.  In `provider.tf`, add providers that are required by the Kyma Terraform module. See [Terraform provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest), and [terracurl](https://registry.terraform.io/providers/devops-rob/terracurl/latest).

    ```
    terraform {
      required_providers {
        btp = {
          source  = "SAP/btp"
          version = "~> 1.18.1"
        }
        terracurl = {
          source  = "devops-rob/terracurl"
          version = "~> 2.1.0"
        }
      }
    }
    
    provider "btp" {
      globalaccount  = var.BTP_GLOBAL_ACCOUNT
      cli_server_url = var.BTP_BACKEND_URL
      idp            = var.BTP_CUSTOM_IAS_TENANT
      username       = var.BTP_BOT_USER
      password       = var.BTP_BOT_PASSWORD
    }
    
    provider "terracurl" {}
    
    ```

5.  In `main.tf`, include the `Kyma` module as a child module.

    ```
    
    module "kyma" {
      source                    = "git::https://github.com/kyma-project/terraform-btp-kyma-environment.git?ref=1.0.0"
      
      BTP_NEW_SUBACCOUNT_NAME        = var.BTP_NEW_SUBACCOUNT_NAME
      BTP_NEW_SUBACCOUNT_REGION      = var.BTP_NEW_SUBACCOUNT_REGION
      BTP_KYMA_PLAN                  = var.BTP_KYMA_PLAN
      BTP_KYMA_REGION                = var.BTP_KYMA_REGION
      BTP_KYMA_CUSTOM_ADMINISTRATORS = var.BTP_KYMA_CUSTOM_ADMINISTRATORS
      store_kubeconfig_locally       = true # enable to produce kubeconfig.yaml file for initial administrative access valid for 2 hrs.
      
      # check inputs section what else can be configured
    }
    
    ```

6.  In `outputs.tf`, define the outputs readable by Terraform CLI.

    ```
    output "subaccount_id" {
      description = "The subaccount ID where the Kyma environment is created."
      value = module.kyma.subaccount_id
    }
    
    output "environment_instance_id" {
      description = "The Kyma environment instance ID."
      value = module.kyma.environment_instance_id
    }
    
    output "apiserver_url" {
      description = "The API server URL of the Kyma cluster."
      value       = module.kyma.apiserver_url
    }
    ```

7.  Run the Terraform CLI in the `tf` folder.

    ```
    cd tf
    terraform init
    terraform plan -out=plan.out
    ```

8.  Validate that the planned changes are correct, and then confirm the `apply` operation.

    ```
    terraform apply plan.out # add -auto-approve in CI/CD
    ```

    This creates a new Kyma runtime in your SAP BTP account.




<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_v5g_mzz_3dc"/>

## Result

As a result of applying the configuration, you have Kyma environment up and running. You can read the environment instance ID, the Kubernetes API server URL, and the subaccount ID of the Kyma cluster from the Terraform outputs, for example:

```
terraform output apiserver_url
terraform output environment_instance_id
terraform output subaccount_id
```

To enable immediate access to the cluster in headless scenarios, the module can be used with the following additional flags:

```
store_cacert_locally           = true
store_kubeconfig_locally       = true
```

With that, the module produces the `kubeconfig.yaml` and `CA.crt` sensitive files. With these files, you can access Kyma runtime using kubectl, so be thoughtful not to publish them in any way.

Additionally, the module comes with a Bash and a PowerShell [scripts](https://github.com/kyma-project/terraform-btp-kyma-environment/tree/main/scripts) that you can use to extract cluster ID and domain values from the Kyma cluster using kubectl. The scripts read the kubeconfig file from the KUBECONFIG environment variable, extract the cluster ID and domain, and write them to local files called `domain.txt` and `cluster_id.txt`.



<a name="loio57c82ab6c4e144cdbd0997ea0358c27c__section_xfr_nzz_3dc"/>

## Next Steps



### Remote State Storage

Terraform maintains a state file that maps your configuration to the actual infrastructure, such as SAP BTP resources. With that, it detects drift and safely computes changes. By default, Terraform writes the state in the local filesystem in the working directory, which may be fine for local executions, but doesn't work for concurrent runs initiated in CI/CD pipelines.

For CI/CD pipelines that create and maintain resources, configure a remote backend to store state centrally, for example: Terraform Cloud, AWS S3, GCS, Azure Blob Storage. See [Backend block configuration overview](https://developer.hashicorp.com/terraform/language/backend) for more information on remote backends for state storage.



### Destroying Resources

To destroy all resources, run the `destroy` command:

```
terraform destroy # -auto-approve when called from CI/CD pipeline
```

> ### Caution:  
> The `destroy` command removes all infrastructure resources mapped in the state files.
> 
> Always ensure you know which configuration you are about to destroy, and avoid `-auto-approve` when executing locally.


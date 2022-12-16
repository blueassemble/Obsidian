Frequently Used Links
[Terraform Registry](https://registry.terraform.io/)
[Docs overview | hashicorp/azurerm | Terraform Registry](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs)
[Documentation | Terraform | HashiCorp Developer](https://developer.hashicorp.com/terraform/docs)


BackLinks
[Terraform Lifecycle](./Terraform%20Lifecycle)


## Overview

Terraform is an open-source infrastructure as code (IAC) tool developed by HashiCorp. It allows you to define, deploy, and manage infrastructure resources, such as cloud resources, networking components, and on-premises resources, using a high-level configuration language called HashiCorp Configuration Language (HCL).

With Terraform, you can write declarative configuration files that describe the desired state of your infrastructure, and Terraform will use these files to create and manage the resources. This helps to automate the process of provisioning, updating, and managing infrastructure, and makes it easier to version control and track changes to your infrastructure over time.

Terraform is designed to be extensible and modular, allowing you to use pre-built "providers" to manage resources from different cloud providers, such as Azure, AWS, and Google Cloud, as well as on-premises resources, such as VMs and networking components.

Terraform also provides features such as resource dependencies, module reuse, and resource provisioning and destruction, which allow you to create complex infrastructure architectures and manage the lifecycle of your resources.

Here's an example of how you might use Terraform to create a virtual machine in Azure:

```
`# Configure the Azure provider 
provider "azure" {
	subscription_id = "abc123"
	client_id       = "abc123"
	client_secret   = "abc123"
	tenant_id       = "abc123" 
}

# Create a resource group 
resource "azure_resource_group" "rg" {
	name     = "my-resource-group"
}
```

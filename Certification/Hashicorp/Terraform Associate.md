
1. You are developing a new Terraform module to demonstrate features of the most popular HashiCorp products. You need to spin up an AWS instance for each tool, so you create the resource block as shown below using the `for_each` meta-argument.

- [ ] aws_instance.bryan-demo[1]
- [-] aws_instance.bryan-demo["vault"] 
- [ ] aws_instance.bryan-demo["2"]
- [ ] aws_instance.bryan-demo.vault


2. Where does Terraform Open Source (OSS) store the _local_ state for workspaces?

- [ ] a file called *terraform.tfstate*
- [ ] a file called *terraform.tfstate.backup*
- [ ] directory called *terraform.workspaces.tfstate*
- [-] directory called *terraform.tfstate.d/<workspace name*

3. What do the declarations, such ad  `name`, `cidr`, and `azs`, in the following Terraform code represent and what purpose do they serve?

```
module "vpc" {
	source = "terraform-aws-modules/vpc/aws"
	version = "2.21.0"

	name = var.vpc_name
	cidr = var.vpc_cidr

	azs = var.vpc_azs
	private_subnets = var.vpc_private_subnets
	public_subnets = var.vpc_public_subnets
	
	enable_nat_gateway = var.vpc_enable_nat_gateway

	tags = var.vpc_tags
}
```

- [ ] the `value` of these variables will be obtained from values created within the child module
- [-] these are where the `variable declarations` are created so Terraform is aware of these variables within the calling module
- [ ] these are the `outputs` that the child module will return
- [ ] these are `variables` that are passed into the child module likely used for resource creation


4. Provider dependencies are created in sevral different ways. Select the valid provider dependencies from the following list: (select three)

- [-] Explicit use of a provider block in configuration, optionally including a version constraint.
- [-] Use of any resource block or data block in the configuration, belonging to a particular provider
- [-] Existence of any resource instance belonging to a particular provider in the current *state*.
- [ ] Existence of any provider plugins found locally in the working directory.
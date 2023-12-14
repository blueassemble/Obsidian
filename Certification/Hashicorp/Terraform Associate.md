
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
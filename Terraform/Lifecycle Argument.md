[Lifecycle Argument Docs](https://developer.hashicorp.com/terraform/language/meta-arguments/lifecycle)

### In this articles
[1. Syntax and Arguments](#syntax-and-arguments)
[2. Custom Condition Checks](#custom-condition-checks)


#### Syntax and Arguments

In Terraform, the "lifecycle" meta-argument is a block of configuration that allows you to specify lifecycle management options for a resource. The lifecycle meta-argument can be used to control the behavior of a resource during different stages of its lifecycle, such as creation, update, and deletion.

Here are some examples of the options that can be specified in the lifecycle meta-argument:

-   `create_before_destroy`: When set to `true`, this option causes Terraform to create a new resource before destroying the old one. This can be useful when you want to update a resource without interrupting its service.
    
-   `prevent_destroy`: When set to `true`, this option prevents a resource from being destroyed. This can be useful when you want to protect important resources from being accidentally deleted.
    
-   `ignore_changes`: This option allows you to specify a list of resource attributes that should be ignored when determining whether to update a resource. This can be useful when you want to update a resource without changing certain attributes.
    
-   `force_new_resource`: When set to `true`, this option forces Terraform to create a new resource even if the existing resource has the same configuration as the new one. This can be useful when you want to ensure that a resource is recreated.
    

The lifecycle meta-argument can be added to any resource block in a Terraform configuration. For example:

```
resource "aws_instance" "example" {
  ami           = "ami-12345"
  instance_type = "t2.micro"

  lifecycle {
    create_before_destroy = true
    prevent_destroy = true
  }
}

```

#### Custom Condition Checks

#### Literal Values Only

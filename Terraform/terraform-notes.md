* Infrastructure as Code (IaaC) with Terraform

Terraform is often referred to as “Infrastructure as Code (IaC)” or more precisely **API as Code**, because it interacts directly with cloud provider APIs to provision and manage infrastructure.

AWS CloudFormation (CFT) and Azure Resource Manager (ARM templates)are also Infrastructure as Code tools, but they are cloud-specific.

**How Terraform Works (Under the Hood)

You write infrastructure definitions in HCL (HashiCorp Configuration Language).Terraform uses provider plugins (AWS, Azure, GCP, etc.) and these providers convert your Terraform code into native API calls for the respective cloud platform. The cloud provider executes those API calls to create resources.

**Problem Statement
In traditional cloud setups, each cloud provider had it's own IaC tool like AWS CFT, ARM & Deployment Manager ( GCP). They have different structure and syntax for each cloud.

-- Need to maintain multiple templates
-- INcrease learning curve and different migration between clouds
-- Vendor lock in

Terraform provides a unified approach:
- Single language (HCL) for all clouds
- Same workflow across environments
- Easy to extend to multi-cloud setups
- Simplifies infrastructure migration
- Reduces vendor lock-in

Terraform <-----> Terraform Provider<------> Target API

** Terraform workflow commands
1) terraform init - This sets up teh environment by downloading provider ( AWS, Azure etc) plugins, modules and initializing the backend ( local or remote) where the state file will be stored. This creates the working directory (.terraform) folder.


2) terraform plan - This is a dry run and shows what changes will be done using the terraform file
3) terraform validate
4) terraform apply - This actually creates the resources

** What is a terraform provider??

A provider is a plugin that enables Terraform to communicate with the platform or cloud service by translating terraform code to API calls.
-- Official Providers ( 30+) - Maintained by HashiCorp
-- Partner providers ( 400+) - Maintained by HashiCorp partner companies
-- Community Providers

A terraform file ends with the extension .tf
The first thing that should be in the tf file is what provider we will be working with.

# tf-remote
TF 101, Remote State Storage

# Purpose
This is not a full blown repo, just following along with : https://learn.hashicorp.com/terraform/getting-started/remote

# Notes 

- In case of local run but remote state saving disable Remote execution in workspace settings, only leave local :
https://app.terraform.io/app/GUSTEST/workspaces/Example-Workspace/settings/general


# Todo


# done
- [x] create token
- [x] test remote state storage

# Logs 

## Init
```
$ terraform init

Initializing the backend...

Successfully configured the backend "remote"! Terraform will automatically
use this backend unless the backend configuration changes.

Initializing provider plugins...
- Checking for available provider plugins...
- Downloading plugin for provider "aws" (hashicorp/aws) 2.31.0...

The following providers do not have any version constraints in configuration,
so the latest version was installed.

To prevent automatic upgrades to new major versions that may contain breaking
changes, it is recommended to add version = "..." constraints to the
corresponding provider blocks in configuration, with the constraint strings
suggested below.

* provider.aws: version = "~> 2.31"

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
```

## Run (apply)
```
An execution plan has been generated and is shown below.
Resource actions are indicated with the following symbols:
  + create

Terraform will perform the following actions:

  # aws_instance.web0 will be created
  ...
aws_instance.web0: Creating...
aws_instance.web0: Still creating... [10s elapsed]
aws_instance.web0: Still creating... [20s elapsed]
aws_instance.web0: Still creating... [30s elapsed]
aws_instance.web0: Creation complete after 32s [id=i-0d2ee89dd01f1a3c0]

Apply complete! Resources: 1 added, 0 changed, 0 destroyed.
Releasing state lock. This may take a few moments...
```

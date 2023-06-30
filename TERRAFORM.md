# Terraform

## Install Terraform

```powershell
choco install terraform
```

## Verify the installation

```powershell
terraform -help
```

## local.tf

```tf
resource "local_file" "foo" {
  content  = "foo!"
  filename = "${path.module}/foo.bar"
}
```

## Commands 

```bash
# initialize terraform
$ terraform init
# review the configuration
$ terraform plan
# apply the configuration
$ terraform apply
# remove the configuration
$ terraform destory
```

## Other commands

```bash
# validate the syntax
terraform validate
# pretty format
terraform fmt
# show all the meta information
terraform show
# show providers
terraform providers
# show in graph(you need to install graphviz)
terraform graph
terraform graph | dot -Tsvg > sample.svg
```


## terraform state command

```bash
# TO view a list Of resources and their current state, use the following command:
terraform state list
# TO get detailed information about a specific resource
terraform state Show <resource_name>
# TO import-resources
terraform import <resource—type>.<resource_name> <resource_id>
# TO move resources
terraform state mv <resource address> <new_resource_address>
# TO remove resource
terraform state rm «resource address>
```

## provisioner

## user_date

## TAINT & UNTAINT

## DEBUGGIN

## MODULE



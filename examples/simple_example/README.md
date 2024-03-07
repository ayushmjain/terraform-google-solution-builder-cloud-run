# Simple Example

This example illustrates how to use the `solution-builder-cloud-run` module.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| backend\_service\_endpoint | Any backend service endpoint that this cloud run service calls | `string` | `null` | no |
| cloud\_run\_service\_image | Cloud Run service container image | `string` | n/a | yes |
| cloud\_run\_service\_name | Cloud Run service name | `string` | n/a | yes |
| cloud\_sql\_database\_connection\_name | Cloud SQL Database connection name | `string` | `null` | no |
| cloud\_sql\_database\_host | Cloud SQL Database host | `string` | `null` | no |
| cloud\_sql\_database\_name | Cloud SQL Database name | `string` | `null` | no |
| cloud\_sql\_dependency | Dependency on Cloud SQL | `any` | `null` | no |
| project\_id | GCP project ID where the cloud run service is created | `string` | n/a | yes |
| redis\_host | Redis host | `string` | `null` | no |
| redis\_port | Redis port | `string` | `null` | no |
| region | GCP region where the cloud run service is created | `string` | n/a | yes |
| vpc\_access\_connector\_id | VPC access connector ID used for accessing a VPC network | `string` | `null` | no |

## Outputs

| Name | Description |
|------|-------------|
| cloud\_run\_service\_endpoint | n/a |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

To provision this example, run the following from within this directory:
- `terraform init` to get the plugins
- `terraform plan` to see the infrastructure plan
- `terraform apply` to apply the infrastructure build
- `terraform destroy` to destroy the built infrastructure

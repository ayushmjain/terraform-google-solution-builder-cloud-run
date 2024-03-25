# terraform-google-solution-builder-cloud-run

## Description
### Tagline
Cloud Run is a managed compute platform that lets you run containers directly on top of Google's scalable infrastructure.

### Detailed
This composition unit creates a Cloud Run service and a Cloud Run service account. This Cloud Run service can be connected to Cloud SQL, Redis.

The resources/services/activations/deletions that this module will create/trigger are:

- Create a Cloud Run service account.
- Create a Cloud Run service.

### PreDeploy
To deploy this blueprint you must have an active billing account and billing permissions.

## Documentation
- [Cloud Run](https://cloud.google.com/run/docs/overview/what-is-cloud-run)

## Cost
[Blueprint cost details](https://cloud.google.com/products/calculator-legacy#id=c5b0d4ca-341f-4636-bfa5-0f5991288c76)

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| annotations | Annotations for cloud run service | `map(string)` | `{}` | no |
| cloud\_run\_service\_image | Cloud Run service container image | `string` | n/a | yes |
| cloud\_run\_service\_name | Cloud Run service name | `string` | n/a | yes |
| dependencies | Dependencies of cloud run service | `list(any)` | `[]` | no |
| env\_variables | Environment variables for cloud run service | `map(string)` | `{}` | no |
| project\_id | GCP project ID where the cloud run service is created | `string` | n/a | yes |
| region | GCP region where the cloud run service is created | `string` | n/a | yes |
| vpc\_access\_connector\_id | VPC access connector ID used for accessing a VPC network | `string` | `null` | no |

## Outputs

| Name | Description |
|------|-------------|
| cloud\_run\_service\_account\_name | n/a |
| cloud\_run\_service\_endpoint | n/a |
| env\_variables | n/a |
| module\_dependency | n/a |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Requirements

These sections describe requirements for using this module.

### Software

The following dependencies must be available:

- [Terraform][terraform] v0.13
- [Terraform Provider for GCP][terraform-provider-gcp] plugin v3.0

### Service Account

A service account with the following roles must be used to provision
the resources of this module:

- Artifact Registry Administrator: `roles/artifactregistry.admin`
- Cloud Run Admin: `roles/run.admin`
- Service Account Admin: `roles/iam.serviceAccountAdmin`
- Service Account User: `roles/iam.serviceAccountUser`

The [Project Factory module][project-factory-module] and the
[IAM module][iam-module] may be used in combination to provision a
service account with the necessary roles applied.

### APIs

A project with the following APIs enabled must be used to host the
resources of this module:

- Compute Engine API: `compute.googleapis.com`
- Cloud Run Admin API: `run.googleapis.com`

The [Project Factory module][project-factory-module] can be used to
provision a project with the necessary APIs enabled.

## Contributing

Refer to the [contribution guidelines](./CONTRIBUTING.md) for
information on contributing to this module.

[iam-module]: https://registry.terraform.io/modules/terraform-google-modules/iam/google
[project-factory-module]: https://registry.terraform.io/modules/terraform-google-modules/project-factory/google
[terraform-provider-gcp]: https://www.terraform.io/docs/providers/google/index.html
[terraform]: https://www.terraform.io/downloads.html

## Security Disclosures

Please see our [security disclosure process](./SECURITY.md).

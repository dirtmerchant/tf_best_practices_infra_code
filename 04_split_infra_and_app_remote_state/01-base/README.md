# Overview

- Creates S3 bucket which will hold Terraform state.
- Create DynamoDB which will be used for locking state.
- Required for [02-app](../02-app) and [03-infra](../03-infra)

## Commands

- Deploy the infra:

  ```sh
  export AWS_DEFAULT_REGION=us-east-1
  terraform init
  terraform plan -out tfplan && terraform apply tfplan
  ```

- Destroy the infra:

  ```sh
  terraform destroy -auto-approve
  ```

## Usage

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| tags | S3 state bucket tags | `map(string)` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| tf\_bucket\_id | Terraform state bucket ID |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

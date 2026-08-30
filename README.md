# Terraform: Up and Running — Study Repo

This repository contains Terraform configurations, notes, experiments, and exercises created while working through ***Terraform: Up and Running, 3rd Edition*** by [Yevgeniy Brikman](https://learning.oreilly.com/search/?query=author%3A%22Yevgeniy%20Brikman%22&sort=relevance&highlight=true).

## Purpose

The goal of this repo is to build practical Terraform experience while working through the concepts in the book.

Rather than organizing everything strictly by chapter, this repository is intentionally structured more like a real Terraform project. Files, modules, and configurations will evolve naturally as new concepts are introduced and existing infrastructure is refactored.

Topics explored include:

* Terraform fundamentals
* Providers and resources
* Input variables and outputs
* Data sources
* State management
* Remote state
* Modules
* Infrastructure reuse
* Terraform workflows
* Testing and validation
* Production Terraform patterns

## Repository Structure

The repository is kept relatively flat and will change as the project grows.

A typical structure may look something like:

```text
.
├── main.tf
├── variables.tf
├── outputs.tf
├── providers.tf
├── terraform.tfvars
├── modules/
├── scripts/
└── README.md
```

Not every file or directory will exist at every stage of the project.

## Prerequisites

The examples primarily use Terraform with AWS.

Useful tools include:

* [Terraform](https://developer.hashicorp.com/terraform)
* AWS CLI
* An AWS account
* Git

Verify Terraform:

```bash
terraform version
```

Verify AWS authentication:

```bash
aws sts get-caller-identity
```

## Common Commands

Initialize the working directory:

```bash
terraform init
```

Format Terraform files:

```bash
terraform fmt
```

Validate the configuration:

```bash
terraform validate
```

Review proposed changes:

```bash
terraform plan
```

Apply changes:

```bash
terraform apply
```

Destroy created infrastructure:

```bash
terraform destroy
```

## About This Repository

This is a hands-on learning repository rather than a polished production infrastructure project.

Configurations may be rewritten, reorganized, or intentionally broken while experimenting with Terraform concepts.

AWS resources created during exercises may incur charges, so temporary infrastructure should be destroyed when it is no longer needed.

## Reference

**Book:** *Terraform: Up and Running, 3rd Edition*
**Author:** Yevgeniy Brikman
**Publisher:** O'Reilly Media

This repository is an independent learning project and is not affiliated with or endorsed by the author or publisher.

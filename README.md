# Terraform: Up and Running — Study Repo

This repository contains Terraform configurations, notes, experiments, and exercises created while working through *Terraform: Up and Running, 3rd Edition* by [Yevgeniy Brikman](https://learning.oreilly.com/search/?query=author%3A%22Yevgeniy%20Brikman%22).

## Purpose

The goal of this repository is to build practical Terraform experience while working through the concepts in the book.

Rather than creating a separate directory for every chapter, each chapter is preserved in its own **Git branch**. Within each branch, the repository is intentionally kept relatively flat so the Terraform code resembles a small real-world project instead of a collection of chapter folders.

This makes it possible to experiment freely while still preserving the completed state of each chapter.

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

## Branch Structure

Each chapter has its own Git branch.

For example:

```text
main
ch2
ch3
ch4
ch5
...
```

A chapter branch represents the state of the Terraform project while working through that chapter.

For example:

```bash
git switch ch2
```

checks out the Chapter 2 version of the project.

```bash
git switch ch3
```

checks out the Chapter 3 version.

New chapter branches are created as **orphan branches**, allowing each chapter to begin with a clean working tree rather than automatically inheriting the Terraform configuration from the previous chapter.

Example:

```bash
git switch --orphan ch4
git rm -rf .
```

After adding the new chapter's Terraform files:

```bash
git add .
git commit -m "Start Chapter 4"
git push -u origin ch4
```

This approach keeps each chapter independently browsable while avoiding a directory structure such as:

```text
chapter-2/
chapter-3/
chapter-4/
```

## Repository Structure

Within each chapter branch, the repository is kept relatively flat and may evolve as concepts are introduced.

A typical branch may look something like:

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

Not every file or directory will exist in every chapter.

The structure is allowed to evolve naturally as Terraform concepts become more advanced.

## Working With the Repository

List available branches:

```bash
git branch -a
```

Switch to a chapter:

```bash
git switch ch2
```

Create the next chapter as a clean branch:

```bash
git switch --orphan ch3
git rm -rf .
```

Create the first commit:

```bash
git add .
git commit -m "Start Chapter 3"
git push -u origin ch3
```

If there are no files to commit yet, an empty commit can be used to publish the branch:

```bash
git commit --allow-empty -m "Start Chapter 3"
git push -u origin ch3
```

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

Each chapter branch serves as a snapshot of that stage of the learning process, making it easy to revisit earlier implementations without requiring all exercises to coexist in the same working tree.

AWS resources created during exercises may incur charges, so temporary infrastructure should be destroyed when it is no longer needed.

## Reference

**Book:** *Terraform: Up and Running, 3rd Edition*
**Author:** Yevgeniy Brikman
**Publisher:** O'Reilly Media

This repository is an independent learning project and is not affiliated with or endorsed by the author or publisher.


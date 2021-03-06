---
layout: "enterprise"
page_title: "Artifacts - Terraform Enterprise (legacy)"
sidebar_current: "docs-enterprise-artifacts"
description: |-
  Terraform Enterprise can be used to store artifacts for use by Terraform. Typically, artifacts are stored with Packer.
---

# About Terraform Artifacts

-> **Deprecation warning**:  The Packer and Artifact Registry features of Atlas will no longer be actively developed or maintained and will be fully decommissioned on Friday, March 30, 2018. Please see our [guide on building immutable infrastructure with Packer on CI/CD](https://www.packer.io/guides/packer-on-cicd/) for ideas on implementing these features yourself.

Terraform Enterprise can be used to store artifacts for use by Terraform.
Typically, artifacts are [stored with Packer](https://packer.io/docs).

Artifacts can be used in to deploy and manage images
of configuration. Artifacts are generic, but can be of varying types
like `amazon.image`. See the Packer [`artifact_type`](https://packer.io/docs/post-processors/atlas.html#artifact_type)
docs for more information.

Packer can create artifacts both while running in and out of Terraform
Enterprise network. This is possible due to the post-processors use of the
public artifact API to store the artifacts.

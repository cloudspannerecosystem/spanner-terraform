# Google Cloud Spanner with Terraform

You can use [Terraform](https://terraform.io) to create, manage and delete Cloud Spanner
resources. Google Terraform modules provide Cloud Spanner support via the following resources:

* [google_spanner_instance](https://www.terraform.io/docs/providers/google/r/spanner_instance)
* [google_spanner_instance_iam](https://www.terraform.io/docs/providers/google/r/spanner_database_iam)
* [google_spanner_database](https://www.terraform.io/docs/providers/google/r/spanner_database)
* [google_spanner_database_iam](https://www.terraform.io/docs/providers/google/r/spanner_database_iam)

## Authentication

Google Terraform modules can be authenticated 

* A service key in JSON format,
  see [documentation](https://www.terraform.io/docs/providers/google/index.html) for more.
* [Application Default Credentials (ADC)](https://cloud.google.com/docs/authentication/getting-started),
  automatically available on GCP machines or via `gcloud auth application-default login`.

## Examples

You can checkout into the following directories and run `terraform apply` to
create a plan and apply changes. The following examples use Application Default
Credentials (ADC) to authenticate. Refer to the
[credentials](https://www.terraform.io/docs/providers/google/index.html) file
to authenticate with a service account.

Edit the main.tf file and replace `YOUR_PROJECT_ID` with your Google Cloud project ID.

* [regional](examples/regional) - Regional cluster with a database.
* [multi-regional](examples/multi-regional) - Multi-regional cluster with a database.
* [lifecycle](examples/lifecycle) - Database protected with lifecycle argument against accidental deletion.

## Codelab

Alternatively, a step-by-step tutorial is also
available as a [codelab](https://codelabs.developers.google.com/codelabs/cloud-spanner-terraform/).

## Issues

Please file bugs and feedback to the Cloud Spanner Terraform resources on the
[Google Terraform Module](https://github.com/terraform-providers/terraform-provider-google).
Issues and feedback to the examples are appreciated on this repo.
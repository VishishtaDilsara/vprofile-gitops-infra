# vprofile-gitops-infra

Terraform for the vProfile EKS infrastructure.

## Pipeline

Two GitHub Actions workflows are included:

1. Pull requests to `main` run `terraform fmt`, `terraform validate`, and `terraform plan`.
2. Manual runs on `main` perform `terraform apply` after a fresh validate/plan cycle.

Slack notifications are sent to the configured channel after PR checks and apply runs.

## Required GitHub Secrets

Set these repository secrets before using the workflows:

1. `AWS_ACCESS_KEY_ID`
2. `AWS_SECRET_ACCESS_KEY`
3. `SLACK_WEBHOOK_URL`

## Notes

The workflows use the S3 backend defined in `backend.tf`. If you change the AWS region, update the workflow environment variables to match.

terraform commit 002
terraform commit 003

Make any change here
another change

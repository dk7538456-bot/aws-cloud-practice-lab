# AWS Cloud Practice Lab

A documented, repeatable practice lab for learning AWS EC2, IAM, and S3 fundamentals. It covers launching a small EC2 instance, applying least-privilege IAM access, and hosting a static page from S3.

> **Cost and security:** AWS resources may incur charges. Use an account or sandbox you are authorized to use, check current pricing and quotas, and remove resources when finished. The S3 website exercise deliberately makes website objects publicly readable; do not upload private data. The S3 website endpoint uses HTTP, so treat it as a learning exercise rather than a production hosting pattern.

## Lab outline

1. [IAM: create a narrowly scoped lab identity](docs/iam-lab.md)
2. [EC2: launch and connect to a small Linux instance](docs/ec2-lab.md)
3. [S3: host a static website](docs/s3-static-website.md)
4. [Clean up resources](docs/cleanup.md)

## Requirements

- An AWS account, training account, or sandbox where you have permission to create IAM, EC2, and S3 resources.
- AWS Console access and (optionally) AWS CLI v2.
- A local copy of this repository.

## Suggested evidence to record

For a portfolio write-up, add screenshots with account IDs and other sensitive details obscured. Record the region, resource configuration, verification steps, and cleanup. Only describe steps you personally completed; the checked-in runbook is a guide, not proof that resources were deployed.

## Folder guide

- `docs/` — guided console exercises and cleanup steps.
- `policies/` — example IAM policy with placeholders to replace before use.
- `site/` — a tiny static page for the S3 exercise.

## License

MIT. See [LICENSE](LICENSE).


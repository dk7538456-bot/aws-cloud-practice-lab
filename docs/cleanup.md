# Cleanup checklist

Before ending the lab, inspect the chosen region and remove resources created just for the exercise:

- Terminate the EC2 instance and verify its state is `terminated`.
- Remove the lab-only security group and key pair after no instance uses them. Delete the local private key securely; never commit it.
- Empty the lab S3 bucket, then delete it.
- Delete lab-only IAM users or roles, access keys (if any), and inline or managed policies created for the exercise.
- Restore the account's original S3 Block Public Access settings if you changed them.
- Review the AWS billing dashboard for unexpected usage.

Some resources cannot be deleted while they are still in use. Resolve those dependencies and check again. Resource names in your account can differ from this guide.


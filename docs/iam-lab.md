# IAM lab: least-privilege access

## Goal

Practice creating a separate lab identity and granting only the S3 access needed for one named lab bucket. Do not use the AWS account root user for day-to-day work.

## Console exercise

1. Sign in using your authorized training or lab account. Enable MFA for privileged identities where available.
2. Create a uniquely named S3 bucket for the lab, noting its exact name and region.
3. In IAM, create a policy based on `../policies/s3-lab-bucket.json`. Replace `REPLACE_WITH_BUCKET_NAME` in both resource ARNs with the bucket name you created.
4. Review the policy before saving. It grants listing on only that bucket and object read/write access within only that bucket; it does not grant bucket deletion or account-wide access.
5. Create a lab user or, preferably when using a compute workload, an IAM role. Attach only the lab policy. Do not create long-lived access keys unless the exercise specifically requires them.
6. Verify the lab identity can list and upload to the chosen bucket. Confirm that an unrelated bucket is not accessible.
7. Remove the user, role attachment, and lab policy when no longer needed.

## Notes

For EC2 applications, prefer an instance profile role over credentials stored on the instance. A website bucket policy that permits anonymous `GetObject` is a separate public-read setting and does not provide administrative access to the bucket.


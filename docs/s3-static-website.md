# S3 lab: static website hosting

## Goal

Host the small sample page in `../site/` from an S3 website endpoint and understand the permissions involved.

## Console exercise

1. Create a globally unique bucket in your chosen region. Keep account- and region-specific information out of this repository.
2. In bucket properties, enable static website hosting and set `index.html` as the index document.
3. For this learning exercise only, configure the bucket's Block Public Access settings to allow the public-read website policy. Do not do this on a bucket containing anything private.
4. Add a bucket policy granting `s3:GetObject` to `Principal: "*"` for objects in this bucket only. Do not grant public list, upload, or delete access.
5. Upload `../site/index.html` and open the website endpoint shown in bucket properties. S3 website hosting uses HTTP.
6. Confirm the page loads, then follow the cleanup guide to delete the object and bucket and restore any changed public-access settings.

## Production note

For a real public website, evaluate HTTPS, a CDN such as CloudFront, origin access controls, logging, and deployment controls. This minimal exercise is for learning the S3 website feature, not a production architecture.


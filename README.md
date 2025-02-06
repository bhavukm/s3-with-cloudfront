# s3-with-cloudfront
AWS Hands-On Project on hosting a Static Website on S3 With CloudFront Distribution

Architectural Diagram:
![image](https://github.com/user-attachments/assets/d44f5dfe-0aba-4c08-98d9-9c677c0bed8f)

1. Domain Registration (Example: website.click): Buy a non-existent domain either from AWS Route53 or from other websites on Internet. (Optional Step)
2. Request a Public Certificate from AWS Certificate Manager (example: *.website.click): This is to use HTTPS-encrypted connections when users use CloudFront.
3. S3 Bucket for Static Website (only HTTP is allowed): Create an S3 bucket with default options and upload your static website content.
4. AWS CloudFront: Create an AWS CloudFront Distribution to server your static website hosted on AWS S3 bucket.
5. Create a DNS record in Route53: Point your CloudFront URL to your website name (choose "A ‐ Routes traffic to an IPv4 address and some AWS resources")




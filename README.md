# s3-with-cloudfront
AWS Hands-On Project on hosting a Static Website on S3 With CloudFront Distribution

Architectural Diagram:
![image](https://github.com/user-attachments/assets/d44f5dfe-0aba-4c08-98d9-9c677c0bed8f)

AWS CloudFront: Is a CDN (Content Delivery Network) based Web Service that speeds up the distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centers called edge locations. When a user requests content that you're serving with CloudFront, the request is routed to the edge location that provides the lowest latency (time delay), so that content is delivered with the best possible performance. 

* If the content is already in the edge location (cached for TTL) with the lowest latency, CloudFront delivers it immediately. 
* If the content is not in that edge location, CloudFront retrieves it from an origin that you've defined—such as an Amazon S3 bucket, a MediaPackage channel, or an HTTP server (for example, a web server) that you have identified as the source for the definitive version of your content.

Steps:

1. Domain Registration (Example: website.click): Buy a non-existent domain either from AWS Route53 or from other websites on Internet. (Optional Step)
2. Request a Public Certificate from AWS Certificate Manager (example: *.website.click): This is to use HTTPS-encrypted connections when users use CloudFront.
3. S3 Bucket for Static Website (only HTTP is allowed): Create an S3 bucket with default options and upload your static website content (index.html file and assets folder from the repo).
4. AWS CloudFront: Create an AWS CloudFront Distribution to server your static website hosted on AWS S3 bucket.
5. Create a DNS record in Route53: Point your CloudFront URL to your website name (choose "A ‐ Routes traffic to an IPv4 address and some AWS resources").
6. Access the website on a browser (example: demo.website.click).

![image](https://github.com/user-attachments/assets/f5289c88-424d-4848-91a7-dafe87a94e74)



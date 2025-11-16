# Project 1 - Deploying Static Website

*Tools: S3, CloudWatch, Route 53, HTTPS (ACM)*

<a href="http://project1-static-webpage.s3-website.us-east-2.amazonaws.com/">Project 1 Static Webpage</a>

### Process:
1. Build static HTML
2. Make S3 bucket for the webapge, ensure ot un-check "Block all public access" option
3. Make JSON bucket policy, can be based on user permission, HTTPS or HTTP, global keys or enterprise keys, which part of the bucket is allowed, requiring MFA or not, preventing user from deleting resources
4. Upload resources to the bucket, ensure that accessible resource is readable right on top (not inside a folder or anything)
5. Start on CloudFront, which is a CDN provider provided by AWS (Free up to 1TB if using Free Tier)
6. Configure CloudFront, ensure to choose the corrrect resources (S3 in this case). Website-endpoint is recommend this time because it is a static webpage
7. for this project, we won't use WAF (Web Application Firewall), but in real life it is very recommended
8. Create the distribution, wait until it is fully deployed. Copy distribution domain name and try accessing it.

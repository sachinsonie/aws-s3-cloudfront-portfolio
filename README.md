Project 1 se (static website on S3 + CloudFront + Route 53 + ACM + WAF

This is my personal portfolio website built with HTML and CSS and deployed on AWS.
The static files are hosted on Amazon S3 and delivered globally using Amazon CloudFront as a CDN.

## Architecture

- Amazon S3 – Hosts the static website (HTML, CSS) using S3 static website hosting.
- Bucket Policy – Allows public read-only access (s3:GetObject) to website files.
- Amazon CloudFront – CDN in front of the S3 website endpoint to improve performance.
- (Planned) Amazon Route 53 – To map a custom domain (e.g., www.myname.com) to CloudFront.
- (Planned) AWS Certificate Manager (ACM) – To issue an SSL certificate for HTTPS on CloudFront.
- (Planned) AWS WAF – To protect the CloudFront distribution using security rules.


## Implementation Steps

1. Built a static portfolio page using HTML and CSS (About Me, Skills, AWS Projects sections).
2. Created an S3 bucket, enabled Static website hosting, and set `index.html` as the index document.
3. Uploaded `index.html` and `style.css` to the S3 bucket.
4. Updated S3 Block Public Access and added a bucket policy allowing public `s3:GetObject` access.
5. Tested the S3 website endpoint to confirm the site loaded correctly.
6. Created an Amazon CloudFront distribution using the S3 website endpoint as the origin.
7. Set `index.html` as the Default root object in CloudFront.
8. Improved the UI with a dark theme, card-style sections, and a responsive grid layout.



## What I Learned

- Hosting a static website on Amazon S3.
- Configuring S3 bucket policies and public access to fix 403 errors.
- Using Amazon CloudFront as a CDN in front of an S3 static website.
- How Route 53, ACM, and WAF fit into a secure static website architecture.

## Screenshot

Home page of the portfolio:

![Portfolio Screenshot](screenshot-home.png)

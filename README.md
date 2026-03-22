# Yewande Faloore- A personal website hosted on AWS

This is a personal portfolio website built and deployed by Yewande Faloore hosted on AWS infrastructure as part of my cloud engineering learning journey.

## What This Project Does
This is a static website hosted using:
- **Amazon S3** — stores the HTML and CSS files
- **CloudFront** — delivers the site fast worldwide with HTTPS
- **IAM** — manages secure access permissions

## These are what i learned from this project
### IAM
- Learned why you never use the root AWS account for your day to day work
- Created a scoped IAM user with only the permissions needed for this specific project. This is called LEAST privilege and it is a security best practice in every cloud environment

### CloudFront CDN Distribution
- Learned how a Content Delivery Network works by deploying CloudFront in front of my S3 bucket
- Understood the concept of edge locations, how CloudFront copies website files to servers around the world so user get fast load times regardless of their location
- Learned how HTTPS works and why it matters ,configured an SSL certificate through AWS Certificate Manager and attached it to my CloudFront distribution to secure the connection between users and my website
- Understood how caching works and why cache invalidation is needed when website files are updated
- Learned the principle of separation of concerns in cloud architecture — S3 stores, CloudFront delivers, IAM secures

### Amazon S3
- Learned how cloud object storage works
- Understood S3 bucket policies and how permissions control who can access files
- Configured S3 for static website hosting

### Route 53 — DNS Management
 - Understood that Route 53 goes beyond basic DNS it can route traffic intelligently based on location, health checks and weighted distribution which is critical in large scale cloud architectures
- Learned that in professional cloud environments all services are mapped to proper domains through DNS, nobody exposes raw AWS URLs to end users

### Git and GitHub
- Learned how version control works and why every cloud engineer needs it
- Understood the workflow of committing changes locally and pushing to a remote repository
- Learned what a .gitignore file is and why protecting credentials from being pushed to GitHub is critical

## How to Deploy
1. Edit files locally in VS Code
2. Upload to S3 using the AWS CLI
3. CloudFront serves the site globally
# AWS EC2 Website Hosting, S3 Backup & CloudWatch Monitoring
http://3.110.155.233/ (click here to view the website)
## Project Overview
This beginner AWS project demonstrates how to host a website on an Amazon EC2 instance, store a backup of the website file in Amazon S3, and monitor CPU utilization using Amazon CloudWatch.

## AWS Services and Tools
- **Amazon EC2:** Runs the website on Amazon Linux 2023.
- **Apache HTTP Server:** Serves the website.
- **Amazon S3:** Stores a backup of the website file in a private bucket.
- **AWS IAM:** Provides permissions to allow the EC2 instance to upload the file to S3.
- **Amazon CloudWatch:** Displays EC2 CPU utilization metrics.
- **AWS CLI:** Uploads the website file to S3.

## Implementation Steps
1. Launched an EC2 instance using Amazon Linux 2023.
2. Installed and started Apache HTTP Server.
3. Created an HTML webpage and accessed it through the browser.
4. Created a private S3 bucket for the website backup.
5. Attached an IAM role with limited S3 upload permissions to the EC2 instance.
6. Uploaded the website file to S3 using the AWS CLI.
7. Viewed the EC2 CPU utilization graph in CloudWatch.

## Architecture

```text
User Browser
     |
     | HTTP
     v
EC2 Instance (Amazon Linux 2023)
     |
     +---- Apache Web Server
     |          |
     |          v
     |      index.html
     |
     +---- AWS CLI + IAM Role
                |
                v
          Private S3 Bucket
          (Website Backup)

EC2 Instance ----> Amazon CloudWatch
                    (CPU Metrics)
```

## Security
- The S3 bucket remains private.
- The EC2 instance uses an IAM role for S3 uploads instead of storing AWS access keys on the instance.
- SSH access should be restricted to trusted sources.

## Future Improvements
- Configure CloudWatch alarms for CPU utilization.
- Enable and verify memory monitoring using the CloudWatch Agent.
- Automate website backups.
- Extend the project with Docker and CI/CD in a future version.

## What I Learned
- Launching and connecting to an EC2 instance.
- Hosting a webpage with Apache on Amazon Linux.
- Using IAM roles and permissions.
- Uploading files to Amazon S3 using the AWS CLI.
- Viewing EC2 monitoring metrics in CloudWatch.


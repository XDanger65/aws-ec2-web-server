# AWS EC2 Web Server Deployment

## Project Overview

This project demonstrates how to deploy a static HTML webpage on an Amazon EC2 instance using Amazon Linux 2023 and Apache HTTP Server.

## Architecture

User Browser → Internet → EC2 Instance → Apache HTTP Server → HTML Webpage

## AWS Services and Technologies

* Amazon EC2
* Amazon Linux 2023
* Apache HTTP Server (httpd)
* EC2 Security Groups
* HTML and CSS
* SSH

## Implementation Steps

1. Launched an EC2 instance using Amazon Linux 2023.
2. Configured a security group to allow SSH (port 22) from my IP and HTTP (port 80) for web access.
3. Connected to the instance using SSH and a private key.
4. Installed Apache using `dnf`.
5. Started and enabled the Apache service.
6. Created a custom webpage at `/var/www/html/index.html`.
7. Verified the deployment through the instance's public IPv4 address.

## Project Structure

```text
aws-ec2-web-server/
├── index.html
├── README.md
└── screenshots/
    └── ec2-website.png
```

## Security Notes

* SSH access should be restricted to trusted IP addresses.
* HTTP is publicly accessible for this demonstration.
* Private keys and credentials must never be committed to GitHub.

## Learning Outcomes

* Launching and configuring EC2 instances.
* Connecting to Linux servers using SSH.
* Installing and managing Linux services.
* Hosting a static webpage on Apache.
* Configuring inbound traffic through security groups.

## Future Improvements

* Configure HTTPS using a domain name and TLS certificate.
* Automate server provisioning with Bash or cloud-init.
* Deploy infrastructure using Terraform.
* Configure monitoring and logging with Amazon CloudWatch.

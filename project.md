Project Documentation: WordPress Deployment on EC2 with Nginx, MySQL, SSL, and GitHub Actions CI/CD
1. Introduction

This document outlines the deployment process of a WordPress site on an EC2 instance using Nginx as the web server, MySQL as the database, a self-signed SSL certificate, and CI/CD with GitHub Actions. This setup ensures efficient deployment, secure access via HTTPS, and streamlined updates using GitHub Actions.

2. Prerequisites

Before setting up the project, ensure the following tools and services are available:

AWS EC2 Instance: A running EC2 instance with Ubuntu 20.04 (or higher) for hosting WordPress.
MySQL Database: MySQL installed and configured on the EC2 instance for WordPress database management.
GitHub Account: A GitHub repository containing the WordPress files.
Domain Name: A registered domain (e.g., mywordpress.work.gd).
Self-Signed SSL Certificate: A self-signed SSL certificate (or purchased SSL certificate).
SSH Access to EC2: SSH keys configured for EC2 access.

3. Steps to Setup WordPress on EC2

Step 1: EC2 Instance Setup
Launch an EC2 instance (Ubuntu 20.04 or higher).
Configure the security group to allow inbound traffic on HTTP (80), HTTPS (443), and SSH (22).
SSH into the EC2 instance.
Step 2: Install Nginx
Install and configure Nginx as the web server.
Step 3: Install PHP and Required Extensions
Install PHP and necessary extensions required by WordPress for running dynamic content.
Step 4: Install MySQL
Install MySQL on the EC2 instance and configure the database for WordPress. Create a database and user with the necessary permissions.
Step 5: Install WordPress
Download WordPress files, extract them, and configure the wp-config.php file to connect to the MySQL database.
Step 6: Configure Nginx for WordPress
Create a new Nginx configuration file for WordPress.
Update the Nginx configuration to point to the WordPress files and handle dynamic content properly with PHP.

4. SSL Setup

Self-Signed SSL Certificate: Generate a self-signed SSL certificate or use a purchased certificate.
Update the Nginx configuration to enable SSL and secure the WordPress site over HTTPS.

5. GitHub Actions CI/CD Configuration

Create a .github/workflows/deploy.yml file in your GitHub repository for automating deployments to the EC2 instance using GitHub Actions.
Configure the workflow to pull the latest code from the repository and deploy it to the EC2 instance via SSH.
Add your EC2 private SSH key as a secret in GitHub to authenticate the deployment process.

6. Access the Website

Once the setup is complete, you can access the WordPress site via:

Domain: https://mywordpress.work.gd
EC2 IP: 52.66.168.73

7. Conclusion

This WordPress deployment setup on EC2 provides a secure and scalable environment for hosting WordPress. The use of Nginx, MySQL, SSL, and CI/CD with GitHub Actions ensures that the site is both high-performing and secure.

Feel free to reach out if you have any questions or need further clarification.

Best regards,
Vamshi Mallavarapu.

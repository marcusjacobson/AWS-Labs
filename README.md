# AWS-Basic-Labs
This repository contains the documentation for various AWS Projects. 

The sections below will cover the details of the different projects in this repo:

## [Build a new Organization and Set Up Users and Groups in IAM](IAM/Build-A-New-Organization-in-IAM.md)
<details>
  <summary>Click to expand/collapse</summary>
  This project consists of 4 sections:
  * Create a new AWS account to manage the Organization
  * Build the OU structure for the Organization
  * Create User Groups in IAM
  * Create User Accounts and Assign to appropriate Groups

  This project demonstrates proficiency in AWS Organizations and IAM, using the AWS Console, CLI and CloudFormation.

  **Note**: The IAM structure built during this project will be referenced in future AWS projects.
</details>

## [Create A Web Server with Auto Scaling](/Create-Web-Server-With-Auto-Scaling/Build-a-Web-Server-Behind-With-Auto-Scaling.md)

This project consists of 8 sections:

* Create a VPC
* Create a series of S3 buckets with replication for the web server to access
* Create a security group for the web server to allow HTTP and HTTPS access
* Create an EC2 instance and set up Apache Web Server
* Connect the web server to the S3 buckets
* Set up an Auto Scaling group
* Stress test the web server to test the functionality of the Auto Scaling group
* Remove AWS assets to avoid recurring charges, and to clean up other remnants from the project.

This project demonstrates proficiency in setting up live EC2 instances with web access, S3 buckts and Auto Scaling groups.

# IAM-Basic-Labs
This repository contains the documentation for various IAM Basic Projects. These projects are practice exercise while preparing for the AWS Certified Solutions Architect Associate certification (SAA-C03) exam.

The sections below will cover the details of the different projects in this repo:

[[_TOC_]]

## [Build a new Organization and Set Up Users and Groups in IAM](IAM\Build-A-New-Organization-in-IAM.md)

This project consists of 4 sections:
* Create a new AWS account to manage the Organization
* Build the OU structure for the Organization
* Create User Groups in IAM
* Create User Accounts and Assign to appropriate Groups

This project demonstrates proficiency in AWS Organizations and IAM, using the AWS Console, CLI and CloudFormation.

**Note**: The IAM structure built during this project will be referenced in future AWS projects.

## Create a Web Server behind an Elastic Load Balancer

This project contains the following elements:
* Create a VPC for the web server with a public subnet and internet gateway
* Create an S3 bucket for web assets, and then create 2 additional buckets as redundant storage for replication.
* Create a security group with web access for the web server.
* Set up an Apache web server on an EC2 instance, and add it to the security group.
* Connect the S3 bucket to the web server, to serve web assets.
* Set up an Elastic Load Balancer to scale out/in the web servers as needed.
* Stress test the web servers to test the Elastic Load Balancer

This project demonstrates proficiency in practical implementations of VPC, S3 buckets, EC2 instances and Elastic Load Balancers
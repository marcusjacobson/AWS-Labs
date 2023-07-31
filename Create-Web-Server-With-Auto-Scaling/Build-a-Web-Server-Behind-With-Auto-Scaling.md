This Project emulates the a practical configuration of a web server, including connected S3 buckets for web assets and implementation of an Elastic Load Balancer to scale out additional instances of the web server as needed based on traffic.

# Project Goal
The goal of this project is to demonstrate proficiency in setting up EC2 instances, Elastic Load Balancers and S3 buckets in a practical use case.

# Setup

* The only pre-requisite for running these projects is to have an active AWS account.
* Created assets may incur charges in the long run, so any chargable assets will be decommisioned/deleted once the project is complete.
* External references are cited within the documents when applicable.

# Project Details

This project consists of the activities below. Click on the hyperlinks to see the processes/details of how these steps were acheived

**Step 1:** [Create a VPC for the web server with a public subnet and internet gateway](/Create-Web-Server-With-Auto-Scaling/1-Create-VPC.md.md)

**Step 2:** [Create an S3 bucket for web assets, and then create 2 additional buckets as redundant storage for replication.](/Create-Web-Server-With-Auto-Scaling/2-Create-S3-Buckets.md)

**Step 3:** [Create a security group with web access for the web server](/Create-Web-Server-With-Auto-Scaling/3-Create-Security-Group.md).

**Step 4:** [Set up an Apache web server on an EC2 instance, and add it to the security group.](/Create-Web-Server-With-Auto-Scaling/4-Create-Web-Server-on-EC2.md)

**Step 5:** [Connect the S3 bucket to the web server, to serve web assets.](/Create-Web-Server-With-Auto-Scaling/5-Connect-Web-Server-to-S3-Buckets.md)

**Step 6:** [Set up an Auto-Scaling group to scale out/in the web servers as needed.](/Create-Web-Server-With-Auto-Scaling/6-Set-Up-Auto-Scaling-Group.md)

**Step 7:** [Stress test the web servers to test the Elastic Load Balancer](/Create-Web-Server-With-Auto-Scaling/7-Stress-Test-Web-Server.md)

**Note**: All AWS assets created during this exercise contains the tag: 
**AWS-Labs:Test-Web-Server**
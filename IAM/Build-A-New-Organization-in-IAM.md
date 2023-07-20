This Project emulates the process of setting up a small organization in AWS. 

**Note:** It is understood that the preferred method for creating users is by connecting federated accounts from another source, but for simplicity I'll just be creating the users directly in IAM. I'll explore integrating federated accounts in a future project. 

# Project Goal
The goal of this project is to demonstrate configuring AWS Organizations and IAM using the AWS Console, CLI and CloudFormation when applicable.

# Setup

* The only pre-requisite for running these projects is to have an active AWS account.
* All IAM items fall under the Free Tier, so no costs will be incurred by this project
* External references are cited within the documents when applicable.

# Project Details

This project consists of the activities below. Click on the hyperlinks to see the processes/details of how these steps were acheived

**Step 1** [Create a new AWS account to manage the Organization](Create-AWS-Account.md)

**Step 2** [Build the OU structure for the Organization](Build-OU-Structure.md)

**Step 3** [Create User Groups in IAM](Create-User-Groups.md)

**Step 4** [Create User Accounts and Assign to appropriate Groups](Create-User-Accounts.MD)

**Note**: All AWS assets created during this exercise contains the tag: **AWS-Labs:Test-Org**


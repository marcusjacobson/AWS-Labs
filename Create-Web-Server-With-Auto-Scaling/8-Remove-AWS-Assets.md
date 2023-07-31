Now that the project has been completed, the following assets will need to be removed to avoid recurring charges, and to generally clean up the AWS account.

# Delete resources that could incur charge

* Delete the Auto Scaling Group. This will need to be done before deleting any EC2 instances, as otherwise the Auto Scaling group will trigger and create more instances.
*  Deleting the Auto-Scaling group will also delete any associated EC2 instances, however double-check to ensure no running instances remain.
* Empty and delete the S3 buckets

# General Cleanup
* Delete the Launch Template
* Deregister the AMI
* Delete the EC2 Security Group
* Delete VPC, Subnets and Internet Gateway. Deleting the VPC should automatically delete the subnets and gateway, but double-check.



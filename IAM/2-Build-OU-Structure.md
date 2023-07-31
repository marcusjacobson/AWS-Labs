# Create Initial OU
To start, I'll create the initial Organizational Unit (OU) in the AWS console, and name it JacoCloud. 

![Initial OU](images\initial-OU.png)

# Create First Child OU

Once the JacoCloud OU is created, I'll create the first Child OU for the IT department:

![Child OU Console Step 1](images\child-OU-console-1.png)

![Child OU Console Step 2](images\child-OU-console-2.png)

# Create Remaining Top Level Child OUs using CLI

For the remaining top level child OUs, I'll use the AWS CLI using the following structure:

    $ aws organizations create-organizational-unit \
        --parent-id parent_ou_id \
        --name New-Child-OU


Notes:
* *parent_ou_id* (line 2) is the OU ID for the OU the new directory will be a child of
* Replace *New-Child-OU* (like 3) with the name of the new OU.

Using this process, the following child OUs will be created:

* HR
* Finance
* Sales-and-Marketing
* Operations

## Sample CLI Output

This is a sample output from the AWS Cloudshell:

**Note**: Senstitive information replaced by asterisks



    [cloudshell-user@ip-10-6-0-159 ~]$ aws organizations create-organizational-unit \
        --parent-id **************** \
        --name HR
    {
        "OrganizationalUnit": {
            "Id": "****************",
            "Arn": "****************",
            "Name": "HR"
        }
    }

# Create Second Level OUs using CloudFormation

I'll use CloudFormation to automate the creation of the remaining OUs. There is some setup required to set up the cloud formation stack, but once that is done all remaining OUs can be created using a single CloudFormation template.

## CloudFormation Prerequisite Setup

The following site is used as reference for creating the CloudFormation Template:

[Deploy AWS Organizations resources by using CloudFormation](https://aws.amazon.com/blogs/security/deploy-aws-organizations-resources-by-using-cloudformation/)

**Note**: The site above also provides the steps to create the IAM policy required for CloudFormation to access Organizations. The following steps will not complete without creating this policy first.

## Create CloudFormation Stack

From the AWS Console, go to CloudFormation and select **Create stack**.

I'll upload the CloudFormation Template provided from the site above, and create the stack as follows:

![Create Stack 1](images\cloud-formation-create-stack-1.png)

![Create Stack 2](images\cloud-formation-create-stack-2.png)

*OU IDs have been redacted for privacy*

![Create Stack 3](images\cloud-formation-create-stack-3.png)

*Note the definition of the IAM role I created earlier*

The stack will automatically run once completed. 

![Run Stack 1](images\cloud-formation-run-stack-1.png)

Once the CloudFormation stack has completed running, it should show a series of CREATE_COMPLETE messages

![Run Stack 2](images\cloud-formation-run-stack-2.png)

Once the CloudFormation stack has completed, verify the additional OUs are present in AWS Organizations:

![Run Stack 3](images\cloud-formation-run-stack-3.png)

# Notes:

* For the time being, I have removed the Service Control Policy statements from the downloadable template.
* The code for the YAML template I used is available here [YAML Code](CloudFormationForAWSOrganizationsYaml.md). Sensitive information has been redacted, and the file type has been changed from YAML to MD to make it easier to view in this document.
* The full list of OUs created for the Org are listed [here](Organizational-Units.md)



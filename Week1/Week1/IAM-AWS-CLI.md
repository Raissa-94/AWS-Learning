# IAM and AWS CLI Basics

## Overview
This section documents what I learned about AWS Identity and Access Management (IAM) and the AWS CLI.

## IAM Users
IAM users represent individual people or applications that need access to AWS resources. 

### What I Practiced
- Created 3 IAM users
- Generated login credentials and i use the credentials of one of my IAM User to sign into my account
- Assigned permissions; Assigned the administratoraccess permission to one of the IAM Users.
- 
- ## IAM Groups
IAM groups allow you to organize users and manage permissions more easily.

### What I Did
- Created a group
- Added users to the group
- Attached policies to the group
# IAM and AWS CLI Basics

## Overview
This section documents what I learned about AWS Identity and Access Management (IAM) and the AWS CLI.

---

## IAM Users

IAM users represent individual people or applications that need access to AWS resources.

### What I Practiced
- Created IAM users
- Generated login credentials
- Assigned permissions

---

## IAM Groups

IAM groups allow you to organize users and manage permissions more easily.

### What I Did
- Created a group
- Added users to the group
- Attached policies to the group

---

## IAM Permissions

Permissions determine what actions users can perform in AWS.

Example:
- Allow EC2 access
- Deny S3 access

---## IAM Policy Structure

Policies are written in **JSON format**.

Example policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "ec2:DescribeInstances",
      "Resource": "*"
    }
  ]
}

### AWS CLI

The AWS CLI allows you to manage AWS services from the command line.

Example command:

aws configure

This command sets up:
The Access Key and Secret key is gotten from the .pem file you downloaded while creating your IAM User

Access Key

Secret Key

Region

Output format

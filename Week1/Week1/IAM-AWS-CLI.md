# IAM and AWS CLI Basics

## Overview
This section documents what I learned about AWS Identity and Access Management (IAM) and the AWS CLI.
- IAM Users
- IAM Groups
- IAM Permissions
- Password Policy
- MFA
- IAM Policy Structure

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

## IAM Permissions

Permissions determine what actions users can perform in AWS.

Example:
- Allow EC2 access
- Deny S3 access

### AWS CLI

The AWS CLI ais used to manage AWS services from the command line using commands
To Give a User or Service access to your AWS Account
aws configure

This command sets up:
The Access Key and Secret key is gotten from the .pem file you downloaded while creating your IAM User

Access Key

Secret Key

Region

Output format
#### Password Policy

A password policy defines the rules users must follow when creating passwords.

**What I Practiced**
- Enabled password policy.
- Set minimum password length
- Required uppercase and lowercase characters
- Required numbers and symbols
- Forced password rotation
Password policies help enforce strong passwords, which improves account security.

#### Multi-Factor Authentication (MFA)

MFA adds an additional layer of security by requiring a second authentication factor.
**MFA= Password + Authentication code from an app**

What I did
- Enabled MFA for an IAM user
- Linked an authenticator app.Downloaded Authy for android
- Tested login with MFA
- Even if someone steals your password, they cannot log in without the second factor.


## IAM Policy Structure

Policies are written using **JSON**.

Example:

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

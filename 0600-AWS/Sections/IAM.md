# IAM

## Overview
IAM = Users and Groups

IAM stands for Identity and Access Management.

It is a global service.

### Users
Users are people that can be grouped.

A user can be in 0-n groups.

### Groups
Groups contain 0-n users.

Groups do not contain other groups.

### Permissions
Users or groups can be assigned policies (JSON document).

It defines what they can and cannot do.

In AWS you should apply the **least privilege principle** (i.e. give the least amount of privileges needed)

The root user can do anything. You only want to use the root when absolutely necessary.

## Example
```
{
  "Version": "2012-10-17",
  "Id": "Admin",
  "Statement": [
    {
      "Sid": "1",
      "Effect": "Allow",
      "Principal":{
        "AWS": ["arn:aws:iam::123123123123:root"]
      },
      "Action": [
        "S3:GetObject",
        "S3:PutObject"
      ]
      "Resource": "*"
    }
  ]
}
```
* **Version**: Policy language version
* **Id**: Optional Identifier of policy
* **Statement**: One or more statements of the policy
  * **Sid**: Optional Identifier of the statement
  * **Effect**: Allow or deny
  * **Principal**: Which account/user/role it is applied to
  * **Action**: List of actions this policy allows or denies
  * **Resource**: List of resources the action applies to
  * **Condition**: Optional list of when this policy is in effect
  * 
## Roles

Some AWS services will need to perform actions on your behalf. Roles provide this ability. Examples are:
* EC2 Instances
* Lamda Functions
* CloudFormation

## Password Policies

You can setup policies on passwords, such as:
* Min Length
* Specific character types
* Allowing users to change their own passwords
* Passsword expiration
* Prevent reuse of passwords

## Two-factor authentication

MFA = Password you know + Device you own

* Virtual MFA Device
  * Google Authenticator (phone)
  * Authy (multi-device)
* U2F Security Key
  * YubiKey
* Hardware Key Fob (Gemalto Token)
* Hardware Key Fob (specific for AWS GovCloud)

## Accessing AWS

Three methods:
* AWS Management Console (Password+MFA)
* AWS CLI (Access Keys) - at the commandline
* AWS SDK (Access Keys) - in code (JS, Python, PHP, Android, iOS, Arduino, and more)

Access Keys are generated through the AWS Console. They are secret, like a password.

## Best Practices
* Don't use root account except for AWS account setup
* Every person should have their own AWS user
* Use access keys for programmatic access
* You can audit your account with the IAM Credentials Report
* You can audit a specific user with the IAM Access Advisor
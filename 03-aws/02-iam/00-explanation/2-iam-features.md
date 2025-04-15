# IAM features

Let's see the features what IAM gives us

## Shared access to your aws account

* You can grant access to others and use the aws resource without sharing your credentials

## Granular permission 

* You can grant different permission to different people for different resources
* For example
    - You can allow some users complete access to Elastic Compute Cloud (EC2), Simple Storage Service (S3) etc..
    - You can also allow read-only access to just some S3 buckets, 
    - You can also allow just some permission to administer EC2 instances
    - You can also just allow access to your billing information but nothing else

## Secure access to AWS resources for applications that run on Amazon EC2
* You can use IAM features to securely provide credentials for applications that run on EC2 instances 
* These credentials provide permissions for your application to access other AWS resources

## Multi-factor authentication (MFA)
* You can add two-factor authentication to your account and to individual users for extra security 
* With MFA users must provide not only credentials to login into account
* Also expected to provide the code from a specially configured device

## Identity federation
* You can allow users who already have passwords elsewhere
* For example, in corporate network we might use identity provider to get temporary access to account

## Free to use
* IAM is the feature of your AWS account offered at no additional charge
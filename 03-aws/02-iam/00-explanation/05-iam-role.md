# IAM Role
An IAM Role in AWS is an identity that grants permissions to entities (users, applications, or AWS services) without needing permanent credentials. Instead of associating credentials with a user, roles use temporary security credentials via AWS STS (Security Token Service).

# Key Points:
No long-term credentials (unlike IAM users).
Can be assumed by AWS services, IAM users, or external entities.
Uses IAM policies to define permissions.
Ideal for cross-account access and service-to-service communication.

# Example Use Cases:
EC2 Instance Role → Grants an EC2 instance permission to access S3.
Cross-Account Role → Allows users from Account A to access resources in Account B.
Lambda Execution Role → Grants AWS Lambda permission to write logs to CloudWatch.
OIDC-based Role → Used for AWS access via GitHub Actions, GitLab, or Kubernetes.

IAM Roles are more secure than IAM users because they avoid hardcoded credentials and use temporary access instead. 🚀  

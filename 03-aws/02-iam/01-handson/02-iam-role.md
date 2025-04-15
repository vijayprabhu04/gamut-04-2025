# Open AWS IAM Console
Go to the IAM console: AWS IAM
In the left menu, click Roles.
Click Create Role.

# Choose the Trusted Entity
Select AWS Service → Choose EC2.
Click Next.

# Attach a Policy (Permissions)
Search for AmazonS3ReadOnlyAccess.
Select the policy and click Next.

# Set Role Name and Create
Enter a role name (e.g., EC2-S3-Access-Role).
Click Create Role.
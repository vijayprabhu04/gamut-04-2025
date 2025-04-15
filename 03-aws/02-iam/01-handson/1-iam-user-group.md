# Create an IAM User
- Sign in to AWS Console
- Go to the AWS Management Console: https://aws.amazon.com/console/
- Navigate to IAM (Identity and Access Management).
- Create a New User
- In the IAM Dashboard, click on Users from the left sidebar.
- Click Add users.
- Enter a User name (e.g., developer-user).
- Choose the Access type:
- AWS Management Console access → If the user needs to log in to the AWS console.
- Programmatic access → If the user needs to use the AWS CLI, SDKs, or API.

# Set Permissions
- Select Add user to a group (skip this if creating the group first).
- You can also attach permissions directly, but it's best to use a group.

# Review and Create
- Click Next, review the details, and click Create user.

# Create an IAM Group
- Navigate to IAM Groups
- In the IAM dashboard, click User groups on the left sidebar.
- Click Create group.
- Set Group Name
- Enter a Group name (e.g., Developers).
- Attach a Policy
- Choose a policy to attach, e.g., AdministratorAccess (for full access) or AmazonS3FullAccess (for S3 access only).
- You can also create a custom policy if needed.
- Create Group
- Click Create group.

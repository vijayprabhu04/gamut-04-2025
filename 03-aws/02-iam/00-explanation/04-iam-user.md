# IAM USER
An IAM User (Identity and Access Management User) in AWS is a specific identity created within an AWS account to represent a person or an application that needs access to AWS resources.

# Key Points:
IAM users have unique credentials (username, password, access keys).
They can be assigned permissions through IAM policies.
They belong to an AWS account but do not have root-level access by default.
Can be part of an IAM Group to inherit permissions.
Used for human users (e.g., developers, administrators) or programmatic access (e.g., CI/CD pipelines, applications).

# Example Use Case:
A developer needs access to AWS resources → You create an IAM user, assign required permissions (e.g., EC2FullAccess), and provide login credentials.
For better security, AWS recommends using IAM roles instead of IAM users whenever possible. 🚀
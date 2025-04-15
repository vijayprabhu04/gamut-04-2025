# IAM Group
An IAM Group in AWS is a collection of IAM users that share the same permissions. Instead of assigning permissions to individual users, you assign them to a group, making management easier.

# Key Points:
Groups don’t have credentials (only users do).
Users in a group inherit the group’s permissions.
A user can belong to multiple groups.
Helps with role-based access control (RBAC) (e.g., Admins, Developers, Read-Only Users).

# Example Use Case:
You create a "Developers" group and attach an EC2 read-only policy.
Add all developers to this group → they automatically get read-only access to EC2.
If access needs to change, update the group policy instead of modifying each user individually.

IAM Groups simplify user management and ensure consistent access control! 🚀
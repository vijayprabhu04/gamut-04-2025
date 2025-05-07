# Deploying an RDS MySQL Database

We will:
- Create an RDS MySQL instance.
- Connect to it from an EC2 instance.
- Perform basic database operations.

# Step 1: Create an RDS MySQL Instance
- Go to AWS Console → RDS → Click Create database.
- Select Standard Create.
- Engine options: Select MySQL.
- Version: Choose the latest version.
- Deployment Option: Single DB instance
- DB instance identifier: my-rds-instance.
- Credentials: Master username: admin && Master password: MySecurePassword123!
- Instance Class: Choose db.t3.micro (Free Tier eligible).
- Storage:
  Storage Type: General Purpose (SSD)
  Allocated Storage: 20 GB
  Enable Auto Scaling: No
- Connectivity:
  VPC: Choose your existing VPC.
  Public Access: Enable (for easy connection from EC2).
  Security Group: Create or choose one that allows MySQL (port 3306).
  Database Options:
  Database name: mydatabase
- Click Create database and wait for deployment.

# Step 2: Connect from an EC2 Instance
- Launch an EC2 instance in the same VPC.
- Install MySQL client: `sudo yum update -y && sudo yum install mysql -y`
- Find RDS Endpoint:
  Go to AWS Console → RDS → Select your database.
  Copy the "Endpoint" (e.g., my-rds-instance.xyz.us-east-1.rds.amazonaws.com).
- Connect to RDS: `mysql -h <RDS-ENDPOINT> -u admin -p`
  Enter your password (MySecurePassword123!).

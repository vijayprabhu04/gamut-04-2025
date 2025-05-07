🛠️ Amazon S3 Hands-on via AWS Console and EC2 (Ubuntu)

✅ Step 1: Create an S3 Bucket
- Go to the S3 Console.
- Click Create bucket.
- Set: Bucket name: my-s3-demo-bucket-<unique-id>
- Region: Same as your EC2 instance
- Leave defaults or uncheck `Block all public access` if you need public files (not recommended for private data).
- Click Create bucket.

✅ Step 2: Launch Ubuntu EC2 Instance (if not already running)
- Go to EC2 Console.
- Launch Ubuntu Server 22.04.
- Choose t2.micro, same region as S3 bucket.
- Ensure port 22 (SSH) is open.
- Launch and note the Public IP and Key Pair.

✅ Step 3: Create an IAM Role for S3 Access
- Go to the IAM Console.
- Click Roles > Create Role.
- Select AWS service > EC2.
- Click Next and search for AmazonS3FullAccess or create a custom policy.
- Name the role `EC2-S3-Access-Role`
- Create the role.

✅ Step 4: Attach IAM Role to EC2 Instance
- Go to EC2 > Instances.
- Select your instance → Actions → Security → Modify IAM Role.
- Choose EC2-S3-Access-Role.
- Click Update IAM role.

✅ Step 5: Connect to EC2 and Install AWS CLI
`ssh -i your-key.pem ubuntu@<EC2-Public-IP>`
Then run:
# Install AWS CLI v2
`curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"`
`unzip awscliv2.zip`
`sudo ./aws/install`

# Test installation:
`aws --version`
You do not need to configure aws configure because the EC2 instance now has an IAM role with S3 permissions.

✅ Step 6: Upload and Download Files from S3
# Create a file
`echo "Hello from EC2 to S3" > testfile.txt`

# Upload to S3
`aws s3 cp testfile.txt s3://my-s3-demo-bucket-<unique-id>/`

# List contents of S3 bucket
`aws s3 ls s3://my-s3-demo-bucket-<unique-id>/`

# Download from S3
`aws s3 cp s3://my-s3-demo-bucket-<unique-id>/testfile.txt downloaded.txt`

# Check downloaded file
`cat downloaded.txt`

🧼 Optional Cleanup
# Delete objects from S3:
`aws s3 rm s3://my-s3-demo-bucket-<unique-id>/testfile.txt`

- Delete bucket from S3 Console.
- Terminate EC2 instance.
- Delete IAM Role if no longer needed.


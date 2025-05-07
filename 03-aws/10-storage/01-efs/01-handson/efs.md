🖥️ Amazon EFS Hands-on via AWS Console
✅ Step 1: Launch an EC2 Instance (if not already running)
- Go to EC2 Dashboard.
- Click Launch Instance.
- Choose: Amazon Linux 2 AMI.
- Instance type: t2.micro (for Free Tier).
- Select an Availability Zone (e.g., us-east-1a).
- Add a security group with ports 22 (SSH) and 2049 (NFS) open.
- Launch the instance.

✅ Step 2: Create a Security Group for EFS
- Go to VPC > Security Groups.
- Click Create security group:
  * Name: EFS-SG
  * Description: Allow NFS access
  * VPC: same as EC2 instance
- Add Inbound rule:
  * Type: NFS
  * Protocol: TCP
  * Port: 2049
  * Source: EC2 instance’s security group
- Click Create security group.

✅ Step 3: Create an EFS File System
- Go to Amazon EFS Console.
- Click Create file system.
- Choose:
  * VPC: same as your EC2 instance
  * Availability Zones: choose the one where EC2 is running
- Automatic mount targets will be created in each subnet (keep defaults).
- In File system policy and access, leave as-is or add tags if needed.
- Click Create.

✅ Step 4: SSH into Ubuntu EC2 and Install NFS Tools
`ssh -i your-key.pem ubuntu@<EC2-Public-IP>`
# Update package list
`sudo apt update`

# Install NFS client
`sudo apt install -y nfs-common`

✅ Step 5: Mount the EFS File System
Get the EFS File System ID (e.g., fs-abc12345) from the EFS console.

# Create a mount directory
`sudo mkdir -p /mnt/efs`

# Mount the EFS using DNS name
`sudo mount -t nfs4 -o nfsvers=4.1 fs-abc12345.efs.<region>.amazonaws.com:/ /mnt/efs`

# Example for us-east-1:
`sudo mount -t nfs4 -o nfsvers=4.1 fs-abc12345.efs.us-east-1.amazonaws.com:/ /mnt/efs`

✅ Step 6: Verify the EFS Mount
# List files
`ls /mnt/efs`

# Write a test file
`echo "EFS is mounted!" | sudo tee /mnt/efs/test.txt`

# Check the content
`cat /mnt/efs/test.txt`

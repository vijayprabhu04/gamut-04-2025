# Step 1: Create Key Pair (if you don't already have one)
- Go to AWS Console → EC2 → Key Pairs.
- Click Create Key Pair.
- Name: my-ubuntu-key (example)
- Key type: RSA
- Private key file format: .pem
It will download a .pem file. Save it safely — you'll need it for SSH

# Step 2: Create or Identify Public Subnet
- Go to VPC → Subnets.
- Make sure you have a subnet:
- Auto-assign public IPv4 is enabled ✅.
- If not, either edit the subnet settings to enable it OR create a new subnet in your VPC.
(This ensures your EC2 will get a public IP to connect.)

# Step 3: Launch Ubuntu EC2 Instance
- Go to EC2 → Instances → Launch Instance.
- Name: ubuntu-server (example)
- Amazon Machine Image (AMI):
- Choose Ubuntu Server 22.04 LTS (or another Ubuntu version you prefer).
- Instance Type: Example: t2.micro (free tier eligible)
- Key Pair: Choose your my-ubuntu-key created earlier.
- Network Settings:
    * VPC: Choose your VPC.
    * Subnet: Select public subnet.
    * Auto-assign public IP: Enable (very important!)
- Firewall Settings (Security Group):
- Create a new security group or use existing.
    * Allow SSH (port 22):
    * Protocol: SSH
    * Port: 22
    * Source: 0.0.0.0/0 (for public access — safe for testing, for production restrict to your IP)
- Click Launch Instance.

# Step 4: Confirm Public IP
- Once instance is running, find its Public IPv4 address in the EC2 dashboard.
- Example: 3.92.123.45

# Step 5: Connect from VS Code Terminal
- Open VS Code.
- Open Terminal (Ctrl + ~).
- Go to the folder where your .pem file is saved.
- Run this command to fix permissions:
  `chmod 400 my-ubuntu-key.pem`
- Now SSH into the instance:
  `ssh -i my-ubuntu-key.pem ubuntu@<your-public-ip>`
Replace <your-public-ip> with the one from AWS.
   `Example: ssh -i my-ubuntu-key.pem ubuntu@3.92.123.45`
- Note: ubuntu is the default username for Ubuntu AMIs.
✅ Done — now you’re inside your Ubuntu EC2 using VS Code terminal!
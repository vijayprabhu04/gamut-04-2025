# Step 1: Allocate Elastic IP
- Go to AWS Console → EC2 → Elastic IPs.
- Click Allocate Elastic IP address.
- Scope: Amazon pool (default option).
- Click Allocate.
✅ You now have a new Elastic IP!

# Step 2: Attach Elastic IP to an EC2 instance
- Select the EIP you just created.
- Click Actions → Associate Elastic IP address.
- Choose: Resource type: Instance
- Instance: Select your EC2 instance (Ubuntu or Windows).
- (Optional) Choose a specific network interface if needed.
- Click Associate.
✅ Now your EC2 instance has a static public IP!

# Step 3: Confirm
- Go to EC2 → Instances.
- Select your instance.
- Under Public IPv4 address, you should now see your Elastic IP assigned.


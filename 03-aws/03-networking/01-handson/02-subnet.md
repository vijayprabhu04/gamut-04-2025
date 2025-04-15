# Prerequisites:
You need an AWS VPC (since subnets belong to a VPC).

# Steps:
- Login to AWS Console → Navigate to VPC Dashboard.
- Click on Subnets → Click Create subnet.
- Choose the VPC where you want to create the subnet.
- Provide: Subnet Name (e.g., my-subnet)
- Availability Zone (Choose one, e.g., us-east-1a)
- IPv4 CIDR Block (e.g., 10.0.1.0/24 → should be a subset of your VPC CIDR)
- Click Create Subnet.
- Optional: Enable Auto-Assign Public IP
- If this subnet is for public instances, edit the subnet and enable auto-assign public IPv4.
# Launch Windows EC2 Instance on AWS and Connect

## Step 1: Create a Key Pair (for RDP password decryption)
- Go to AWS Console → EC2 → Key Pairs.
- Click Create Key Pair.
- Name: my-windows-key
- Key type: RSA
- Private key file format: .pem
- It will download a .pem file — save it safely, you will need it to get the administrator password.

## Step 2: Create or Verify Public Subnet
- Go to VPC → Subnets.
- Ensure the subnet has Auto-assign public IPv4 enabled ✅.
- If not, either edit the subnet or create a new one.

## Step 3: Launch Windows EC2 Instance
- Go to EC2 → Instances → Launch Instance.
- Name: windows-server (example).
- Amazon Machine Image (AMI):
- Choose Microsoft Windows Server 2022 Base (or your required Windows version).
- Instance Type: Example: t2.medium (Windows instances need more memory, minimum 2 GB RAM).
- Key Pair: Choose your previously created my-windows-key.
- Network Settings:
   * VPC: Select your VPC.
   * Subnet: Select your public subnet.
   * Auto-assign public IP: Enable.

- Firewall Settings (Security Group):
   * Allow RDP (port 3389):
   * Protocol: RDP
   * Port range: 3389
   * Source: 0.0.0.0/0 (for testing; for production, restrict to your IP).
- Click Launch Instance.

## Step 4: Get Public IP Address
- After launching, find your instance’s Public IPv4 address in the EC2 dashboard.
- Example: 3.92.123.45

## Step 5: Decrypt Windows Administrator Password
- In EC2 dashboard → Select your instance → Connect → RDP Client tab.
- Click Get Password (it may take a few minutes after launch).
- Upload your .pem file.
- Decrypt to reveal the Administrator Password.
- Save this password.

## Step 6: Connect via RDP
- Option 1: Using Windows built-in RDP
- Open Remote Desktop Connection (mstsc).
- Enter the Public IP.
- Username: Administrator.
- Password: (the one you decrypted).

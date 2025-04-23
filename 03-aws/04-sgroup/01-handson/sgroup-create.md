# Using AWS Console
- Go to AWS VPC Dashboard → Security Groups.
- Click Create Security Group.
- Provide: Name: my-sg
- VPC: Select your existing VPC.

# Add Inbound Rules:
- Allow SSH (22) from your IP (x.x.x.x/32).
- Allow HTTP (80) from everyone (0.0.0.0/0).
- Click Create.
- Attach to EC2 Instance:
- Go to EC2 Instances → Select your instance.
- Click Networking → Change Security Groups.
- Attach the newly created SG.
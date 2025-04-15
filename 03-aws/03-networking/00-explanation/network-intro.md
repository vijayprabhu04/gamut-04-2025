# Networking
AWS Networking provides the infrastructure and services to enable secure and scalable communication between resources within AWS and the internet. It is built on Amazon VPC (Virtual Private Cloud), which allows users to create isolated network environments.

# VPC (Virtual Private Cloud)
- AWS VPC is like having a private piece of land in cloud where you can build & customize your own house (in this case, your network)
- Imagine it as a gated community where you have the freedom to construct your buildings (servers), lay down roads (networking), and control who can come in and out (security), all within a space that's isolated from others.

# Subneting
- Think of subnets as dividing your land into smaller plots.
- Each plot can have a specific purpose, like one for your web servers (public-facing) and another for your databases (private).
- The wizard will ask you to configure at least one subnet.
- Provide a name for your subnet and select an availability zone, which is essentially choosing the neighborhood within the AWS region where your subnet will reside.

# Internet Gateway
- An Internet Gateway is like the main gate to your community, allowing traffic to flow between your VPC and the internet.
- The VPC wizard will usually handle this step for you, attaching an internet gateway to your VPC so that your resources can communicate with the outside world.

# NAT Gateway
- Enables private subnet instances to access the internet securely (e.g., for updates).
- NAT Gateway (managed AWS service) is preferred over NAT Instance for scalability.

# Route Tables
- Controls traffic flow inside a VPC.
- Defines routes to subnets, IGW, NAT, VPNs, etc.
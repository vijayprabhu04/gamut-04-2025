# Introduction to Amazon EC2
- Amazon Elastic Compute Cloud (EC2) is a web service that provides resizable compute capacity (virtual servers) in the AWS cloud. 
- It allows users to launch and manage virtual machines, known as instances, on demand.

# Key Features of EC2
- Scalability – Can scale up or down based on demand.
- Multiple Instance Types – Offers different instance families optimized for compute, memory, or storage.
- Elastic IPs – Static public IPs that can be reassigned.
- Security – Controlled through Security Groups and IAM roles.
- Storage Options – Supports EBS (Elastic Block Store) and Instance Store.
- Networking – Can be assigned private/public IPs and placed in VPC subnets.
- Billing – Pay for what you use (On-Demand, Reserved, Spot Instances).

# Types of EC2 Instances
- General Purpose (e.g., t3, m5) – Balanced CPU, memory, and networking.
- Compute Optimized (e.g., c5, c6g) – Best for CPU-intensive tasks.
- Memory Optimized (e.g., r5, x1) – Designed for memory-intensive applications.
- Storage Optimized (e.g., i3, d2) – High disk performance.
- Accelerated Computing (e.g., g4, p4) – Includes GPUs and FPGAs.

# How EC2 Works
- Choose an AMI (Amazon Machine Image) – Pre-configured OS images (Linux, Windows, etc.).
- Select Instance Type – Choose based on CPU, memory, and storage needs.
- Configure Network & Security:
- Attach to a VPC and Subnet.
- Assign a Security Group (firewall rules).
- Enable Elastic IP (optional).
- Add Storage – Choose EBS volume size and type.
- Launch the Instance – AWS provisions the server.
- Connect to the Instance:
- Linux: SSH using a private key.
- Windows: RDP using a password.

# Pricing Models
- On-Demand – Pay per second/minute; best for short-term use.
- Reserved Instances – Commit for 1-3 years at a discount.
- Spot Instances – Use spare capacity at lower prices but can be interrupted.
- Savings Plans – Flexible discount pricing over time.
- Dedicated Hosts – Physical server reserved for you.

# Use Cases
✅ Web hosting and applications
✅ Running databases (MySQL, PostgreSQL)
✅ Machine learning and big data processing
✅ Development and testing environments
✅ Gaming servers

# Summary
- EC2 is AWS’s virtual server solution with flexible compute power.
- Choose instance types based on workload.
- Use security groups and IAM roles for security.
- Pricing varies based on usage models.
- Supports autoscaling and integration with other AWS services.
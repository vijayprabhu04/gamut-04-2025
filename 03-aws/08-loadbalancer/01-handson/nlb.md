# Deploying a Network Load Balancer (NLB) in AWS

# Scenario
We will:

- Launch two EC2 instances in a VPC.
- Install a simple TCP listener on both instances.
- Set up an NLB to distribute TCP traffic across the instances.
- Test the setup using nc (netcat).

# Step 1: Launch Two EC2 Instances

- Create two EC2 instances (Amazon Linux 2).
- Allow port 80 and port 22 in their security groups.
- Connect to each EC2 instance via SSH and install a simple TCP server.

`sudo yum update -y && sudo yum install -y nc`

- Start a TCP server that listens on port 80

# On Server 1: `echo "Hello from Server 1" | sudo nc -lk -p 80`
# On Server 2: `echo "Hello from Server 2" | sudo nc -lk -p 80`

# Step 2: Create a Network Load Balancer
- Go to AWS Console → EC2 → Load Balancers.
- Click Create Load Balancer → Network Load Balancer.
* Basic Configuration:
  Name: my-nlb
  Scheme: Internet-facing
  IP address type: IPv4
* Listeners:
  Protocol: TCP
  Port: 80
  Forward to: Target Group
* Create a Target Group:
  Target type: Instances
  Protocol: TCP
  Port: 80
  Health Check: TCP
  Register both EC2 instances.
- Click Create

# Step 3: Test the Network Load Balancer using port 80
- Find the DNS name of the NLB in the AWS console.
- Run the following command from any machine: `nc <NLB-DNS-NAME> 80`
- You should see responses like: 
  `Hello from Server 1`
  `Hello from Server 2`
- Repeat multiple times to observe load balancing in action.

# Step 3: Test the Network Load Balancer using port 22
- Try ssh from any maching using NLB dns name everytime you might land in different machine

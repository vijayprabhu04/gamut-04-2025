# Monitor CPU utilization of an EC2 instance

# Step 1: Launch an EC2 Instance
- Go to AWS Console → EC2 → Launch Instance.
- Select Amazon Linux 2 as the AMI.
- Choose an instance type (t2.micro for free-tier).
- Configure Security Group: Allow SSH (22) and HTTP (80).
- Launch the instance and connect via SSH.

# Step 2: Enable CloudWatch Monitoring
- Navigate to EC2 Dashboard → Instances.
- Select the instance and go to the Monitoring tab.
- Click on View in CloudWatch.
- You’ll see default metrics like CPUUtilization, NetworkIn, NetworkOut, etc.

# Step 3: Create a CloudWatch Alarm
- Go to CloudWatch Console → Alarms → Create Alarm.
- Select metric:
- Click Select metric → Choose EC2 → Per-Instance Metrics.
- Select CPUUtilization for your EC2 instance.
- Set conditions:
- Threshold: Greater than 70%.
- Period: 5 minutes.
- Configure actions:
- Choose SNS Notification.
- Create an SNS topic and subscribe with your email.
- Create Alarm.

# Test it: Install a CPU stress tool to generate load.

`sudo yum install stress -y`
`stress --cpu 2 --timeout 300`


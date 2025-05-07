# Send custom application logs to CloudWatch Logs.

# Step 1: Install CloudWatch Agent
- Connect to the EC2 instance.
- Run the following commands:

`sudo yum install amazon-cloudwatch-agent -y`
`sudo mkdir -p /var/log/myapp`
`echo "Hello CloudWatch Logs" | sudo tee /var/log/myapp/app.log`

# Step 2: Configure CloudWatch Agent

`sudo amazon-cloudwatch-agent-config-wizard`

- Select On-premises or Amazon EC2? → Amazon EC2
- Enable logs collection and specify /var/log/myapp/app.log.

# Step 3: Start CloudWatch Agent

`sudo systemctl start amazon-cloudwatch-agent`

- Check CloudWatch Logs Console → Log Groups.
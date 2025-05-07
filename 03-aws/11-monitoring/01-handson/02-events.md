# Automating Actions using CloudWatch Events

## Objective: Automatically stop an EC2 instance when it is idle.

## Step 1: Create a CloudWatch Rule
- Go to CloudWatch Console → Events → Create Rule.
- Select Event Source → EC2 Instance State Change.
- Choose "Idle CPUUtilization < 5% for 30 minutes".
- Set the Target:
    Select EC2 Stop Instance.
    Choose the instance.

🚀 Test it: Leave the EC2 instance idle and see if it stops!
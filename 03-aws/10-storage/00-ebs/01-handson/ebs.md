✅ Step 1: Launch an EC2 Instance (if not already running)
- Go to the EC2 Dashboard.
- Click Launch Instance.
- Choose Amazon Linux 2 AMI.
- Select an instance type (e.g., t2.micro for free tier).
- In Configure Instance, select an Availability Zone (e.g., us-east-1a).
- Complete the launch and wait for the instance to be in running state.

✅ Step 2: Create an EBS Volume
- In the EC2 dashboard, go to Elastic Block Store > Volumes.
- Click Create Volume.
- Set:
  * Volume type: gp3
  * Size: e.g., 5 GiB
  * Availability Zone: Match your EC2 instance's AZ (e.g., us-east-1a)
- Optionally, add a Tag like:
  * Key: Name, Value: MyEBSVolume
- Click Create Volume.

✅ Step 3: Attach the EBS Volume to EC2
- Go to Volumes, right-click the newly created volume.
- Choose Attach Volume.
- Select the EC2 Instance ID.
- Device name: leave default (/dev/xvdf).
- Click Attach.
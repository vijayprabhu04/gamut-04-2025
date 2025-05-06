# What is an EIP (Elastic IP) in AWS?
- Elastic IP (EIP) is a static public IPv4 address provided by AWS.
- Normally, when you launch an EC2 instance, it gets a dynamic public IP — it can change if the instance is stopped and started again.
- With an EIP, you get a permanent IP address that you can:
- Attach to any EC2 instance
- Detach and reassign to another EC2 instance if needed
- This makes sure your server is always reachable with the same IP, even if you reboot it.

# Why use an Elastic IP?
- You need a fixed IP for your EC2, useful for:
- DNS mapping (pointing a domain name to server)
- Production servers
- Disaster recovery (quickly remap the IP to another EC2)
- Without EIP, your server IP may change on reboot — not good for production.

# Key Points about EIP
- Static IP: Does not change until you release it.
- Free when in use:	AWS doesn't charge if the EIP is attached to a running EC2.
- Charged when idle	If you allocate an EIP but don't attach it, AWS charges you!
- 5 EIPs per region	By default, you can have up to 5 Elastic IPs per AWS region.
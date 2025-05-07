# EBS (Elastic Block Store) volumes introduction

## What is an EBS volume?
- Amazon EBS is a block storage service used with Amazon EC2 instances. 
- It behaves like a virtual hard disk that you can attach to EC2 instances to store data persistently (even after the instance is stopped or terminated, if configured).

## Key Concepts
Concept	        Description
----------------------------
Volume Types	gp3 (general purpose SSD), io2/io1 (high IOPS), st1 (throughput HDD), sc1 (cold HDD)
Durability	    Data is replicated within an Availability Zone
Snapshots	    Backups of EBS volumes stored in S3
Encryption	    Can be enabled for data-at-rest security
Attach/Detach	Volumes can be attached to or detached from EC2 instances
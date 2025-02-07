# CI/CD Pipeline for Uptime-Kuma | Get Real-Time Bot Alerts for Server Downtime | Open Source Monitoring

Uptime-Kuma is an open-source self-hosted monitoring tool that provides a sleek interface to track the uptime of websites, services, and APIs. When integrated into a CI/CD pipeline for a blog, it helps ensure continuous availability and performance monitoring. 

Features:
* Real-time monitoring with customizable intervals.
* Alerts via multiple channels (email, Slack, Telegram, etc.).
* Historical data and uptime statistics.
* Sleek, user-friendly interface.
  
Phase 1: Launching EC2 Instance

Setting Up EC2

1. EC2 Instance Launch:
Launched an EC2 instance with Ubuntu OS for the project.

3. Instance Type Selection:
Choose t2.large instance (2 vCPUs, 8 GB RAM) to efficiently handle the workload.

3. Configure Instance Details:
Use the default settings.
Ensure you have selected the correct VPC and subnet.
Click “Next: Add Storage.”

4. Add Storage:
Modify the root volume size to 30 GB.
Click “Next: Add Tags.”

5. Add Tags:
(Optional) Add tags for better management.
Click “Next: Configure Security Group.”

6. Configure Security Group:
Create a new security group.
Set the security group name and description.

Add a rule to allow all traffic (Not recommended for production environments):
Type: All Traffic
Protocol: All
Port Range: All
Port Range : 22, 80, 443, 8080, 9000, 3001, 5000
Source: 0.0.0.0/0 (for IPv4) and ::/0 (for IPv6)

Note: Opening all ports is insecure and should only be done for learning purposes in a controlled environment.
Click “Review and Launch.”

7. Review Instance Launch:
Review all configurations.
Click “Launch.”

After launching EC2 instance associate an Elastic IP to ensure a static public IP address for consistent access.

Phase 2: Security Setup

Installing Jenkins, Docker and Trivy

To Install Jenkins
Connect to your server, and enter these commands to Install Jenkins







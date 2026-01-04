# Highly-Available-Architecture
This setup ensures your application is fault-tolerant, scalable, and responsive even during failures or traffic spikes.

In this module, I will be:

Designing fault-tolerant Multi-AZ architectures
Auto-scaling EC2 instances with health checks and recovery
Configuring DNS failover using Route 53 health checks
Setting up Multi-AZ RDS for database resilience
Setting up Shared Storage with EFS

Services Used 🛠
Amazon EC2 – Auto Scaling app instances across multiple AZs
Application Load Balancer (ALB) – Distribute traffic and monitor instance health
Amazon RDS (Multi-AZ) – Highly available relational database
Amazon Route 53 – DNS routing with health checks and failover
Amazon S3 – Backup for DNS Failover
Amazon EFS – Shared storage across EC2 instances

Architecture Diagram
<img width="816" height="534" alt="Screenshot 2026-01-03 at 5 41 55 PM" src="https://github.com/user-attachments/assets/d436ad57-05e5-414a-bc20-d076c219db83" />




An Amazon RDS MySQL instance with Multi-AZ failover
In this section, I will build the following:
A private database layer that is only accessible from the EC2 application instances
Secure access via Security Groups
Automatic standby replica for failover handling

Added Inbound Security Group for MYSQL 
<img width="1700" height="671" alt="Screenshot 2026-01-04 at 8 54 16 AM" src="https://github.com/user-attachments/assets/bbb62332-433c-4a54-98b8-5f652cdc6fc3" />

Set Up DNS Failover with Route 53
Even with Multi-AZ infrastructure, you need a way to intelligently route user traffic based on system health. In this section, you'll configure Route 53 to route traffic to your application via the ALB and automatically failover if the ALB becomes unhealthy.

In this section, I will build:
A Hosted Zone to manage your domain's DNS records
A Health Check to monitor the application’s availability via the ALB
A Failover Routing Policy using Route 53
An optional backup record (e.g., static S3 site) for failover

Create a Hosted Zone.
<img width="990" height="752" alt="Screenshot 2026-01-04 at 9 31 41 AM" src="https://github.com/user-attachments/assets/42ac00e0-b2ad-4ff7-867d-223f4ab854d6" />




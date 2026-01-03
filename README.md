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

# Cloud-Project
Using the services VPC, Security Groups, EC2, Nat Gatways, RDS, Application Load Balancer, Autoscaling Group, Certificate Manager, EFS, Route 53 and Certificate Manager to host a WordPress Website. 
# Overview
This project showcases the deployment of a WordPress website using a combination of AWS cloud services to achieve scalability, security, and high availability. As a software engineer, the goal was to deepen my understanding of cloud infrastructure and DevOps best practices by creating a fully operational website on the cloud. I also wanted to learn more about relational databases. 

The website is hosted on EC2 instances, leveraging an RDS database for backend data storage. It utilizes Elastic File System (EFS) for shared storage among instances and integrates with AWS Certificate Manager for SSL/TLS encryption. The Application Load Balancer and Autoscaling Group work together to distribute traffic and scale the system automatically. Route 53 is used to configure domain name management, ensuring seamless user access.

Purpose:
This project was developed to learn and demonstrate how to design, deploy, and manage a cloud-based architecture that integrates with a cloud database for a content management system like WordPress. It provides a foundation for hosting websites in a secure and efficient manner, ideal for professional environments.

cloudproject.sophiabeebe.com **This link will not be valid. I am shutting the site down because it costs money to keep up. Please watch the youtube video to see my project.**


[Software Demo Video]([[http://youtube.link.goes.here]](https://youtu.be/zfPN8i5sXMo))

# Cloud Database
The project uses Amazon Relational Database Service (RDS) to host the MySQL database for the WordPress backend.

Database Structure:
The RDS MySQL database stores all WordPress-related data, including user information, posts, pages, and site configuration settings.

Tables: The database includes standard WordPress tables such as wp_users, wp_posts, wp_options, and more.
Scalability: The RDS instance is configured for multi-AZ deployment to ensure high availability and fault tolerance.

Here is the project Reference Architecture: 
![1 _WordPress_Project_Reference_Architecture](https://github.com/user-attachments/assets/5decd037-4830-4a84-af5d-24d38339f038)

# Development Environment
The environment was built within a Virtual Private Cloud (VPC) to provide a secure and isolated network for all services.

Tools Used
Amazon VPC: Configured subnets, route tables, and internet gateways to manage network communication.
NAT Gateway: Allowed secure internet access for private subnets.
EC2 Instances: Hosted WordPress and the application logic.
EFS: Provided shared file storage across multiple EC2 instances.
Application Load Balancer: Distributed incoming traffic among instances.
Autoscaling Group: Ensured elasticity by dynamically adjusting the number of instances.
Certificate Manager: Managed SSL/TLS certificates.
Route 53: Handled DNS and domain name management.

VPC Enviroment
![2 _VPC_Reference_Architecture](https://github.com/user-attachments/assets/8aa772fb-c2d2-4c74-bd4b-52552a459c87)

{Describe the tools that you used to develop the software}
NAT Gateway Structure
![3 _Nat_Gateway_Reference_Architecture](https://github.com/user-attachments/assets/7ef68423-678b-44f6-884a-fe3224f067ca)
WordPress
![4 WordPress_SG](https://github.com/user-attachments/assets/9dca07b3-e598-4dac-acc6-52428845579d)
![5 WordPress_RDS](https://github.com/user-attachments/assets/1332f075-48dc-4e7b-8265-46f8e46f51b2)

WordPress itself is written in PHP, and the deployment was managed using AWS Management Console and CLI. No additional custom software was written for this project, but Bash scripts were used for automation and configuration.

# Useful Websites

{Make a list of websites that you found helpful in this project}

- [Web Hosting AWS]([http://url.link.goes.here](https://aws.amazon.com/websites/))
- [What is a Database?]([http://url.link.goes.here](https://www.oracle.com/database/what-is-database/))
- - [What is the Cloud?]([[http://url.link.goes.here](https://www.oracle.com/database/what-is-database/](https://www.cloudflare.com/learning/cloud/what-is-the-cloud/))

# Future Work

Implement CloudFront CDN: To further improve site performance by caching content closer to users.
Enable Automatic Backups: Configure automated RDS snapshots for data recovery.
Improve Security: Add AWS WAF to block malicious traffic.
Monitoring: Integrate CloudWatch for enhanced performance and availability monitoring.
Optimize Cost: Explore cost-saving options, such as Reserved Instances or Savings Plans.

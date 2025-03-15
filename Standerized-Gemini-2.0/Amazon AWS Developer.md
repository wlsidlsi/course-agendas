**I. Introduction to AWS and Core Services**

*   Understanding Cloud Computing Concepts
    *   Defining cloud computing: IaaS, PaaS, SaaS
    *   Benefits of cloud computing: scalability, cost-effectiveness, flexibility
*   AWS Overview
    *   Regions and Availability Zones
    *   AWS Management Console, CLI, and SDKs
    *   AWS Account Setup and Security Best Practices
*   Identity and Access Management (IAM)
    *   IAM Users, Groups, and Roles
    *   IAM Policies and Permissions
    *   Multi-Factor Authentication (MFA)

**II. Compute Services**

*   Elastic Compute Cloud (EC2)
    *   EC2 Instance Types
    *   Launching and Managing EC2 Instances
    *   Security Groups and Network ACLs
    *   Elastic Block Storage (EBS)
    *   Creating and Managing AMIs (Amazon Machine Images)
    *   EC2 Instance Connect and Session Manager
    *   Practical: Launch a web server on EC2 (e.g., using `apt update && apt install -y nginx`)
*   Elastic Container Service (ECS)
    *   Docker Containerization Fundamentals
        *   Creating and running Docker images using `docker build` and `docker run`
    *   ECS Concepts: Task Definitions, Clusters, Services
    *   Deploying Docker Containers to ECS
    *   Task Definitions: CPU, Memory, Network Mode, Container Definitions
    *   Practical: Deploy a simple containerized application using ECS.
*   Elastic Kubernetes Service (EKS)
    *   Kubernetes Fundamentals
    *   EKS Cluster Creation and Configuration
    *   Deploying Applications to EKS
    *   Understanding Pods, Deployments, and Services in Kubernetes
    *   `kubectl` command-line tool
    *   Practical: Deploy a sample application to EKS using `kubectl apply`.
*   AWS Lambda
    *   Serverless Computing Fundamentals
    *   Creating and Deploying Lambda Functions
    *   Lambda Triggers: API Gateway, S3, DynamoDB
    *   Lambda Layers
    *   Practical: Create a Lambda function that responds to an S3 upload event.

**III. Storage and Database Services**

*   Simple Storage Service (S3)
    *   S3 Buckets and Objects
    *   S3 Storage Classes: Standard, Intelligent-Tiering, Glacier
    *   S3 Object Versioning and Lifecycle Policies
    *   S3 Bucket Policies and Access Control Lists (ACLs)
    *   S3 Pre-signed URLs
    *   Practical: Create an S3 bucket, upload files, and configure versioning.
*   Elastic Block Storage (EBS)
    *   EBS Volume Types: SSD, HDD
    *   Creating and Attaching EBS Volumes to EC2 Instances
    *   EBS Snapshots
    *   Practical: Create an EBS volume and attach it to an EC2 instance; take a snapshot.
*   Relational Database Service (RDS)
    *   RDS Database Engines: MySQL, PostgreSQL, SQL Server, Oracle, MariaDB
    *   Creating and Managing RDS Instances
    *   Database Backups and Restores
    *   Connecting to RDS Instances
    *   Practical: Launch a MySQL RDS instance and connect to it.
*   DynamoDB
    *   NoSQL Database Fundamentals
    *   DynamoDB Tables, Items, and Attributes
    *   Primary Keys and Secondary Indexes
    *   DynamoDB Streams
    *   Practical: Create a DynamoDB table, add items, and query data.
*   Elastic File System (EFS)
    *   Creating and Mounting EFS File Systems
    *   Sharing File Systems Across EC2 Instances
    *   Practical: Create an EFS file system and mount it to multiple EC2 instances.

**IV. Networking and Content Delivery**

*   Virtual Private Cloud (VPC)
    *   VPC Subnets (Public and Private)
    *   Route Tables and Internet Gateways
    *   Network Address Translation (NAT) Gateways
    *   Security Groups and Network ACLs
    *   VPC Peering
    *   Practical: Create a VPC with public and private subnets.
*   Elastic Load Balancing (ELB)
    *   Application Load Balancer (ALB), Network Load Balancer (NLB), Classic Load Balancer (CLB)
    *   Load Balancer Target Groups
    *   Health Checks
    *   Practical: Configure an ALB to distribute traffic across multiple EC2 instances.
*   Route 53
    *   Domain Name System (DNS) Fundamentals
    *   Route 53 Hosted Zones and Record Sets
    *   Routing Policies: Simple, Weighted, Latency-based, Failover
    *   Practical: Register a domain with Route 53 and configure DNS records.
*   CloudFront
    *   Content Delivery Network (CDN) Fundamentals
    *   CloudFront Distributions and Origins
    *   Caching Strategies
    *   Practical: Create a CloudFront distribution to serve static content from an S3 bucket.

**V. Deployment and Automation**

*   CloudFormation
    *   Infrastructure as Code (IaC) Fundamentals
    *   CloudFormation Templates: JSON and YAML
    *   CloudFormation Stacks
    *   Practical: Create a CloudFormation template to deploy an EC2 instance.
*   Elastic Beanstalk
    *   Deploying Applications with Elastic Beanstalk
    *   Supported Platforms: Node.js, Python, Java, PHP, .NET, Ruby, Go, Docker
    *   Environment Configuration
    *   Practical: Deploy a web application using Elastic Beanstalk.
*   CodePipeline
    *   Continuous Integration and Continuous Delivery (CI/CD)
    *   CodePipeline Stages and Actions
    *   Source, Build, and Deploy Stages
    *   Practical: Create a CodePipeline to automatically deploy code changes from a Git repository.
*   CodeBuild
    *   Build Environments and Build Specifications (`buildspec.yml`)
    *   Practical: Configure CodeBuild to build and test your application.
*   CodeDeploy
    *   Deployment Strategies: In-Place, Blue/Green
    *   Deployment Configuration
    *   Practical: Use CodeDeploy to deploy application updates to EC2 instances.

**VI. Monitoring and Security**

*   CloudWatch
    *   Monitoring EC2 Instances, RDS Databases, and other AWS Services
    *   CloudWatch Metrics, Alarms, and Logs
    *   Creating Custom Metrics
    *   Practical: Create CloudWatch alarms to monitor CPU utilization of EC2 instances.
*   CloudTrail
    *   Auditing AWS API Calls
    *   Analyzing CloudTrail Logs
    *   Practical: Analyze CloudTrail logs to identify security events.
*   AWS Config
    *   Evaluating Resource Configurations
    *   Creating AWS Config Rules
    *   Practical: Create an AWS Config rule to ensure that all S3 buckets have encryption enabled.
*   Security Best Practices
    *   Principle of Least Privilege
    *   Data Encryption at Rest and in Transit
    *   Regular Security Audits

**VII. Advanced Topics**

*   AWS Organizations
    *   Managing Multiple AWS Accounts
    *   Organizational Units (OUs)
    *   Service Control Policies (SCPs)
*   AWS Direct Connect and VPN Gateway
    *   Hybrid Cloud Architectures
    *   Connecting On-Premises Networks to AWS
*   AWS Step Functions
    *   Orchestrating Serverless Workflows
    *   State Machines and Tasks
*   AWS Machine Learning Services
    *   Amazon SageMaker
    *   Amazon Rekognition
    *   Amazon Comprehend
*   AWS IoT Core
    *   Connecting and Managing IoT Devices

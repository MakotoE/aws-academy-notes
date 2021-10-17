# Types of cloud service models:
- Infrastructure as a Service: Virtual machines are provided
- Platform as a Service: The underlying framework is provided so that code can be run on it
- Software as a Service: The software suite is provided

# Advantages to cloud computing:
- Trade capital expense for variable expense
- Massive economies of scale: More units of service is provided for less input cost
- No need to guess required capacity
- Increased speed and agility
- Money goes to the software side of service instead of the hardware
- Rapid deployment

# Major AWS Services
- Computer services
  - Amazon Elastic Compute Cloud (EC2)
    - Virtual machines
  - AWS Lambda
    - Serverless compute platform
  - AWS Elastic Beanstalk
    - Web application services
  - Amazon Elastic Container Service (ECS)
    - Container orchestration service
  - Amazon Elastic Kubernetes Service (EKS)
  - Amazon Elastic Container Registry (ECR)
    - Container storage
  - Amazon Fargate
    - Serverless container platform
- Security, Identity, and Compliance services
  - AWS Identity and Access Management (IAM)
  - Amazon Cognito
    - User access control for apps
  - AWS Shield
    - DDoS protection
  - AWS Artifact
    - View AWS security and compliance reports
  - AWS Key Management Service (KMS)
- Storage services
  - Amazon Simple Storage Service (S3)
    - Object storage (Media with optional metadata)
  - Amazon Elastic File System (EFS)
    - File storage
  - Amazon Elastic Block Store (EBS)
    - Block storage (Low-level blocks of bytes)
- Database services
  - Amazon Relational Database Service (RDS)
    - Relational database
  - Amazon DynamoDB
    - Key-value storage with in-memory caching
  - Amazon Redshift
    - Data analysis
  - Amazon Aurora
    - High speed MySQL and PostgreSQL database
- Networking and Content Delivery services
  - Amazon Virtual Private Cloud (VPC)
    - Network isolation
  - Amazon Route 53
    - DNS
  - Amazon CloudFront
    - CDN
  - Elastic Load Balancing
- Management and Governance services
  - AWS Trusted Advisor
    - Provides recommendations to optimize efficiency and expenditures
  - AWS CloudWatch
    - Monitor resources
  - AWS CloudTrail
    - Track user activity and API usage
  - AWS Well-Architected Tool
    - Reviews the system architecture for efficiency and security 
  - AWS Auto Scaling
  - AWS CLI
  - AWS Config
  - AWS Management Console
  - AWS Organizations
- AWS Cost Management services
  - AWS Cost & Usage Report
  - AWS Budgets
  - AWS Cost Explorer

# AWS Cloud Adoption Framework
- The AWS CAF provides guidance and best practices for cloud adoption
- Divided into six perspectives
- Business
  - Business
  - People
  - Governance
- Technical
  - Platform
  - Security
  - Operations

# AWS pricing philosophy
- Compute: Charged per duration
- Storage: Charged per GB
- Data transfer: Charged per outbound external data transfer (not inbound or inter-AWS service transfer)

# Total cost of ownership
- The total cost of an AWS ecosystem may include server, storage, network and support
- AWS Pricing Calculator can be used to estimate total cost of ownership

# AWS management
- AWS Organizations is a management service for centralized billing and account management
- AWS Identity and Access Management (IAM) sets up access policies
- AWS Billing and Cost Management is used to pay AWS bills and monitor costs

# AWS support
- Different tiers of support plans: Basic, Developer, Business, Enterprise
- AWS Technical Account Manager: Support staff who provides guidance for AWS solutions
- AWS Trusted Advisor: Cloud export that looks for ways to optimize expenditures

# AWS global infrastructure
- Region
  - A region is a cluster of cloud infrastructure, and divides all data centers by geographic location
  - Data may be replicated across regions
- Availability zone
  - Each region has multiple availability zones, which are fully isolated partitions of AWS infrastructure
  - Designed for fault isolation
  - By using different availability zones, applications are better protected from outages caused by natural disasters
- Points of presence
  - CDN edge locations for low latency content delivery

After completing this module, you should be able to:
Recognize the shared responsibility model
Identify the responsibility of the customer and AWS
Recognize IAM users, groups, and roles
Describe different types of security credentials in IAM
Identify the steps to securing a new AWS account
Explore IAM users and groups
Recognize how to secure AWS data
Recognize AWS compliance programs

# Shared responsibility model
- AWS is responsible for protecting the hardware, software, and facilities that run AWS services
- The customer is responsible for application security, for example:
  - Correct configuration of AWS services
  - Operating systems on compute instances
  - Authentication of users

# AWS IAM
- AWS IAM can manage user access to AWS resources, by defining fine-grained access rights:
  - Who can access the resource
  - Which resources can be accessed
  - How resources can be accessed
- IAM components
  - IAM user: A person or application that authenticates with an AWS account
  - IAM group: A collection of IAM users
  - IAM policy: Defines which resources can be accessed and the level of access to each resource, and can be attached to users, groups, roles, and/or resources
  - IAM role: Grants temporary access to specific resources
- Types of access for an IAM user:
  - Programmatic access
    - Authenticate using access key ID and secret access key
  - Management Console access
    - Authenticate using Account ID or alias, username, password, and/or authentication code
- Inline policy: A one-off policy for just one user or group

# Securing a new account
- An AWS account root user has full access to all AWS services and resources
- The root user should be used to create IAM users and assign permissions to those users
  - An administrator account can be created which has full access to necessary services
  - The root user should only be used when necessary, and the IAM user of necessary access scope should be used for everyday use
- A password policy for all users should be created
- Use AWS CloudTrail (enabled by default) for event logs
- Start a billing report with AWS Cost and Usage Report

# Compliance programs
- AWS Config can be used to evaluate resource configurations to meet regulations
- AWS Artifact provides security and compliance reports for AWS services
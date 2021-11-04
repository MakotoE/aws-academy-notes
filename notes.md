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
    - NoSQL database
  - Amazon ElastiCache
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

# Classless Inter-Domain Routing (CIDR)
- A method for allocating IP addresses
- Example CIDR: 192.0.2.0/24
- The IP prefix indicates start of range
- The number after the slash indicates network mask prefix length
  - The smaller the number, the more addresses are in the allocation range

# Amazon VPC
- Provisions an isolated virtual network
- Belongs to a single AWS Region and spans multiple Availability Zones
- Subnet
  - Subdivisions of a VPC
  - Belongs to a single Availability Zone
- Elastic network interface: Static IP address that can be remapped between different instances on demand
- Route table: A set of rules to direct network traffic
- Network address translation gateway: Enables instances in a private subnet to communicate with the internet but blocks incoming internet traffic
- VPC peering: a network connection between two VPCs
- Site-to-Site VPN: Allows VPC to connect to a remote network. Commonly used to connect to outside data centers.
- AWS Direct Connect: Similar to Site-to-Site but this is for high-bandwidth requirements. Connects a data center directly to an AWS data center using a fiber-optic connection.
- AWS Transit Gateway: A central hub for managing VPC connections
- VPC security
  - Security group
    - A subnet firewall to filter traffic
    - Stateful, meaning decisions can be based on previous traffic activity
    - Allow rules only
  - Network access control list
    - Subnet firewall
    - Stateless
    - Allow and deny rules

# Amazon Route 53
- DNS service
- Can run health checks
- Can register domain names
- Various types of routing policies
  - Simple routing: For single-server environments
  - Weighted round-robin routing: Assign weights to resources
  - Latency routing: Priorities low latency
  - Geolocation routing
  - Geoproximity routing
  - Failover routing: Redirects to an alternative if a health check fails
  - Multivalue: Picks from various records at random

# Amazon CloudFront
- CDN service
- Edge location: Serves the most popular content and is closest to users
- Regional edge cache: Serves less popular content and is further away

After completing this module, you should be able to:
Provide an overview of different AWS compute services in the cloud
Demonstrate why to use Amazon Elastic Compute Cloud (Amazon EC2)
Identify the functionality in the EC2 console
Perform basic functions in EC2 to build a virtual computing environment
Identify EC2 cost optimization elements
Demonstrate when to use AWS Elastic Beanstalk
Demonstrate when to use AWS Lambda
Identify how to run containerized applications in a cluster of managed servers

# Amazon EC2
- Secure, resizable, on-demand virtual machines
- EC2 launch instance wizard pages
  - AMI
    - Amazon Machine Image
    - Supports Windows and Linux
  - Instance type
    - Different hardware capabilities to fit the workload
    - Choose between different memory sizes, processing power, disk space, and network performance
    - Instance type identifier: For a t2.large, t is the family name, 3 is the generation number, and large is the size
  - Network setting
    - Choose the VPC and subnet to deploy in
  - IAM role
    - Attach an IAM role to the instance
  - User data
    - A script to run at startup
  - Storage option
    - Configure root volume and additional volumes
    - An EBS block can be attached for persistent data after termination
  - Tags
    - Metadata
  - Security group
  - Key pair
    - Used to connect to the instance, such as for SSH
- EC2 cost optimization
  - Different pricing models
    - On-demand
      - For unpredictable, short-term workloads
    - Spot instance
      - Price changes based on demand
      - Flexible scheduling and durations
    - Reserved instance
      - Reserve on a yearly basis
      - Steady workloads
    - Dedicated host
      - Reserves hardware for the instance 
      - For specific software licenses
  - To optimize cost
    - Choose the optimal instance type and size
    - Increase elasticity: Design for automatic scaling to handle peak loads
    - Choose the optimal pricing model
    - Optimize storage options
  - Cost allocation tagging: Provides information about what resources are being used by whom and for what purpose
- Amazon ECS
  - Container management service
  - Supports Docker
  - Can be backed by EC2 or Fargate
    - EC2: Need to specify the details and scaling strategy for the EC2 instances
    - Fargate: AWS manages the EC2 instances
  - Task definition: Describes the containers that form the application, such as the image, ports to open, storage volumes
  - ECS cluster: A group of EC2 instances that is running an ECS container agent
- Amazon ECR: Container registry for storing containers
- AWS Lambda
  - Serverless computing platform which allows you to run code without managing the virtual machines
  - Triggered by an event
  - Used to run tasks
  - As a maximum duration limit
- AWS Elastic Beanstalk
  - Managed service similar to Lambda
  - Elastic Beanstalk is not triggered by events
  - Used for web applications
  - Can run continuously

# Storage services
- Amazon EBS
  - Block storage
  - Can be used as persistent storage for EC2 instances
  - Allows partial file changes
    - With object storage, the entire file must be replaced
  - Snapshots can be made to create a copy of a volume at a point in time
  - Pricing
    - Charged by amount provisioned per month
    - Inbound data transfer is free
    - Outbound data across Regions incurs charges
- Amazon S3
  - Object storage 
  - Bucket: A group of objects
  - Storage classes
    - Standard: Low latency and high throughput
    - Intelligent-tiering: Optimizes costs by monitoring access patterns to automatically move data to the optimal tier
    - Standard-Infrequent Access: Has the same latency as standard but with low storage price and an added per-GB retrieval fee
    - One Zone-Infrequent access: Same as Standard-IA but objects are stored in one Availability Zone only, meaning less resilience
    - Glacier
      - Low-cost storage class for archiving, and takes a long time to retrieve objects
      - Vault: A collection of archives
    - Glacier Deep Archive: Even lower costs but with a longer retrieval time
  - Objects can be encrypted with a S3 managed keys, with customer provided keys, and/or with AWS KMS keys
  - Charged for
    - Per-GB in storage
    - Transfer out to other regions
    - HTTP requests
  - Amazon EFS
    - File storage
    - Can be mounted to multiple EC2 instances concurrently as a network file system

# Database services
- Amazon RDS
  - Supports relational databases
  - Can be run in a VPC
  - Multi-AZ deployment: Creating a main database and a synchronously replicated standby database in a different Availability Zone to increase availability
  - Read replica: A read-only copy of the main database to improve latencies on the main database
  - Charged for
    - Service time (From instance launch to termination)
    - Instance type
    - Additional storage (Provisioned storage is not charged)
    - Number of requests
    - Outbound data transfer
- Amazon DynamoDB
  - NoSQL database
  - Main components of NoSQL: table/document, items, attributes
  - Highly scalable
  - Retrieving data
    - Query operation is used to find items by primary key
    - Scan operation is used to find an item by a non-key attribute
- Amazon Redshift
  - Accelerated analytics queries
  - Parallelized processing: The leader node assigns small divisions of tasks to multiple compute nodes
- Amazon Aurora
  - High-performance MySQL and PostgreSQL databases
  - Can be stored in multiple AZ for high availability

# AWS Well-Architected Framework
- Operational excellence
  - Focus: Run and monitor systems to deliver business value; continually improve supporting processes and procedures
  - Perform operations as code
    - Store workloads and systems in code
  - Make frequent, small, reversible changes
  - Refine operations procedures frequently
  - Anticipate failure
    - Test failure scenarios
  - Learn from operational failures
- Security
  - Focus: Protect information, systems, and assets; assess risks and mitigation strategies
  - Implement a strong identity foundation
    - Implement the principle of least privilege; enforce separation of duties; centralize privilege management
  - Enable traceability
  - Apply security at all layers
    - Defense in depth
  - Automate security best practices
    - Enables scaling without requiring more human resources
  - Protect data in transit and at rest
  - Prepare for security events
    - Have an incident management process and run simulations
- Reliability
  - Focus: Ensure a workload works correctly and consistently
  - Automatically recover from failure
    - Trigger failover automatically instead of manually
  - Test recovery processes
  - Scale horizontally to increase aggregate workload availability
    - Instead of one large resource, split it into multiple smaller ones so that system-wide failure is less likely
  - Stop guessing capacity
    - Automate scaling
  - Manage change in automation
    - Automate the process of making changes to infrastructure
- Performance efficiency
  - Focus: Use IT and computing resources efficiently to meet system requirements
  - Democratize advanced technologies
    - Consume technologies as a service so that people less proficient with technologies can use them without knowing how to manage them
  - Go global in minutes
  - Use serverless architectures
  - Experiment more often
    - Compare different types of instances and configurations
  - Consider mechanical sympathy
    - Use technologies are best optimized for a workflow
- Cost optimization
  - Focus: Avoid unnecessary costs
  - Implement cloud financial management
    - Use cloud services to manage finances
  - Adopt a consumption model
    - Pay only for resources that are needed
  - Measure overall efficiency
    - Measure business output vs costs
  - Stop spending money on undifferentiated heavy lifting
    - Avoid doing the hard work of managing hardware
  - Analyze and attribute expenditure
    - Analyze costs of individual workloads to measure return on investment
- AWS Well-Architected Tool helps review the state of your workloads

# Reliability
- Assume anything can break
- Mean time between failure = mean time to failure + mean time to repair
- Availability: A percentage of time that a system is operating normally
- Highly available system
  - A system that can withstand some degradation while still remaining available
  - Minimizes downtime by quickly restoring services
- Factors that influence availability
  - Fault tolerance
  - Scalability
  - Recoverability

# Load balancing and auto-scaling
- A load balancer ensures high availability and fault-tolerance
- Types of load Elastic Load Balancers
  - Application load balancer
    - Application level
    - Routes traffic based on content of request
  - Network load balancer
    - Transport level
    - Routes traffic based on IP header data
    - Has ultra-low latency
  - Classic load balancer
    - Operates at application and transport level
    - Not recommended for use
- Listener: A process that checks for requests
- Target group: The destination of traffic from load balancer
- Elastic Load Balancers can be monitored with CloudWatch and logged with CloudTrail
- An Elastic Load Balancer can perform health checks
- EC2 Auto Scaling group
  - A collection of EC2 instances that is scaled as needed
  - A launch configuration defines how each instance should be launched
  - An Elastic Load Balancer can be attached to distribute incoming traffic across instances
  - Scaling options
    - Maintain current instance level: Constant number of instances
    - Manual scaling: Specifies max, min, and desired capacity
    - Scheduled scaling: Scaling is planned according to time
    - Dynamic, on-demand scaling: Uses metrics such as CPU utilization to decide on scaling level; can also be triggered by a CloudWatch alarm
    - Predictive scaling: Uses machine learning models to predict expected traffic to determine scaling level
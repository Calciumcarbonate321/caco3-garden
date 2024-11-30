---
dg-publish: true
---
Module 2
#### Amazon EC2
Basically virtual machines. Scalable cloud compute service  that allows users to run virtual servers known as instances in AWS data centers. 

##### Features
1. Elasticity and scalability
2. Variety of instance types: Many instance types are there and can use AMI(Amazon Machine Image) as a template to create and launch new instances.
3. Configurability
4. Pay-As-You-Go pricing
5. Easy integration with other AWS services
6. Security
7. Security groups act as firewalls for instances to control inbound and outbound traffic.
8. Monitoring and management 
9. EBS(Elastic Block Storage) provides persistent block storage volumes for use with EC2 instances.
10. Placement groups allow you to influence placement within AWS infrastructure(used to ensure low latency).
##### Benefits
1. AWS Regions and AZs improve stability and reduce latency
2. Use EC2 fleet to optimize scale, performance and cost.
3. Elastic Fabric Adapter to run applications that require high levels of interinstance communications(basically an IPC)
4. AWS Private Link to access other Amazon services.
5. Regular maintenance done by AWS.
##### Pricing options
1. Standard reserved instances(75% discount if long term)
2. Convertible reserved instances(54% discount)
3. Scheduled reserved instances
4. Spot instances(cheapest)

#### Amazon S3
S3 means Simple Storage Service. Secure, scalable and high performance object storage service by AWS. High scalability. 11 nines stability(99.999999999%)

##### Key concepts
1. **Buckets** are containers used for storing files. Each bucket is globally unique and can contain unlimited number of objects.
2. **Objects** are individua files stored in S3. Each Object consists of the data, a unique key and optional metadata.
3. **Permissions and Access Control**: S3 uses IAM and ACLs to manage data securely.
4. **Versioning**: S3 allows versioning and keep multiple versions of the same object to protect against accidental deleting.
##### Advantages
1. Scalable
2. Durable
3. Secure
4. High availability 
5. Low cost
6. Ease of integration with other AWS services
7. Flexible storage options
##### Challenges
1. Complex pricing
2. Latency when accessing large datasets
3. Complex access control with large teams

#### Amazon RDS
Relational Database Service is a fully managed database services that simplifies the setup, operation and scaling of relational databases in the cloud.
MySQL, PostgreSQL, Oracle, SQL Server, and
MariaDB.
##### Components of RDS
1. **DB Instance**: A VPS where the db runs.
2. **DB Engine:** The RDBMS engine(like postgres or mysql)
3. **DB Storage**: Storage used to store the data(usually EBS)
4. **DB Parameter Group**: A collection of settings that control the behavior of the DB engine.
5. **DB Security Group**: Firewall and access rules.
6. **Multi-AZ Deployment**: Provides high availability by replicating data to a standby instance in
another availability zone.
7. **Read Replicas**: Used to offload read queries, improving performance for read-heavy
workloads.
![[RDS.png]]
##### Advantages
1. High availability due to Multi AZ deployments.
2. Scalability
3. Security(encrypted data at rest and in transit)
4. Monitoring and management using cloud watch
5. Automated Backups
6. Cost Effective(since it is managed service)
##### Challenges
1. Vendor lock in
2. limited control
3. Performance for big data

#### Amazon VPC
Virtual Private Cloud allows users to create isolated, secure virtual networks within AWS
![[VPC.png]]
##### Key features
1. Isolation
2. Subnets: Can divide the VPC into public and private subnets for different groups
3. Security
4. Custom IP addressing(own private IP ranges and subnets)
5. VPN connectivity
6. Peering between VPCs
7. Elastic IPs and NAT
##### Advantages
1. Isolation and security
2. Customizable network architecture
3. Scalability
4. Hybrid Cloud connectivity
5. High availability
6. Internet and private connectivity
7. Cost control
##### Challenges of VPC
1. Complex in config
2. Network management overhead as VPCs grow in complexity
3. Limited public IPs
4. Latency and bandwidth constraints
5. Peering limitations
6. Cost of additional services
7. Tough to troubleshoot

#### Amazon SQS
![[SQS.png]]![[SQS_2.png]]
Messages can be max 256kb in size. Can be JSON, XML or plain text.
Message stored in queue temporarily
FIFO queues 
##### Advantages
1. **Decoupling Components:** Enhances flexibility and independent scaling of microservices.
2. **Reliability:** Ensures message delivery with redundancy and fault tolerance.
3. **Scalability:** Handles virtually unlimited messages.
4. **Asynchronous Communication:** Allows producers and consumers to operate independently.
5. **Managed Service:** Reduces operational overhead with built-in scaling and fault tolerance.
6. **AWS Integration:** Works seamlessly with services like Lambda, SNS, and CloudWatch.
7. **Cost-Effective:** Pay-as-you-go model optimizes costs.
8. **Security:** Supports encryption and IAM-based access control.
##### Challenges
1. **Message Ordering:** Standard queues don’t guarantee order; FIFO queues may have lower throughput.
2. **Visibility Timeout:** Requires careful management to avoid message duplication or delays.
3. **Message Size Limit:** 256 KB limit may require alternate solutions like Amazon S3 for larger payloads.
4. **Message Retention:** Messages are retained for up to 14 days, risking loss if unprocessed.
5. **Latency:** Possible delays in processing during traffic spikes or polling.
6. **DLQ Management:** Needs additional configuration and monitoring for failed messages.
7. **FIFO Queue Limits:** Throughput is capped at 300–3,000 TPS.
8. **No Message Prioritization:** Lacks built-in prioritization, requiring custom implementations.

### Amazon SNS
Simple Notification Service allows to send notifications to large number of subscribers or endpoints.
![[sns-delivery-protocols.png]]

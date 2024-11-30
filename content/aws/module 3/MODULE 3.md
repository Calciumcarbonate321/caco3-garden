---
dg-publish: true
---
Module 3
#### AWS Lambda
Serverless compute service that allows you to run code in response to events without provisioning or managing servers.
It lets a person automatically run code in response to
many types of events, such as HTTP requests from the Amazon API gateway, table updates in
Amazon DynamoDB, and state transitions.
![[product-page-diagram_Lambda-RealTimeStreamProcessing.d79d55b5f3a5d6b58142a6c0fc8a29eadc81c02b.png]]
![[product-page-diagram_Lambda-RealTimeFileProcessing.a59577de4b6471674a540b878b0b684e0249a18c.png]]
##### Key features
1. serverless compute
2. event driven
3. auto scaling 
4. pay as you go
5. concurrency control
6. monitoring and logging
7. built in fault tolerance(auto retries, dead-letter queues and error handling)
##### Advantages
1. No server management
2. Cost savings
3. Ease of use
##### Disadvantages
1. Execution time of max 15mins
2. Cold starts
3. Resource limits

#### Amazon DynamoDB
Managed No-SQL DB from AWS that provides fast and predictable performance with seamless scalability.
##### Key features
1. Fully managed
2. Scalability
3. Low latency and high throughput
4. Flexible data model
5. Global tables
6. Integrated with AWS Ecosystem
7. Security(Encryption, IAM and VPC endpoints)
8. Transactions(ACID)
9. Streams(for real-time data)
10. Backup and restore
##### Advantages
1. High availability and durability
2. Fully managed
3. Low latency
4. Scalable and flexible
5. Serverless integration(with lambda)
6. Security
##### Disadvantages
1. Limited querying flexibility
2. Provisioned capacity limits
3. Consistency modes
4. Small item size of only 400kb per item
5. Complexity increases with large data

#### Amazon ECS
Elastic Container Service AKA EC2 Container Service is a managed service that allows users to run Docker-based applications packaged as containers across a cluster of EC2 instances.
With ECS, Fargate launch type, the load and responsibility of EC2 cluster is transferred over to AWS.
##### Key features
1. Fully managed
2. Scalability
3. Integration with AWS services
4. Fargate support
5. Task definitions can be used to say how containers should run
6. Service scheduling can start/stop in schedule.
7. ECS cluster management
##### Advantages
1. Managed service
2. Flexible deployment options
3. Integration with AWS Ecosystem
4. High scalability
5. Cost efficiency
6. Improved developer productivity 
7. Security
##### Disadvantages
1. Cluster management overhead
2. Limited cross-cloud support(again, vendor lock in)
3. Region limitations
4. Cost complexity

#### Amazon S3 Glacier
S3 Glacier is low-cost cloud storage service designed by AWS for archiving and long-term data backup. Designed to provide a cost-effective service for storing large amounts of archival data that doesn't require immediate access. Part of S3 family.
Can set policy to automatically move data from S3 Standard to Glacier after a set retention period.![[s3_glacier.png]]
##### Advantages
1. Low cost storage
2. High durability 
3. Flexible retrieval options
4. Seamless integration with S3
5. Scalable
6. Long term data archiving
7. Security
8. Compliance(suitable for healthcare, financial services and government use)
##### Disadvantages
1. Retrieval latency, can take hours to even a day
2. Retrieval costs add up
3. Cold data accessibility
4. Limited features(no event notifs like S3)
5. Low data availability
6. Data restoration process high
7. No support for object modification(once uploaded, can't edit object, can only delete)

#### Amazon Kinesis
Used  to analyze streaming data and process it for further use at large amounts of scales. Fully managed by Amazon.
- Kinesis data streams(for real time streaming of data)
- Kinesis data firehose(for loading data into AWS services)
- Kinesis data analytics(for analyzing the streaming data)
- Kinesis video streams(for streaming video data)
![[Kinesis.png]]
#### Amazon Redshift
Large scale data warehousing. Fully managed by Amazon. Can use SQL-based tools to analyze large datasets.
##### Key features
1. Massively Parallel Processing
2. Columnar Storage
3. Scalable
4. SQL interface
5. Integration with AWS ecosystem
6. Automated backups
7. ML integration
![[redshift.png]]

#### Amazon EMR
Elastic Map Reduce simplifies running big data frameworks like Hadoop, Spark on AWS. Designed to process large amount of data efficiently across a scalable cluster of virtual servers.![[emr.png]]

#### AWS Disaster Recovery and Backup
AWS Disaster Recovery and Backup solutions provide organizations with secure, scalable, and cost-
effective ways to back up and restore data, as well as to ensure business continuity in case of disasters.
These services are designed to minimize data loss and reduce downtime by leveraging the AWS global
infrastructure and automation capabilities.![[disaster recovery.png]]
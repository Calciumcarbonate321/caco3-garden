#### AWS Management Console
Used to manage stuff on AWS. Users can login using AWS account or AWS SSO. Levels of access granted using IAM or Organization.
Can access all services using this. Does resource monitoring. Can vie real time costs and view usage reports and stuff. Create and manage IAM users and roles to control access to AWS resources.
##### Key features
1. User friendly web UI
2. Centralized access to all AWS services
3. Resources Management
4. Dashboard and overview
5. IAM integration
6. Monitoring and analytics using cloud watch
7. Billing and cost management
##### Advantages
1. Ease of use
2. Centralized access
3. Real-time monitoring and insights
4. Const management tools
5. Security and access control
6. Flexible resource provisioning
7. Cross-account management
#### Disadvantages
1. Complex for large deployments
2. Limited automation
3. Not ideal for all use cases. AWS CLI offers more control.
##### Best practices
1. Setup IAM roles and policies
2. Leverage AWS CloudFormation to automate resource provisioning and deployments.
3. Use tagging for resource management(apply tags to resources for better organisation)
4. Monitor usage and cost regularly
5. Implement cost optimization
6. Automate with CLI or SDK for large scale ops 

#### AWS CLI
Open source tool that allows users to interact with AWS services via command line.
##### Key features
1. Unified interface
2. Cross-platform
3. Batch processing 
4. Secure authentication
5. Configurable Profiles
6. JSON, YAML and Text output formats
7. Scripting and automation is easy using this
8. Integrates with AWS SDK
9. Supports CloudFormation
10. Supports AWS Systems Manager(used to run scripts across multiple ec2 instances)
#### Advantages
1. Speed and efficiency
2. Automation
3. Flexibility
4. Cost management
5. Easy integration
6. Lightweight
7. Consistent across all AWS services
##### Disadvantages
1. Error handling is tough as CLI gives limited feedback
2. Limited visualization
3. Not ideal for large scale ops
4. Security less than GUI
5. Lack of advanced error recovery
6. Requires maintenance

#### AWS SDK
Software Development Kits are set of libraries provided by AWS that allow developers to interact with AWS services using their preferred programming language.
##### Key features
1. Simplified API calls because of high level abstraction
2. Credentials management is simplified
3. Quality error handling and retries on failure
4. Async and sync calls
5. Server specific features(like uploading file to S3)
6. Concurrency
##### Advantages
1. Ease of use
2. Cross language support
3. Automatic retry logic
4. Security
5. Scalability 
6. Active community and updates

#### AWS CloudFormation
AWS CloudFormation is a service that allows you to model and provision AWS infra using infra as code (IaC). Can use this to define and manage AWS resources.
![[CloudFormation.png]]
##### Key features
1. IaC, can define in template file in JSON or YAML format which can be used to create/update resources.
2. Declarative syntax can be used to describe what you want.
3. Stack management: A CloudFormation stack is a collection of AWS resources that you can manage as a single unit.
4. Before deploying, can create change set to preview the changes that will occur.
5. Auto rollback in case of error when CRUD operation of a stack.
6. Drift detection happens to ensure the stack resources don't change from template.
##### Advantages
1. Automation and consistency
2. Version control of templates
3. Scalability
4. Multi region and multi account
5. Security
6. Improved cost management
7. Reusability
8. Integration with CI/CD pipelines
##### Disadvantages
1. Limited error feedback
2. Slow stack updates
3. Third party integrations are tough.

#### AWS Trusted Advisor
AWS Trusted Advisor is an online resource to help AWS users reduce cost, increase
performance, improve security, and monitor service limits across their AWS infrastructure
##### Key features
1. Cost optimization
	- Idle resources
	- Reserved instances underutilization 
	- S3 storage optimization(tells to move to cheaper classes)
2. Security
	- IAM best practices
	- S3 bucket permissions
	- Security group configuration
3. Fault Tolerance
	- Elastic Load balancing, tells when to use this
	- Recommends auto scaling 
	- Encourages use of Multi AZ
4. Performance
    - Optimization of EC2 instances, tells which class to use based on usage.
    - Guides how to use CloudFront caching
5. Service Limits
	 - AWS Resource limits, monitors the service limits
	 - Sends notifs when limits are approaching

#### AWS CloudWatch
Monitoring and observability service provided by AWS to collect, monitor and analyze data from AWS resources.
##### Key features
1. Metrics collection and monitoring 
2. CloudWatch logs
3. CloudWatch alarms
4. CloudWatch Events enables you to setup rules that react to certain system events in AWS services.
5. CloudWatch synthetics, used to run synthetic tests(automated) on applications.
6. CloudWatch service lens, provides end-to-end visibility of performance of applications, correlating logs and traces from AWS services.
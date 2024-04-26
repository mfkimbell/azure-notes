# azure-notes


# Azure

(compute)

## Azure VM-virtual machiens (aws EC2)
* instance types = VM series
* elastic block stoarge = azure disk: persistent storage volumes for your VM
* Script, aws user-data = azure custom-data: scripts that are run on the startup of your VM
* Secuirty groups, AWS Security group = Azure NIC Network Security Group
* Autoscaling, Azure VM Scale Sets = AWS Autoscaling: increase number of resources as needed


## Availability Set (AWS auto scaling group)
* **Update Group** area of VMs that will update during matienence, only one domain udpates at a time,** uazusually 3-5**
* **Fault domain** grouping in data centers that share power and network,** max of 20**

## Azure VNet (aws VPC)
* Secure your network using, Azure NSGs and ASGs = AWS NACLs and Security Groups

## Azure DNS (AWS Route 53)

## Azure Container Instances (AWS ECS & Fargate)
* run containerized applications without managing servers (serverless)

## Azure Container Registry (AWS ECR)

## Azure Kubernetes Service (AWS EKS)

## Azure Blob (AWS S3)
* Blob storage resources: Storage Account, Container, and Blob
* Replication, Azure Object Replication = AWS Cross Region Replication
* Static Website Cache, Azure CDN = AWS Cloudfront: cache content from a static website
  
## Azure SSE (aws KMS)
* Does data encryption
  
## Azure Key Vault (AWS KMS)
* Stores keys, secrets, and certificaitons

## Azure Webjobs (AWS LAMBDA/STEP + EVENT BRIDGE)
* background jobs/tasks that run for an application
* Azure WebJobs is a feature of Azure App Service that enables you to run a program or script in the same context as a web app, API app, or mobile app. WebJobs are often used to run background tasks as part of an application. They can be triggered by a schedule (timer-based), by an event (such as a queue message being added), or run continuously.
  
## Azure Files (AWS EFS)

## Azure Databox (AWS Snow Family/snowball)
* transfer petabytes and exabytes of data to the cloud.

## Azure Function (aws lambda)
* like lamda functions
* serverless
* compute on demand
* scalable
* support for multiple languages

## Azure SQL (AWS RDS)
* fully scalable relational databse in the cloud
* Azure SQL Database serverless (aws Aurora Serverless): just a serverless database
* High availability, Azure zone redundant configuration (aws Multi-Zone Deployment)
* Secondary DB, Azure active geo-replication = AWS Read Replicas

## Azure App Service (elastic beanstalk)

## Azure Application Gateway (AWS Application Load Balancer)

## CosmosDB (aws dynamodb)

## Azure AD - Active Directory (aws IAM)

## Azure Frontdoor (aws cloudfront)

## Azure Monitor (aws cloudwatch)
Azure Monitor collects, analyzes, and acts on telemetry data from your Azure and on-premises environments. It helps to understand how applications are performing and proactively identifies issues affecting them and the resources they depend on.


<img width="1272" alt="Screenshot 2024-04-10 at 12 25 44 PM" src="https://github.com/mfkimbell/cloud-notes/assets/107063397/31f97365-4f9f-444a-b9ff-4d62d24696ef">

## Azure Event Grid (aws eventbridge)

## Azure Event Hub (aws kinesis)

## Azure Service Bus (aws Event Bridge service bus or SQS+SNS)

## Azure Activity Log
Azure Activity Log is a service that provides an audit trail of all write operations (PUT, POST, DELETE) made to resources in your Azure account. It records when resources are modified or deleted, who made changes, and what operations were performed. While useful for security and audit purposes, the Azure Activity Log does not provide information about the performance of resources, only about operations performed on them.

## Azure Traffic Analytics
Azure Traffic Analytics is a solution that provides visibility into network traffic by analyzing the NSG flow logs (Network Security Group Flow Logs). It allows you to understand which users and applications are consuming bandwidth, helps identify traffic flow patterns, and detects network anomalies. However, this tool is more focused on network-level insights and traffic flow rather than overall performance metrics related to CPU, memory, or disk, which are typically involved in general performance issues.

## Azure Log Analytics (AWS Cloudwatch Logs)

## Azure Notification Hub (aws SNS)

## Azure Storage Queue (aws SQS)


## Azure Advisor
* a personalized cloud consultancy service provided by Microsoft Azure. It analyzes your deployed Azure resources and offers recommendations to optimize your Azure environment. The goal of Azure Advisor is to help you improve the cost-effectiveness, performance, reliability, and security of your applications and services running on Azure

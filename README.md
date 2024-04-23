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

## CosmosDB (aws dynamodb)

## Azure AD - Active Directory (aws IAM)

## Azure Frontdoor (aws cloudfront)

## Azure Monitor (aws cloudwatch)


<img width="1272" alt="Screenshot 2024-04-10 at 12 25 44 PM" src="https://github.com/mfkimbell/cloud-notes/assets/107063397/31f97365-4f9f-444a-b9ff-4d62d24696ef">

## Azure Event Grid (aws eventbridge)

## Azure Event Hub (aws kinesis)

## Azure Service Bus (aws Event Bridge service bus or SQS+SNS)


## Azure Notification Hub (aws SNS)

## Azure Storage Queue (aws SQS)

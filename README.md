# azure-notes
![scope-levels](https://github.com/mfkimbell/azure-notes/assets/107063397/6b5c8c07-632d-4c25-b7c8-3c75a8452dad)

Managed Identity
Managed Identity is an Azure feature that allows services to authenticate to other Azure services without storing credentials in the code. Azure manages the identity lifecycle, including credential rotation.

Types of Managed Identities:

System-Assigned Managed Identity: Tied to a specific Azure resource (e.g., a virtual machine, Azure Function, or Azure App Service). When the resource is deleted, the identity is also deleted.
User-Assigned Managed Identity: Independent of any specific resource and can be shared across multiple resources. The identity's lifecycle is managed separately.
Key Features:

Credential Management: Azure handles the management, rotation, and protection of credentials.
Integration with Azure AD: Managed identities are first-class entities in Azure AD and can be assigned roles and permissions.
Seamless Authentication: Services can authenticate to Azure resources using managed identities without needing to manage credentials.
Pros:

Security: Eliminates the need to store credentials in code or configuration files.
Simplicity: Simplifies authentication by automating identity and credential management.
Scalability: Easily scalable as the number of resources and services grows.
Cons:

Scope: Limited to Azure resources that support managed identities.
Flexibility: Less control over the identity compared to manually managed credentials.
Role-Based Access Control (RBAC)
RBAC is an authorization system that provides fine-grained access management to Azure resources. It allows you to assign roles to users, groups, and managed identities.

Key Features:

Role Assignments: Permissions are grouped into roles (e.g., Reader, Contributor, Owner) and assigned to users, groups, or managed identities.
Scope Levels: Roles can be assigned at different levels, such as subscription, resource group, or individual resource.
Custom Roles: Ability to create custom roles to tailor permissions to specific needs.
Pros:

Granular Control: Fine-grained access management enables precise control over who can do what with Azure resources.
Scalability: Easily scalable across large environments with many users and resources.
Auditability: Provides detailed logs and reports for auditing and compliance purposes.
Cons:

Complexity: Can become complex to manage in very large environments with many roles and role assignments.
Initial Setup: Requires thoughtful planning and setup to align roles with organizational needs and security policies.
Managed Identity vs. RBAC: How They Work Together
Managed Identity for Authentication: Managed identities are used for secure authentication to Azure services without storing credentials.
RBAC for Authorization: RBAC is used to authorize access to resources. Managed identities are assigned roles through RBAC to grant them the necessary permissions.
Example Scenario
Scenario: An Azure Function needs to access an Azure Key Vault to retrieve secrets.
Managed Identity: Enable a system-assigned managed identity for the Azure Function.
RBAC: Assign the managed identity the "Key Vault Reader" role in the Azure Key Vault. This role assignment allows the Azure Function to access the secrets it needs.
Conclusion
Managed identities simplify the authentication process by eliminating the need for credential management, while RBAC provides the necessary authorization framework to control access to Azure resources. Together, they provide a robust security model for managing access to Azure services.

## Status Codes to know for AZ-204 exam
* 200 success
* 400 bad request
* 401 unauthorized
* 403 forbidden
<img width="795" alt="Screenshot 2024-05-02 at 6 36 36 PM" src="https://github.com/mfkimbell/azure-notes/assets/107063397/bb0863c3-95c9-4d51-840d-e6adb1f87158">

* 404 not found

### 409 Conflict Error
* The 409 Conflict error is an HTTPS status code that indicates a conflict between a client's request and the current state of a resource. This error usually occurs in response to a PUT request. For example, a 409 error may occur when uploading a file that is older than an existing file on the server.

### 500 Internal Server Error
The HTTP status code 500, also known as the Internal Server Error, is a generic error response that indicates the server encountered an unexpected condition that prevented it from fulfilling the request. This error is usually returned by the server when no other error code is suitable. 

SiteGround
What is “HTTP 500 Internal Server Error” and How to Fix It? - SiteGround KB

Apigee Docs

  
### 502 Bad Gateway
* The HTTP 502 status code indicates that one server on the internet received an invalid response from another server. It is a gateway or proxy server error, and it is usually indicative of issues between servers on the backend rather than with the client directly. Key aspects include:
* Gateway/Proxy: It occurs when a gateway or proxy server, which is acting as an intermediary for the client, receives an invalid response from the upstream server.
* Configuration Issues: This error can often result from network misconfigurations or servers failing to respond properly.
* Potential Causes: Causes might include servers being down, network errors, or faulty programming in the backend that the gateway is unable to handle.

### 503 Service Unavailable:
* The HTTP 503 status code means that the server is currently unable to handle the request because it is temporarily overloaded or down for maintenance. There is no inherent problem with the request itself, but the server is simply unable to process it at this time. Here are some key points about the HTTP 503 error:
* Temporary: This error suggests a temporary condition which will be alleviated after some delay. It is often used when servers undergo maintenance or are temporarily overloaded.
* Retry-After Header: Servers can optionally include a Retry-After header indicating how long to wait before making a new request.
* Load Balancers: In a scenario with load balancers, this error might indicate that all servers are too busy or down.

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
* **Fault domain** grouping in data centers that share power and network, **max of 20**

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

## Azure App Service (AWS ElasticBeanstalk or AWS Amplify )

## Azure Application Gateway (AWS Application Load Balancer)

## CosmosDB (aws dynamodb)

## Azure AD - Active Directory (aws IAM)

## Azure Frontdoor (aws cloudfront)

## Azure Monitor (aws cloudwatch)
Azure Monitor collects, analyzes, and acts on telemetry data from your Azure and on-premises environments. It helps to understand how applications are performing and proactively identifies issues affecting them and the resources they depend on.

## Azure Resource Manager ARM (AWS CloudFormation)
* AWS CloudFormation, Terraform, and Azure Resource Manager (ARM) are infrastructure as code (IaC) tools 

## Azure App Service (AWS Elastic Beanstalk)
* contains Azure Web Apps, API Management, Azure Functions, Azure Logic Apps

## Azure App Configuration (AWS Systems Manager)



<img width="1272" alt="Screenshot 2024-04-10 at 12 25 44 PM" src="https://github.com/mfkimbell/cloud-notes/assets/107063397/31f97365-4f9f-444a-b9ff-4d62d24696ef">

## Azure Event Grid (aws eventbridge)

## Azure Event Hub (aws kinesis)

## Azure Service Bus (aws Event Bridge service bus or SQS+SNS)


Event Grid is fire and forget. System A publishes to Event Grid where the event is consumed by System B. System A doesn't care or know that System B consumed or did anything with that event. Think of push notifications. A system like Reddit publishes an event when someone comments. Your app subscribes to that event stream and shows you a notification when it receives something. The sending system doesn't care or need to know about that.

Service Bus is fire but don't forget. System A publishes to Service Bus where the message is consumed by System B. System A may have some expectation or requirement to know that message has been consumed. Messages are queued until they can be received, and can be ordered (first in, first out). Think of a distributed finance system. Someone makes a payment from one account to another. That message is sent to a queue where it is picked up by another system for processing. The sending system needs to know that message was received otherwise it may try to resend and then incorrectly re-debit the senders account. Ordering of messages is also important here.

Even Hub is fire, fire, fire. Systems A, B, C and all their friends stream events to Event Hub. System X consumes batches of events. System Y consumes telemetry data about the events. Think of IoT devices. A building with 10,000 sensors sending events on changes in state (temperature, etc) gets fed into a central store. One system might take in batches of events (temperature data) to generate a heatmap of the building. Another system might analyse the telemetry stream to detect anomalies.

## Azure Activity Log (AWS Cloudtrail)
* all about changes to resources
Azure Activity Log is a service that provides an audit trail of all write operations (PUT, POST, DELETE) made to resources in your Azure account. It records when resources are modified or deleted, who made changes, and what operations were performed. While useful for security and audit purposes, the Azure Activity Log does not provide information about the performance of resources, only about operations performed on them.

## Azure Search

## Azure Logic Apps (AWS Step Functions)

## Azure Audit Log (AWS Cloudtrail)
* contains the history of sign-in activity and audit trail of changes made within a particular tenant
  
## Azure Traffic Analytics (AWS Elastic loadbalancer, not super clear why)
Azure Traffic Analytics is a solution that provides visibility into network traffic by analyzing the NSG flow logs (Network Security Group Flow Logs). It allows you to understand which users and applications are consuming bandwidth, helps identify traffic flow patterns, and detects network anomalies. However, this tool is more focused on network-level insights and traffic flow rather than overall performance metrics related to CPU, memory, or disk, which are typically involved in general performance issues.

## Azure Log Analytics (AWS Cloudwatch Logs)
Azure Log Analytics is a tool within the Azure Monitor suite. It collects telemetry and other data from a variety of sources and provides a query language for complex analytics, insights, and the ability to act on the collected data.

Here are the core features of Azure Log Analytics:

Data Collection: Gathers data from various sources like Azure resources, on-premises environments, and other cloud platforms.
Advanced Queries: Uses Kusto Query Language (KQL) to analyze collected data for patterns, anomalies, and trends.
Alerting: Allows you to create alerts based on metrics or query results.
Integration: Works closely with other Azure services, including Azure Automation and Azure Security Center, for a comprehensive monitoring solution.

## Azure Notification Hub (aws SNS)

## Azure Storage Queue (aws SQS)


## Azure Advisor
* a personalized cloud consultancy service provided by Microsoft Azure. It analyzes your deployed Azure resources and offers recommendations to optimize your Azure environment. The goal of Azure Advisor is to help you improve the cost-effectiveness, performance, reliability, and security of your applications and services running on Azure

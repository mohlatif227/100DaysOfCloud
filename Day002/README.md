First VM Provisioning from Azure Portal

- When you provision virtual machine(vm/instance) on Azure first time, you'll have to create below
	- Resource Group
	- Virtual Network(VNet) similar to VPC
	- Subnet
	- Assign Public IP (if you want to access over internet)
	- Disk Allocation
	- Security Group to allow access(SSH/HTTP/HTTPS/ICMP for ping)
		- Region - Select nearest geolocation as per your requirement
		- Availability  Zone
Create First Website using Azure CLI

	- First you have to login to your [Azure Portal](https://portal.azure.com) and then click on  cloud shell as below

	- Please follow this link for more details  about [Cloud Shhell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview)
	- Now clone below git repository in order to provision static website using Azure CLI
```
git clone https://github.com/Azure-Samples/html-docs-hello-world.git
cd html-docs-hello-world
az webapp up --location westus --name [your_name] --html
http://[your_name].azurewebsites.net
az group delete --name [resource_group_name]
```


Service Categories

- Migration
	- Azure Migrate
	- Azure Active Directory
- DevOps
	- Azure DevOps
	- Azure Pipelines (Continuous Integration and Deployment).
	- Azure DevTest Labs
	- Azure CDN (Content Delivery Network)
- IOT
	- Azure IoT Central
	- Azure IoT Hub
	- Azure Sphere - Make your IoT device secure
- Analytics
	- Azure HDInsight
	- Azure Databrikcks 
	- Azure Synapse Analytics
-   AI
	- Azure Cognitive Services
		- Decision
		- Language
		- Speech
		- Vision
		- WebSearch
	- Azure Bot Service
	- Azure Machine Learning Studio
	- Azure Machine Learning Services
- Integration
	- Azure Logic Apps
	- Azure Event Grid
Designing Solutions 

- E-Commerce Front End on Azure


-  Azure Pricing calculator.

Managing Services

- Azure Monitor
	- Application Insights
	- Logs Analytics
	- Service Health
- Azure Backup
- Azure Advisor
	- Cost analysis and recommendation 
	- Security analysis and recommendation
- Azure Policy
- Advance Threat Protection
- ARM Template
- Azure Blueprints

Summary




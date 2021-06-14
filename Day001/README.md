# Day01

## - What is Cloud Computing
	- Cloud computing is remote virtual pools of on-demand shared resources offering compute, storage, database and networks which can be rapidly deployed at any scaled.
## - What is Virtualization
	- A piece of software to provision multiple virtual vm(OS) on single physical host using hypervisor.
	- A hypervisor is logical entity between physical host and multiple VMs.
## - Cloud Deployment Models
	- Public Cloud
	- Private Cloud
	- Hybrid Cloud
## - Key Cloud Concepts
	- On demand resourcing - provision resources any time
	- Scalability  - ability to rapidly scale your infra as per need up and down; in and out.
		- Vertical Scaling: Scaling up and down alters the power and performance of an instance, perhaps using one with greater CPU and more Memory power.
		- Horizontal Scaling: Scaling 'in and out' adds or removes the numbers of instances you're using to your fleet of compute resources.
	- Economy of Scale
		- Low resource costs compared to traditional hosting
	- Flexibility and Elasticity
		- The amount of resources you require
		- How much and how long you want it
		- What scale
	- Growth
	- Utility Base Metering
		- Pay as you go
	- Share Infrastructure
	- Highly Available.
	- Security
## - Cloud Services Models
	- Software as a Service(SaaS)
	- Platform as a Service(PaaS)
	- Infra as as a Service(IaaS)
## - Common Use Cases of Cloud Computing.
	- Migration of production Services
	- Traffic bursting
	- Backup/DR
	- Web Hosting
	- Test/Dev environment provision quickly
	- Proof of Concept
	- Big Data and Data manipulation

## Azure Services

###	- Compute
		- Azure Virtual Machines
		- Azure App service
		- Azure Container Instances
		- Azure Kubernetes Service
		- Azure Functions 
###	- Storage
		- Azure Blob Storage - For unstructured data
			- Hot: Frequently accessed
			- Cool: Infrequently accessed
			- Archive: Rarely accessed.
		- Hierarchical File Storage
			- Azure File Storage(typically SMB can be mount on WIndows Servers)
			- Azure Data Lake Storage - Gen2 - For data analytics application(Hadoop compatible)
		- Ralational Databases
			- Azure Sql Database
			- Open Source
				- For Mysql
				- For MariaDB
				- For Postgres 
		- Azure Synapse Analytics
			- For Data warehouse applications.
		- No Sql Database
			- Azure Cosmos DB
			- Azure Cache for Redis
### - Networking
		- VNet(Virtual Network)
		- Subnets
		- VNet Peering ( to connect VNet1 vm to Vnet2 vm)
		- Azure VPN: send encrypted traffic over the public internet
		- Azure ExpressRoute: Dedicated connection, High speed and reliable; much expensive compare to Azure VPN
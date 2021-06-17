# Lab1 

## Understanding Core Azure Storage Products

- Today again we're going through hands-on lab section, let's do our hands dirty with lab work.
- I'm following this lab

### Introduction

Blob data stands for Binary Large OBject data. Blob data and can represent a wide variety of types of data you normally store on your computer including images, videos, and documents. In Azure you can store blobs inside of storage accounts. Storage accounts are containers capable of storing different categories of data including:
- Blobs
- Files
- Tables
- Queues
You should usually choose blob storage when dealing with unstructured data. Depending on your blob storage needs you can choose between the following types of blobs in Azure blob storage:
- Block blobs are divided into blocks of up to 100MB in size. Blobs of up to 4.75TB (terabytes) can be stored using block blobs in Azure Storage. Using multiple blocks to represent the blob allows for more efficient handling of large blobs. Usually, the complexity of managing individual blocks is handled for you so you can simply deal with the entire blob rather than individual blocks.
- Append blobs are optimized for appending new data at the end of the blob. This is particularly useful for storing log data where new lines are added at the end and the data never needs to be modified after it is written.
- Page blobs are optimized for random read/write operations. The name comes from the practice of operating systems organizing memory into pages of relatively small sizes that can be easily managed. In Azure, page blobs are collections of individual pages of up to 4MB each. They are used for storing virtual machine disks in Azure.
- The Replication sets the durability and availability of the storage. The following options are available:
	- Locally-redundant storage (LRS) is the cheapest option and stores the data in a single data center. If that data center goes offline you will not be able to access the data.
	- Zone-redundant storage (ZRS) stores data across three data centers in a region. It can tolerate individual data center outages but not regional outages.
	- Geo-redundant storage (GRS) stores data across multiple data centers in two regions, a primary region and a secondary region. This option is more expensive but can tolerate entire regional outages. There is also read-access geo-redundant storage (RA-GRS) which allows you to read from the secondary region compared to GRS which only allows you to access the secondary in the case of a Microsoft-initiated region failover to the secondary.
- Finally, the Account kind describes if the storage account is general-purpose or specialized. General-purpose accounts allow storage of blobs, tables, files, and queues whereas specialized kinds only allow one type such as only blob storage. There are different pricing models for each account kind so a specialized kind may reduce your costs. StorageV2 is the recommended default.


### Disk Storage in Azure


Azure virtual machines (VMs) use Azure disks as their attached disk storage. Azure disks are built-on top of page blobs which are the type of blobs optimized for random access. When you create Azure disks you can choose to manage the storage account yourself or to use managed disks where Azure manages the storage account for you. Managed disks are the preferred option. Within managed disks you can choose between:
- Ultra SSDs which provide the best throughput and I/O operations per second (IOPS) performance characteristics but at the highest prices. Consider Ultra SSDs for mission-critical I/O intense applications such as running databases.
- Premium SSDs are the next best performing and are well-suited to production workloads with all but the highest performance I/O requirements that may benefit from using Ultra SSDs.
- Standard SSDs are the least expensive SSD option and are suitable for production workloads with low I/O performance requirements such as web servers and lightly used applications.
- Standard HDDs use spinning disk technology and are therefore the least expensive option but also provide the lowest performance. Use them for backups and infrequently accessed applications.


## Lab2


## Understanding Core Azure Networking Products


### Azure Virtual Networks



Introduction

Azure Virtual Networks (VNets) is the basic building block for logically isolating resources using networks in Azure. VNets enable many different Azure services, such as load balancers, virtual machines and more, to communicate securely with one another. In combination with other Azure services like network security groups they also provide layers of protection from different segments of the Internet to your Azure resources. In this Lab Step, you will navigate to a VNet in the Azure Portal and learn about Azure Virtual Networks.


### Azure Load Balancers



Introduction

Azure Load Balancer allows you to direct incoming traffic to multiple resources such as virtual machines. Load balancing is a strategy often used to direct incoming internet traffic to more than one virtual machine serving the same web application, among many other uses. This allows companies to deploy highly scalable, high-availability solutions, since they can scale the number of targets behind a load balancer up and down as much as needed and still direct internet traffic to a single load balancer.


### Azure Application Gateways



Introduction

Azure Application Gateways are an alternate load balancing solution provided by Azure, which differs from the load balancers covered earlier in this Lab in several meaningful ways to provide more customized support for both public and private web applications. While the load balancers covered earlier route traffic purely based on IP address and port information, application gateways can take this a step further and route based on things like URIs. This means that an application gateway can route traffic sent to "some-ip-address/admin" differently than, say, traffic sent to "the-same-ip-address/general" This allows for much more detailed control of your routing.
Application Gateways also have the ability to accept traffic for more than one site using multiple site hosting. Application Gateway Multiple Site Hosting works by sending traffic from examplesite1.com to backend pool 1, traffic from examplesite2.com to backend pool2, and so on. This allows for the management of up to 100 sites using a single Application gateway.
Application Gateways offer many other very useful features such as SSL termination, connection draining and request redirection. While this Lab Step will cover the fundamentals of Azure Application Gateways, it's highly worth it to learn more about application gateways in depth.


### Azure VPN Gateways



Introduction

Azure VPN Gateways are a type of Azure Virtual network Gateway which allows you to create secure connections between your on-premises network and an Azure Virtual Network (VNet). Azure uses leading security practices to protect data traveling between your on-premises network and your Azure network as if it were a single virtual private network (VPN). Among the benefits of this is the ability to use a hybrid infrastructure consisting of cloud and on-premises resources, with more security than you would get by simply handling your traffic over the public internet.


### Azure Content Delivery Network



Introduction

Azure Content Delivery Networks (CDN) offers a way to deliver data efficiently on a global scale. CDNs typically cache content on more than one server in order to guarantee that when a user requests data, the data is on a server close enough to them to minimalize the amount of time the user has to wait for that data. Azure installs CDN data on servers in point-of-presence (POP) locations all around the world to efficiently deliver data, regardless of the user's location. Azure often uses something called a cache, which is a set of previously-stored data, to serve to users, so that new information doesn't have to be requested and received every time. This greatly reduces the latency, or wait time, the end-user experiences.
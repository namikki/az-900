# Azure Fundamentals AZ-900 Real Exam Questions

### Question 1

Your company has datacenteres in Los Angeles and New York. The company has Microsoft Azure subscription. You are configuring the two datacenters as geo-clustered sites for resiliency. You need to recommend an Azure storage redundancy option. You have the following data storage requeriments:
- Data must be stored on multiple nodes.
- Data must be stored on nodes in separate geographic locations.
- Data can be read from the secondary location as well from the primary location.

Which of the following Azure storage redundancy options should you recommend?

a) Zone-redundant storage

b) Geo-redundant storage

c) Locally redundant storage

**d) Read-only geo-redundant storage**

**Note**:
- **Read-only geo-redundant storage (RA-GRS)** builds on GRS by allowing read access to the data in the secondary location as well as the primary. This option meets the requirement for data to be stored on multiple nodes in separate geographic locations and allows data to be read from both the primary and secondary locations.

**The other options:**
- **Geo-redundant storage (GRS)** provides redundancy by replicating data to a secondary geographic location, but it does not allow reading from secondary location unless the primary location fails.
- **Zone-redundant storage (ZRS)** stores data across multiple availability zones within the same region.
- **Locally redundant storage (LRS)** stores multiple copies of data within a single region.

---

### Question 2

Your developers have created 10 web applications that must be host on Azure. You need to determine which Azure web tier plan to host the web apps.

The web tier plan must meet the following requirements:
- The web apps will use custom domains.
- The web apps each require 10 GB of storage.
- The web apps must each run in dedicated compute instances.
- Load balancing between instances must be included.
- Costs must be minimized.

Which web tier plan should you use?

a) Basic

b) Free

c) Shared

**d) Standard**

**Note:** 
- **Custom domains**: both the Basic and Standard tiers support custom domains, but the Free and Shared tiers do not.
- **10 GB of storage:** the Basica tier offers 10 GB of storage, while the Standard tier offers 50 GB. The Free and Shared tiers offer less storage.
- **Dedicated compute instances:** The Standard tier provides dedicated compute instances, which means that each web app will run in its own isolated environment. The Basic tier also offers dedicated compute instances. The Free and Shared tiers do noto offer dedicated compute instances.
- **Load balancing:** The Standard tier includes built-in load balancing across multiples instances, which is not available in the Basic, Free, or Shared tiers.
- **Cost minimization:** The Basic tier might be cheaper than the Standard tier, but it does not meet the load balancing requeriment.

### Question 3

You are required to deploy an Artificial Intelligence (AI) solution in Azure. You want to make sure that you are able to build, test, and deploy predictive analytics for the solution.

Solution: You should make use of Azure Cosmos DB.

Does the solution meet the Goal.

a) Yes

**b) No**

**Note:**
- Azure Cosmos DB is a globally distributed, multi-model database service designed for high availability and low latency. It is used for managing data at scale and is ideal for scenarios requiring distributed data, such as IoT, web apps, and real-time analytics. However, **it is not** specifically designed for building, testing, and deploying predictive analytics or AI models.
- To build, test, and deploy predictive analytics for an AI solution, you should consider using **Azure Machine Learning** ou **Azure Synapse Analytics**. These services are specifically tailored for AI and Machine Learning workloads, providing the tools and frameworks necessary for developing predictive models.

### Question 4

Your company's infrastructure includes a number of business units that each need a large number of various Azure resources for everyday operation. The resources required by each business unit are identical. You are required to sanction a strategy to create Azure resources automatically.

Solution: You recommend that the Azure Resource Manager templates be included in the strategy. Does the solution meet the goal?

**a) Yes**

b) No

**Note:**
- **Azure Resource Manager (ARM)** templates are JSON files that define the infrastructure and configuration of your Azure resources. They allow you to automate the deployment of Azure resources in a consistent and repeatable manner. By using ARM templates, you can define a blueprint for the resources needed by each business unit and deploy them automatically, ensuring that all required resources are created with the same configurations every time.

### Question 5

Your company has virtual machines (VMs) hosted in Microsoft Azure. The VMs are located in a single Azure virtual network named VNet1. The company has users that work remotely. The remote workers require access to the VMs on VNet1. You need to provide access for the remote workers.

What should you do? Does the solution meet the goal?

a) Configure DirectAcess on a Windows Server 2012 server VM.

**b) Configure a Point-to-Site (P2S) VPN.**

c) Configure a VNet-to-VNet VPN.

d) Configure a Site-to-Site (S2S) VPN.

e) Configure a Multi-Site VPN.

**Note:**
- A **Point-to-Site (PSN) VPN** is a secure connection that allows individual remote users to connect to your Azure Virtual Nertwork (VNet1) from their remote locations. This is ideal for remote workes who need access to the virtual machines hosted by Azure.

- **Configure a Site-to-Site (S2S) VPN:** This is used to connect entire on-premises networks to an Azure Virtual Network, which is more suitable for connectiong corporate offices rather than individual remote workers.

- **Configure a VNet-to-VNet VPN:** This is used to connect two different Azure virtual networks.

- **Configure DirectAcess on a Windows Server 2012 server VM:** DirectAccess is an alternative to VPN that provides remote access, but it is more complex to set up and manage, and is not specifically designed for Azure environments.

- **Configure a Multi-Site VPN:** This is an extension of Site-to-Site VPN that connects multiple on-premises sites to a single Azure virtual network, but it is not intended for individual remote users.

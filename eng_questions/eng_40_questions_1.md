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

### Question 6

You have been informed by your superiors of the company's intentions to automate server deployment to Azure. There is, however, some concern that administrative credentials could be uncovered during this process. You required to make sure that during the deployment, the administrative credentials are encrypted using a suitable Azure solution.

Solution: You recommend the use of Azure Information Protection. Does the solution meet the goal?

**a) No**

b) Yes

**Note:**
- **Azure Information Protection** is a cloud-based solution that helps organizations classify, label, and protect documents and emails by applying labels. It is primarily used for protecting sensitive information within documents and emails, not specifically for encrypting administrative credentials during server deployment.
- For encrypting administrative credentials during deployment, **Azure Key Vault** would be the appropriate solution. **Azure Key Vault** is designed to securely store and manage sensitive information, such as secrets, encryption keys, and certificates. By using Key Vault, you can ensure that administrative credentials are encrypted and securely accessed during the deployment process.

### Question 7

Choose the correct answer.

When you are implementing a Software as a Service (SaaS) solution, you are responsible for:

**a) Configuring the SaaS solution.**

b) Defining scalability rules.

c) Installing the SaaS solution.

d) Configuring high availability.

**Note:**
- When you are implementing a Software as a Service (SaaS) solution, you are responsible for configuring the SaaS solution. Everything else is managed by the cloud provider. SaaS requires the least amount of management. The cloud provider is responsible for managing everything, and the end user just uses the software. Software as a service (SaaS) allows users to connect to and use cloud-based apps over the Internet. Common examples are email, calendaring and office tools (such as Microsoft Office 365).

### Question 8

You plan to migrate all the servers to Azure. You need to recommend a solution to ensure that some of the servers are available if a single Azure data center goes offline for an extended period. What should you include in the recommendation? 

a) Elasticity

**b) Fault tolerance**

c) Scalability

d) Low latency

**Note:**
- **Fault tolerance** is the ability of a system to continue operating properly in the event of a failure of some of its components. In the context of Azure, this means designing your deployment in such a way that if a single Azure data center goes offline, your services remain available.
- To achieve fault tolerance in Azure, you would typically use features like **Availability Zones** or **Geo-redundant storage**, which distribute your resources across multiple data centers or regions. This ensures that your servers and services remain operational even if one data center experiences an outage.

**The other options** are important cloud concepts, but they don't specifically address the need for availability in the event of a data center failure: 
- **Elasticity:** Refers to the ability of a system to automatically scale up or down based on demand.
- **Scalability:** Refers to the ability a system to handle increased load by adding resources.
- **Low latency:** Refers to minimizing the delay in processing or transmitting data, but it doesn't relate to availability in case of a data center failure.

### Question 9

What are two characteristics of public cloud?

**a) Metered pricing**

b) Dedicated hardware

**c) Self-service management**

d) Unsecured connections

e) Limited storage

**Note:**
- **Public Cloud** is a model of cloud computing where services are offered over the public internet and shared across organizations. Two key characteristics of the public cloud are:
- **Metered Pricing:** Public cloud services typically operate on a pay- as-you-go model. Users are charged based on their consumption of resources such as compute power, storage, and bandwidth. This metered pricing allows for cost flexibility and scalability.
- **Self-Service Management:** Public cloud platforms provide users with self-service portals or APIs, enabling them to manage, configure, and deploy resources on-demand without direct intervention from the service provider.

### Question 10

You have an on-premises network that contains 100 servers. You need to recommend a solution that provides additional resources to your users. The solution must minimize capital and operational expenditure costs. 

What should you include in the recommendation?

**a) A hybrid cloud**

b) A complete migration to the public cloud

c) An additional data center

d) A private cloud

**Note:**
- A **hybrid cloud** solution allows you to combine on-premises infrastructure with resources in the public cloud. This approach enables you to extend your existing resources without the need for significant capital expenditure on additional hardware or data centers. It also helps to minimize operational costs by leveraging the scalability and flexibility of the public cloud when additional resources are needed.

### Question 11

You have 1,000 virtual machines hosted on the Hyper-V hosts in a datacenter. You plan to migrate all the virtual machines to an Azure pay-as-you-go subscription. You need to identify which expenditure model to use for the planned Azure solution.

Which expenditure model should you identify?

a) Elastic

**b) Operational**

c) Capital

d) Scalable

**Note:**
- When you migrate virtual machines to an Azure pay-as-you-go subscription, you are shifting from a capital expenditure (CapEx) model, where you invest in physical infrastructure, to an operational expenditure (OpEx) model. In the OpEx model, you pay for the resources you use on a recurring basis (e.g., monthly or annually), which includes costs for compute, storage, and other services. This model is associated with the flexibility of paying for what you use rather than upfront capital investment. 

**The other options:**
- **Elastic:** Refers to the ability to scale resources up or down based on demand.
- **Scalable:** Refers to the capability of the system to handle growth.

### Question 12

Match the Azure services benefits to the correct descriptions.

- A cloud service that remains available after a failure occurs: **Fault tolerance**
- A cloud service that can be recovered after a failure occurs: **Disaster recovery**
- A cloud service that perfomns quickly when demand increases: **Dynamic Scalability**
- A cloud service that can be accessed quickly from the internet: **Low latency**

### Question 13

You plan to provision Infrastructure as a Service (IaaS) resources in Azure. Which resource is an example of IaaS?

a) an Azure web app

b) an Azure SQL database

c) an Azure logic app

**d) an Azure virtual machine**

**Note:**
- **Infrastructure as a Service (laaS)** provides virtualized computing resources over the cloud. With laas, you are responsible for managing the operating system, applications, and associated configurations, while the cloud provider manages the underlying hardware and networking resources.
- An Azure virtual machine is a classic example of laas. You get a virtualized server environment where you can install and manage your own operating system and applications. 

**The other options fall under different service models:**
- **An Azure web app:** This is an example of **Platform as a Service (PaaS)**, where the underlying infrastructure is managed by Azure, and you only need to manage the application and data.
- **An Azure logic app:** This is also an example of **Platform as a Service (PaaS)**, specifically used for building workflows that integrate apps and services.
- **An Azure SQL database:** This is another example of **Plataform as a Service (PaaS)**, where the database engine is fully managed by Azure, and you focus on the data and schema.

### Question 14

You can assign a _____ to every Azure resource.

a) Policy

b) Blueprint

c) Service endpoint

**d) Lock**

**Note:**
- You can assign a policy to any scope that you have access to, such as a management group, subscription, or resource group. However, you cannot assign a policy directly to an individual resource. You can assign a lock on every Azure resource that you have access to. You can apply a lock at different levels of scope: subscription, resource group, or individual resource.

### Question 15

What is the first stage in the Microsoft Cloud Adoption Framework for Azure?

**a) Define your strategy**

b) Ready your organization

c) Adopt the cloud

d) Make a plan

**Note:**

![microsoft_cloud_adoption_framework_for_azure](/.img/caf-baseline-journey.png)

### Question 16

Drag and drop the words to their places:

*Scalabity* *Agility* *Geo-Distribution*

- Applications can be deployed, tested and launched rapidly: *Agility*
- Applications and data can be deployed to multiple regions: *Geo-Distribution*
- Resources can be provisioned dynamically to meet changing demands: *Scalabity*

### Question 17

You plan to use Azure to host two apps named App1 e App2. The apps must meet the following requirements:
- You must be able to modify the code of App1.
- Administrative effort to manage the operating system of App1 must be minimized.
- App2 must run interactively with the operating system of the server.

Which type of cloud service should you use for each app?

- **App1:** PaaS
- **App2:** IaaS

### Question 18

Which term represents the ability to increase the computing capacity of a virtual machine by adding memomry or CPUs.

a) Agility

b) Elasticity

c) Horizontal scaling

**d) Vertical scaling**

### Question 19

What is a feature of an Azure Virtual Network?

**a) Isolation and segmentation**

b) Packet inspection

c) Resource cost analysis

d) Geo-redundancy

**Note:**
- **Isolation and segmentation:** Azure Virtual Network (VNet) allows you to create isolated and segmented networks within the cloud. This feature enables you to control traffic flow, enforce security policies, and create isolated environments for different applications or services.

**Why the other options are not correct:**
- **Resource cost analysis:** This is not a feature of an Azure Virtual Network. Resource cost analysis is related to billing and monitoring, which is handled by other Azure services like Azure Cost Management.
- **Packet inspection:** Packet inspection refers to the ability to inspect and filter network traffic, which is typically handled by Azure Firewall or Network Security Groups (NSGs), not by the Virtual Network itself.
- **Geo-redundancy:** Geo-redundancy refers to the replication of data across different geographic regions for disaster recovery and high availability. This is a feature of Azure Storage, not Azure Virtual Network.

### Question 20

Which of the following enables Azure resources to be deployed close to users?

a) Scalability

b) High availability

c) Elasticity

**d) Geo-distribution**

**Note:**
- **Geo-distribution** enables Azure resources to be deployed close to users by distributing resources across multiple geographic locations. This helps to redice latency, improve performance, and provide a better user experience by ensuring that the resources are located closer to the end-users.

### Question 21

Match the cloud computing benefits to the appropriate descriptions. Each benefit may be used once, more than once, or not at all.

**Benefits:** Disaster recovery, Geo-distribution, Scalability, High availability

- Increase the compute capacity of apps in the cloud: **Scalability**
- Provide a continuous user experience with no apparent downtime: **High availability**
- Ensure the users always have the best experience by deploying apps to all the regions where there are users: **Geo-distribution**

### Question 22

You need to identify the type of failure for which an Azure Availability Zone can be used to protect access to Azure services. What should you identify?

a) a storage failure

b) an Azure region failure

c) a physical server failure

**d) an Azure data center failure**

**Note:**
- **Azure Availability Zones** are specifically designed to protect against failures at the **data center level** within a single Azure region. Each Availability Zone is an independent data center with its own power, cooling, and networking. If one data center (Availability Zone) fails, services running in another Availability Zone in the same region will continue to function, ensuring high availability.

**Other Options:**
- **a physical server failure:** Azure Availability Sets are more relevant for protecting against physical server failures. An Availability Set ensures that VMs are distributed across multiple physical servers, racks, and storage units within a single data center. This approach minimizes the impact of a single server failure. However, Availability Zones offer more comprehensive protection, as they guard against entire data center failures rather than just server failures.
- **an Azure region failure**: **Geo-redundancy or Azure paired regions** are used to protect against **Azure region failures**. If an entire Azure region fails (e.g., due to a natural disaster), geo-redundancy ensures that services can failover to a secondary region. Availability Zones, however, are within a single region and do not protect against region-wide failures.
- **a storage failure**: **Azure Storage Redundancy** options, such as Locally Redundant Storage (LRS) or Geo-Redundant Storage (GRS), are designed to protect against **storage failures**. LRS replicates data within the same data center, while GRS replicates data across different regions. Availability Zones focus on broader infrastructure resilience rather than just storage.
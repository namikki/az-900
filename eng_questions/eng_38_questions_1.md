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

### Question 23

You plan to extend your company's network to Azure. The network contains a VPN appliance that uses an IP address of 131.107.200.1. You need to create an Azure resource thath defines the VPN appliance in Azure. Which Azure resource should you create?

a) NAT Gateways

b) Azure Data Box Gateway

c) Application Gateways

d) On-premises Data Gateways

e) Virtual Network Gateways

f) Web Application Firewall Policies

**g) Local Network Gateways**

h) Azure Stack Edge/Data Box Gateway

**Note:**
- A Local Network Gateway is an object in Azure that represents your on- premise VPN device. A Virtual Network Gateway is the VPN object at the Azure end of the VPN. A 'connection' is what connects the Local Network Gateway and the Virtual Network Gateway to bring up the VPN. The local network gateway typically refers to your on-premises location. You give the site a name by which Azure can refer to it, then specify the IP address of the on-premises VPN device to which you will create a connection. You also specify the IP address prefixes that will be routed through the VPN gateway to the VPN device. The address prefixes you specify are the prefixes located on your on-premises network. If your on- premises network changes or you need to change the public IP address for the VPN device, you can easily update the values later.

### Question 24

You plan to deploy several Azure virtual machines. You need to ensure that the services running on the virtual machines are available if a single data center fails. 

Solution: You deploy the virtual machines to a scale set. Does this meet the goal?

a) Yes

**b) No**

**Note:**
- Deploying virtual machines to a **scale set** alone does not ensure that the services running on them will remain available if a single data center fails. Scale sets help with load balancing and automatic scaling of virtual machines within the same data center or across multiple data centers, but they do not inherently provide high availability across data centers.
- **Correct approach:** To ensure that your services are available even if a single data center fails, you should deploy the virtual machines across **Availability Zones** within a region. Availability Zones are physically separate locations within an Azure region, and deploying VMs across them can protect against data center failures.

**Explanation of other options:**
- **Availability Zones** would ensure high availability across data centers within the same region, which is necessary to meet the goal. 
- **Scale sets** are beneficial for scaling out and managing a set of identical VMs but do not inherently provide redundancy across data centers.
- Deploying VMs to an **Availability Set** would protect against rack-level failures within a single data center, but not a full data center failure.

### Question 25

For each of the following statements, select Yes if the statements is true. Otherwise, select No.

- An Azure subscription can be associate with multiple Azure Active Directory (Azure AD) tenants: **No**
- You can change the Azure Active Directory (Azure AD) tenant to which an Azure subscription is associated: **Yes**
- When an Azure subscription expires, the associated Azure Active Directory (Azure AD) tenant is deleted automatically: **No**

**Note:**
- An Azure subscription can only be associated with a single Azure AD tenant at a time. However, you can have multiple subscriptions associated with the same Azure AD tenant.
- Azure allows you to transfer a subscription to another Azure AD tenant if needed. This is done through the Azure portal by reassigning the subscription to a different directory.
- The Azure AD tenant is not deleted when an Azure subscription expires. The Azure AD tenant exists independently of any subscription and can continue to be used or associated with other subscriptions.

### Question 26

Resource groups provide organizations with the ability to manage the compliance of Azure resources across multiple subscriptions. 

Instructions: If the statement is correct, select "No change is needed". If the statement is incorrect, select the answer choice that makes the statement correct.

**a) Management groups**

b) Azure policies

c) Azure App Service plans

d) No change is needed

**Note:**
- **Management groups** provide organizations with the ability to manage the compliance, policies, and access control for Azure resources across multiple subscriptions. Resource group on the other hand, are containers for resources within a single subscription, and are not designed to manage compliance across multiple subscriptions.
- **Resource groups** are used to organize and manage resources within a single subscription.
- **Azure policies** help enforce compliance at the resource level, but they are not specific to managing across multiple subscriptions.
- **Azure App Service** plans are used for managing the scaling and hosting of web apps, but they are unrelated to managing compliance across multiple subscriptions.

### Question 27

Your company plans to migrate to Azure. The company has several departments. All the Azure resources used by each department will be managed by a department administrator. What are two possible techniques to segment Azure for the departments?

a) multiple Azure Active Directory (Azure AD) directories

**b) multiple resource groups**

**c) multiple subscriptions**

d) multiple regions

**Note:**
- **Multiple subscriptions:** Each department can be assigned its own Azure subscription, which allows complete isolation of resources, billing, and management. This way, department administrators can manage their own resources without affecting others.
- **Multiple resource groups:** Within a single subscription, you can create multiple resource groups, each of which can be dedicated to a different department. Resource groups allow for organizing and managing resources, including access control and cost management.

**Other options:**
- **Multiple Azure Active Directory (Azure AD) directories:** While Azure AD directories provide identity and access management, they are not typically used to segment resources for different departments. It's more about organizing users and applications across the entire organization. 
- **Multiple regions:** Regions are geographic locations where Azure services are hosted, and they are used for redundancy, compliance, and performance. They are not typically used for department-level segmentation.

### Question 28

For each of the following statements, select Yes if the statements is true. Otherwise, select No.

- A single Microsoft account can be used to manage multiple Azure subscriptions: **Yes**
- Two Azure subscriptions can be merged into a single subscription: **No**
- A company can use resources from multiple subscriptions: **Yes**

### Question 29

To complete the sentence, select the appropriate option in the answer area.

- You have several virtual machines in an Azure subscription. You create a new subscription.

a) The virtual machines cannot be moved to the new subscription.

**b) The virtual machines can be moved to the new subscription.**

c) The virtual machines can be moved to the new subscription only if they are all in the same resource group.

d) The virtual machines can be moved to the new subscription only if they run Windows Server 2016.

**Note:**
- **You can move a VM and its associated resources to a different subscription** by using the **Azure portal**. Moving between subscriptions can be handy if you originally created a VM in a personal subscription and now want to move it to your company's subscription to continue your work. You do not need to start the VM in order to move it and it should continue to run during the move.

### Question 30

You have an Azure environment that contains multiple Azure virtual machines. You plan to implement a solution that enables the client computers on your on-premises network to communicate to the Azure virtual machines. You need to recommend which Azure resources must be created for the planned solution. Which two Azure resources should you include in the recommendation?

**a) a virtual network gateway**

b) a load balancer

c) an application gateway

d) a virtual network

**e) a gateway subnet**

**Note:**
- **Virtual Network Gateway:** A virtual network gateway is necessary to establish a VPN connection between the on-premises network and the Azure virtual network. It facilitates secure communication by acting as the gateway through which traffic passes when connecting on-premises resources with Azure.
- **Gatewat subnet:** A gateway subnet is required to host the virtual network gateway. It is a dedicated subnet in your Azure virtual network specifically for the gateway.

**Other options:**
- **A load balancer:** A load balancer is used for distributing traffic among virtual machines in Azure, not for connecting on-premises networks to Azure.
- **An application gateway:** An application gateway is a Layer 7 load balancer used for HTTP/HTTPS traffic management, not for establishing connections between on-premises and Azure.
- **A virtual network:** While a virtual network is necessary, it is implied in the question that the virtual machines already reside in a virtual network. You do not need to create a new one for this solution.

### Question 31

You attempt to create several managed Microsoft SQL Server instances in an Azure environment and receive a message that you must increase your Azure subscription limits. What should you do to increase the limits? 

**a) Create a new support request**

b) Upgrade your support plan

c)Create a service health alert

d) Modify an Azure policy

**Note:**
- When you need to increase your Azure subscription limits (quotas), the correct procedure is to create a support request with Azure. This is the process by which you can request an increase in the number of resources or services you are allowed to provision within your Azure subscription. Microsoft reviews the request and can approve an increase based on your requirements.

**Other options:**
- **Create a service health alert:** This option is used to monitor the health of Azure services and alert you to any outages or issues affecting the services you're using. It doesn't affect or change subscription limits.
- **Upgrade your support plan:** While upgrading your support plan can provide you with faster response times and more comprehensive support options, it does not automatically increase your resource limits.
- **Modify an Azure policy:** Azure policies are used to enforce organizational standards and assess compliance at scale. Modifying a policy won't change the subscription limits; it's used more for governance purposes.

### Question 32

For each of the following statements, select Yes if the statements is true. Otherwise, select No.

- Each Azure subscription can contain multiple account administrators: **Yes**
- Each Azure subscription can be managed by using a Microsoft account only: **No**
- An Azure resource group contais multiple Azure subscriptions: **No**

**Note:**
- Each Azure subscription can have multiple account administrators.
- We can create using a Microsoft account, but we can use AD.
- Think of Azure resource group as a room and Azure subscription as a house. We have many rooms inside a house, but we cannot have a house inside the room.

### Question 33

For each of the following statements, select Yes if the statements is true. Otherwise, select No.

- Availability zones can be implemented in all Azure regions: **No**
- Only virtual machines that run Windows Server can be created in availability zones: **No**
- Availability zones are used to replicate data and applications to multiple regions: **No**

**Note:**
- Not all Azure regions suppoort availability zones.
- Availability zones can be used with Azure services, not just VMs.
- Availability zones are unique physical locations within a single Azure region.

### Question 34

Your company plans to move several servers to Azure. You are evaluating which Azure services can be used to meet the compliance policy requirements. Which Azure solution should you recommend?

a) one resource group for all the servers and a resource lock for FinServer 

**b) a virtual network for FinServer and another virtual network for all the other servers**

c) a resource group for FinServer and another resource group for all the other servers 

d) a VPN for FinServer and a virtual network gateway for each other server

**Note:**
- This solution meets the compliance policy requirement by placing FinServer on a separate network segment. A virtual network (VNet) in Azure is a logical isolation of the Azure cloud dedicated to your subscription, which ensures that resources can only communicate with each other if they are in the same VNet or are connected via VNet peering.

**Other options:**
- **a resource group for FinServer and another resource group for all the other servers:** Resource groups are used for organizing and managing Azure resources, but they do not provide network isolation. All resources in different resource groups can still communicate over the same network unless specifically restricted.
- **a VPN for FinServer and a virtual network gateway for each other server:** A VPN is used for connecting Azure virtual networks with on-premises networks securely over the internet, but it does not inherently provide network segmentation within Azure.

### Question 35

Which service enables cloud architects and central information technology groups to define a repeatable set of Azure resources that implements and adheres to an organization's standards, patterns, and requirements? 

**a) Azure Blueprints**

b) Azure Monitor

c) Compliance Manager

d) Azure Advisor

**Note:**
- Azure Blueprints enables cloud architects and central IT groups to define a repeatable set of Azure resources that adheres to an organization's standards, patterns, and requirements. It allows for the creation of environments that comply with organizational policies by bundling together Resource Manager templates, policy assignments, role assignments, and Resource Groups into a single package. This helps to ensure that new deployments meet predefined standards and compliance requirements.

**Other options:**
- **Compliance Manager:** Compliance Manager is a tool in Microsoft 365 that helps organizations manage regulatory compliance activities related to Microsoft cloud services. It is not specifically designed for defining or deploying Azure resources.
- **Azure Monitor:** Azure Monitor is a service that provides full-stack monitoring and visibility across applications and infrastructure. It is used for monitoring the performance and health of Azure resources, not for defining or deploying them.
- **Azure Advisor:** Azure Advisor is a personalized cloud consultant that helps you follow best practices to optimize your Azure deployments. It provides recommendations for high availability, security, performance, and cost, but it does not define or deploy Azure resources like Azure Blueprints does.

### Question 36

Your business intends to use Azure to deploy an Artificial Intelligence (AI) solution. How should the business develop, test, and implement predictive analytics solutions?

a) Azure Logics Apps

b) Azure Batch

**c) Azure Machine Learning Designer**

d) Azure Cosmos DB

**Note:**
- **Azure Machine Learning Designer** is a visual, drag-and-drop interface in Azure Machine Learning that allows data scientists and developers to develop, test, and implement predictive analytics solutions. It enables users to create machine learning models, train them, and deploy them without writing extensive code. This tool is specifically designed for building Al and machine learning solutions, making it the most appropriate choice for developing predictive analytics solutions.

**Other options:**
- **Azure Batch** is a service that enables large-scale parallel and high- performance computing applications. It is used for running large-scale parallel jobs efficiently in the cloud, but it is not designed specifically for developing, testing, or implementing Al or predictive analytics solutions. 
- **Azure Cosmos DB** is a globally distributed, multi-model database service designed for building highly responsive, scalable applications. While it can be used to store and retrieve data, it is not used for developing predictive analytics solutions. 
- **Azure Logic Apps** is a cloud service that helps you automate workflows and integrate apps, data, services, and systems. It is used for creating automated workflows but is not designed for developing or deploying Al or predictive analytics solutions.

### Question 37

A company is planning to set up a Microservices-based application on Azure. They want to use a service that could be used to orchestrate the deployment of container-based applications. Which of the following could be used for this purpose? 

a) Azure Functions

b) Azure SQL Database

**c) Azure Kubernetes**

d) Azure Logic Apps

**Note:**
- **Azure Kubernetes Service (AKS)** is a managed container orchestration service that automates the deployment, management, and scaling of containerized applications using Kubernetes. It is specifically designed for orchestrating container-based applications and is a perfect choice for a microservices-based architecture on Azure.

**Other options:**
- **Azure Functions** is a serverless compute service that allows you to run event-driven code without managing infrastructure. It is used for running small pieces of code or functions in response to events, but it is not used for orchestrating containerized applications.
- **Azure Logic Apps** is a cloud service that helps automate workflows and integrate apps, data, services, and systems. It is not designed for orchestrating containerized applications but rather for automating workflows.
- **Azure SQL Database** is a fully managed relational database service in the cloud. While it is a database service, it is not used for orchestrating or deploying container-based applications.

### Question 38

A newly established company created the following resources using a pay-as-you-go Azure subscription. Azure Kubernetes and Azure Storage.  Account The Azure Kubernetes service belongs to which of the following deployment models? 

**a) Platform as a Service**

b) Hardware as a Service

c) Infrastructure as a Service

d) Software as a Service

**Note:**
- Azure Kubernetes Service (AKS) is a managed Kubernetes service, which means that Azure takes care of the underlying infrastructure, including the setup and management of the Kubernetes control plane and nodes. This makes AKS a Platform as a Service (PaaS) offering, as it provides a platform for deploying and managing containerized applications without having to manage the underlying infrastructure manually.

**Other options:**
- **Hardware as a Service (HaaS):** Haas typically refers to leasing physical hardware, which is not applicable to AKS, as AKS is a cloud service that abstracts away the physical hardware.
- **Infrastructure as a Service (IaaS):** IaaS refers to services that provide virtualized computing resources over the internet, such as virtual machines and storage. While AKS does involve infrastructure, it abstracts the infrastructure management, making it a PaaS rather than a pure IaaS service.
- **Software as a Service (SaaS):** SaaS refers to software that is centrally hosted and accessed via the internet (e.g., Microsoft Office 365). AKS is not a SaaS offering, as it provides a platform for deploying and managing applications rather than being an application itself.
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

**Note**: **Read-only geo-redundant storage (RA-GRS)** builds on GRS by allowing read access to the data in the secondary location as well as the primary. This option meets the requirement for data to be stored on multiple nodes in separate geographic locations and allows data to be read from both the primary and secondary locations.

**The other options:** **Geo-redundant storage (GRS)** provides redundancy by replicating data to a secondary geographic location, but it does not allow reading from secondary location unless the primary location fails. **Zone-redundant storage (ZRS)** stores data across multiple availability zones within the same region. **Locally redundant storage (LRS)** stores multiple copies of data within a single region.

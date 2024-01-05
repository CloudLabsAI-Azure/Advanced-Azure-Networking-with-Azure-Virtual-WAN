## Advanced Azure Networking with Azure Virtual WAN

Azure Networking Solutions provides a fundamental understanding of key networking concepts within the Microsoft Azure cloud platform. This overview serves as a primer for individuals and organizations looking to leverage Azure's networking capabilities to build secure, scalable, and highly available cloud environments.

### Key features of Azure Networking Solutions

  - **Virtual Networks (VNets)**: Azure VNets provide isolation and segmentation of resources in the cloud. They allow you to create private networks, control IP address ranges, and subnets, and segment resources based on requirements.

  - **Virtual Network Gateway**: This facilitates secure cross-premises connectivity by establishing encrypted connections between on-premises networks and Azure.

  - **Virtual WAN**: It is a service that brings many networking, security, and routing functionalities together to provide a single operational interface.

  - **Azure Firewall**: A managed network security service that filters and inspects network traffic, enforcing security policies and protecting Azure Virtual Network resources.

  - **Azure VPN Gateway**: Establishes encrypted cross-premises connections between Azure and on-premises networks, ensuring secure communication.

  - **Azure Bastion**: A managed service that provides secure RDP and SSH access to Azure virtual machines, eliminating the need for public IP addresses.


## Hands-on Lab Scenario

Contoso Insurance is preparing to launch a new online insurance portal that has been developed by its in-house development team. In order to ensure a smooth and successful launch, the portal will undergo testing by both internal and beta users. To facilitate this testing process, Contoso has chosen to utilize Azure as its cloud platform. Azure offers a wide range of Infrastructure as a Service (IaaS) capabilities, including computing, networking, storage, and security features. These features make Azure an ideal choice for businesses operating in the insurance industry.

In addition to testing the new portal, Contoso also has plans to modernize its operations by migrating its existing on-premises infrastructure to the Azure cloud. This migration will not only improve scalability but also enhance the overall security of their systems. To achieve this, Contoso will provision a comprehensive Azure Network Topology, which will include both a Platform and Application Landing Zone. Furthermore, they will establish hybrid connectivity between their on-premises data center and the Azure cloud.

Contoso is seeking assistance in configuring and deploying their insurance application on Azure, following the desired end-state architecture. This process will be carried out in phases, with the infrastructure of Azure resources for the Contoso Insurance Application being carefully aligned with the end-state architecture. Throughout the development and testing stages, progress will be closely monitored to ensure a successful outcome.

## Azure services and related products

  - Virtual Network
  - Virtual Machines
  - Virtual Network Gateway
  - Azure VPN Gateway
  - Azure Network Watcher

## Lab Context

You will learn the fundamentals of Azure networking in this hands-on lab. You will gain practical experience using networking resources, establishing connections between cloud-based and on-premise resources, and dealing with Azure resources.

### Exercise 1: Getting Started with Azure

In this exercise, you'll log in to the Azure Portal and review the pre-deployed resources that are part of the lab environment. 

### Exercise 2: Create a secured Virtual Hub and Azure firewall

This exercise walks you through the steps to convert a virtual WAN hub to a secured hub by installing Azure Firewall directly from the Azure Virtual WAN portal pages.

### Exercise 3: Enforce Branch-to-Branch Inspection

The exercise focuses on configuring rules, testing the webpage through Firewalls and configuring routing intent and policies through the Virtual WAN portal.

### Exercise 4: Isolate, Monitor and Remediate Azure vWAN Networking Issues

The exercise focuses on troubleshooting Azure vWAN networking issues, including viewing routes, configuring BGP peers, monitoring routes, using Azure Monitor Insights, and setting up packet captures for site-to-site VPNs, ensuring efficient network management and troubleshooting.


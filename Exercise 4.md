# Exercise 4: Virtual WAN custom routing

In this exercise you will create custom routing scenarios. 

As you learned from previous exercise the default routing in virtual WAN is Any-to-Any, but there are cases where you want to have custom routing.

## Task 1: Sample Scenario #1  

An on-premises connection should not have access to another branch connection transiting Virtual WAN (hub-to-hub connectivity).

1. Navigate to the home page in the Azure portal, type **Virtual WANs (1)** in the search box and select **Virtual WANs (2)** from the results.

    ![](media/11.png)

1. On the **Virtual WANs** page, select **vwan-prod-001**.

   ![](media/12.png)

1. On the **Basics** tab of the **vwan-prod-001** page, select **Hubs (1)** under the Connectivity section from the left navigation pane, and then click on **vwan-hub-prod-001 (2)**.

    ![](media/117.png)

1. On the **vwan-hub-prod-001** Virtual HUB page, select **Route Tables** under Routing.

1. Select the **Default** route table.

1. Select **Propagations** tab.

1. Toggle to **No** the Propagate routes from connections to this route table? option. 

1. Review the effective routes routing on the VM Nic on each on-premises network.


## Task 2: Sample Scenario #2

In this sample scenario, in addition to Scenario 1: 

- Azure VNets will be segmented into 2 separate trusted zones. Zone-1 and Zone-2: 

    - vnet-spoke1-<inject key="DeploymentID" enableCopy="false"/> on vhub-1 and vnet-spoke3-<inject key="DeploymentID" enableCopy="false"/> on vhub-2 will be members of Zone-1 and should be allowed to connect to each other but not to vnet-spoke2-<inject key="DeploymentID" enableCopy="false"/> and vnet-spoke4-<inject key="DeploymentID" enableCopy="false"/> which will members of Zone-2.

    - vnet-spoke2-<inject key="DeploymentID" enableCopy="false"/> on vhub-1 and vnet-spoke4-<inject key="DeploymentID" enableCopy="false"/> on vhub-2 (Zone-2) should be allowed to connect to each other but not to vnet-spoke1-<inject key="DeploymentID" enableCopy="false"/> on-vhub-1 and vnet-spoke3-<inject key="DeploymentID" enableCopy="false"/> on vhub-2 which will members of Zone-1.

- On-premises network should only access Azure vNets directly connected to their VPN connection and not across Virtual WAN hub-to-hub connectivity. 

- You will create a total of 4 route tables, 2 route tables on each hub like the below: 

   - rt-hub1-zone-1 

   - rt-hub1-zone-2 

   - rt-hub2-zone-1 

   - rt-hub2-zone-2 

- Each vnet connection will be associated with its own route table respectively. 

    - vnet-spoke1-<inject key="DeploymentID" enableCopy="false"/> on vhub-1 with rt-hub1-zone-1

    - vnet-spoke2-<inject key="DeploymentID" enableCopy="false"/> on vhub-1 with rt-hub1-zone-2 

    - vnet-spoke3-<inject key="DeploymentID" enableCopy="false"/> on vhub-2 with rt-hub2-zone-1 

    - vnet-spoke4-<inject key="DeploymentID" enableCopy="false"/> on vhub-2 with rt-hub2-zone-2

- 2 labels will be created: zone-1 and zone-2 that will be used on each route table.

### Create Route tables

1. Navigate to the home page in the Azure portal, type **Virtual WANs (1)** in the search box and select **Virtual WANs (2)** from the results.

    ![](media/11.png)

1. On the **Virtual WANs** page, select **vwan-prod-001**.

   ![](media/12.png)

1. On the **Basics** tab of the **vwan-prod-001** page, select **Hubs (1)** under the Connectivity section from the left navigation pane, and then click on **vwan-hub-prod-001 (2)**.

    ![](media/117.png)

1. On the **vwan-hub-prod-001** Virtual HUB page, select **Route Tables** under Routing and Select **+ Create Route Table**.


1. Enter Name of Route table named as 



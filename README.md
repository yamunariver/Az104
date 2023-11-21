##  You have an Azure subscription that contains a web app named App1.

You configure App1 with a custom domain name of webapp1.contoso.com.

You need to create a DNS record for App1. The solution must ensure that App1 remains accessible if the IP address changes.

Which type of DNS record should you create?

Select only one answer.

` `

`A`

`CNAME`

`SOA`

`SRV`

`TXT`

`For web apps, you create either an A (Address) record or a CNAME (Canonical Name) record. An A record maps a domain name to an IP address. A CNAME record maps a domain name to another domain name. DNS uses the second name to look up the address. Users still see the first domain name in their browser. If the IP address changes, a CNAME entry is still valid, whereas an A record must be updated.
`



## You have a Basic Azure App Service plan that contains a web app.

You need to ensure that the web app can scale automatically when the CPU percentage goes beyond 80 percent for a duration of 15 minutes.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

`
`

`Configure a deployment slot.`

`Configure a scaling condition to scale based on a metric, and then add the rules.`

`Configure a scaling condition to scale based on an instance count, and then set the instance count.`

`Scale out the App Service plan.`

`Scale up the App Service plan.`


`Scale up the web app by adding more CPU, memory, and disk space to fulfill the requirement. Increase the number of virtual machine instances that run the app. The scale settings take only seconds to apply and affect all the apps in the App Service plan. Then, you must set up a scaling condition with the required metrics to scale up/down and scale out/in when certain thresholds are met.`



## you have an Azure virtual network that contains two subnets named Subnet1 and Subnet2. You have a virtual machine named VM1 that is connected to Subnet1. VM1 runs Windows Server.

You need to ensure that VM1 is connected directly to both subnets.

What should you do first?

Select only one answer.


` `
`From the Azure portal, add a network interface.`

`From the Azure portal, create an IP group.`

`From the Azure portal, modify the IP configurations of an existing network interface.`

`Sign in to Windows Server and create a network bridge.`


`A network interface is used to connect a virtual machine to a subnet. Since VM1 is connected to Subnet1, VM1 already has a network interface attached that is connected to Subnet1. To connect VM1 directly to Subnet2, you must create a new network interface that is connected to Subnet2. Next, you must attach the new network interface to VM1.`

`An IP group is a user-defined collection of static IP addresses, ranges, and subnets. A network bridge allows you to connect multiple existing network connection in Windows together. Changing the IP configurations of the existing network interface results in VM1 being connected to Subnet2 but not to Subnet1.`




## You have an Azure subscription that contains a resource group named RG1.

You have an Azure Resource Manager (ARM) template for an Azure virtual machine.

You need to use PowerShell to provision a virtual machine in RG1 by using the template.

Which PowerShell cmdlet should you run?

Select only one answer.

`
`
`New-AzManagementGroupDeployment`

`New-AzResourceGroupDeployment`

`New-AzSubscriptionDeployment `

`New-AzVM`


`Virtual machines are deployed to resource groups, so you must run the New-AzResourceGroupDeployment cmdlet. You can deploy virtual machines to subscriptions or management groups directly, therefore, New-AzManagementGroupDeployment and New-AzSubscriptionDeployment cannot be used. New-AzVM can be used to provision a new virtual machine, but without using a template.`




## You have an Azure subscription that contains four virtual machines. Each virtual machine is connected to a subnet on a different virtual network.

You install the DNS Server role on a virtual machine named VM1.

You configure each virtual network to use the IP address of VM1 as the DNS server.

You need to ensure that all four virtual machines can resolve IP addresses by using VM1.

What should you do?


Select only one answer.

`
`

`Configure a DNS server on all four virtual machines.`

`Configure network peering.`

`Create and associate a route table to all four subnets.`

`Create Site-to-Site (S2S) VPNs.`



`By default, Azure virtual machines can communicate only with other virtual machines that are connected to the same virtual network. If you want a virtual machine to communicate with other virtual machines that are connected to other virtual networks, you must configure network peering.`

`A route table controls how network traffic is routed. But without network peering, network traffic is still limited to single virtual network.`

`Configuring a Site-to-Site (S2S) VPN is incorrect because you are not connecting on-premises virtual machines to the cloud.`



## You have an Azure subscription.

You plan to implement four Azure virtual networks that will be peered. All virtual machines will use a DNS suffix of contoso.com.

You need to configure name resolution for the virtual networks to ensure that all the virtual machines can communicate by using their FQDNs. The solution must minimize administrative effort.

What should you use?

Select only one answer.

`a DNS server on an Azure virtual machine`

`an Azure Private DNS zone`

`an Azure public DNS zone`

`Azure-provided name resolution`

`Azure Private DNS allows for private name resolution between Azure virtual networks. Azure public DNS provides DNS for public access, such as name resolution for a publicly accessible website. Azure-provided name resolution does not support user-defined domain names and only supports a single virtual network. A DNS server on a virtual machine can also be used to achieve the goal but involves much more administrative effort to implement and maintain than using Azure Private DNS.`



## You have an Azure subscription that contains a virtual network named VNet1.

You plan to enable VNet1 connectivity to on-premises resources by using an encrypted connection.

What should you configure for VNet1?

Select only one answer.

`a private endpoint connection`

`a public IP address`

`a VPN`

`internet routing`


`A VPN gateway is a type of virtual network gateway that sends encrypted traffic between a virtual network and an on-premises location across a public connection. You can also use a VPN gateway to send traffic between virtual networks across the Azure backbone. A VPN gateway connection relies on the configuration of multiple resources, each of which contains configurable settings.`






## You have an Azure subscription that contains a virtual network named VNet1.

You plan to deploy a virtual machine named VM1 to be used as a network inspection appliance.

You need to ensure that all network traffic passes through VM1.

What should you do?


Select only one answer.




`Configure a user-defined route.`

`Create a virtual network gateway.`

`Modify the default route.`

`Modify the system route.`



`Azure automatically creates a route table for each subnet on an Azure virtual network and adds system default routes to the table. You can override some of the Azure system routes with custom user-defined routes and add more custom routes to route tables. Azure routes outbound traffic from a subnet based on the routes on a subnet's route table.`



## You have a Microsoft Entra tenant.

Your company has several offices in the same region. Each office has a dedicated IT staff.

You need to ensure that the IT staff in each office can manage passwords for their users and administrators.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.


`Assign the Helpdesk Administrator role.`

`Assign the Password Administrator role.`

`From the Azure portal, add administrative units.`

` From the Azure portal, create a new custom role. `

` You must create an administrative unit and the Helpdesk role assignment allows members to change password for both users and other administrators. `



## You have an Azure subscription that contains a tenant named contoso.com.

All users in contoso.com are currently able to invite external users to B2B collaboration.

You need to ensure that only members of the Guest Inviter, User Administrator, and Global Administrator roles can invite guest users.

What should you configure?

Select only one answer.


`Access reviews`

`Conditional Access`

`Cross-tenant access settings`

`External collaboration settings`

``External collaboration settings let you specify which roles in your organization can invite external users for B2B collaboration. These settings also include options for allowing or blocking specific domains and options for restricting which external guest users can see in your Microsoft Entra directory.
``
`` Conditional Access allows you to apply rules to strengthen authentication and block access to resources from unknown locations. ``

`` Cross-tenant access settings are used to configure collaboration with a specific Microsoft Entra organization. ``

`` Access reviews are not used to control who can invite guest users.  ``


## You have an Azure subscription that contains 200 virtual machines.

You plan to use Azure Advisor to provide cost recommendations when underutilized virtual machines are detected.

You need to ensure that all Azure admins are notified whenever an Advisor alert is generated. The solution must minimize administrative effort.

What should you configure?


Select only one answer.


`an action group`

`an application security group`

`an Azure Automation account`


`a capacity reservation group`

`
Whenever Azure Advisor detects a new recommendation for resources, an event is stored in the Azure Activity log. You can set up alerts for these events from Azure Advisor. You can select a subscription and optionally a resource group to specify the resources for which you want to receive alerts. You also need to create an action group that will contain all the users to be notified.
`



## You have an Azure subscription that contains a container app named App1. App1 is configured to use cached data.

You plan to create a new container.

You need to ensure that the new container automatically refreshes the cache used by App1.

Which type of container should you configure?

Select only one answer.

`blob`

`init`

`privileged`

`sidecar`

`
Azure Container Apps manages the details of Kubernetes and container orchestration. Containers in Azure Container Apps can use any runtime, programming language, or development stack of your choice. You can define multiple containers in a single container app to implement the sidecar pattern, for example, an agent that reads logs from the primary app container in a shared volume and forwards them to a logging service
`


## You have a Basic Azure App Service plan that contains a web app.

You need to ensure that the web app can scale automatically when the CPU percentage goes beyond 80 percent for a duration of 15 minutes.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.


`Configure a deployment slot.`

`Configure a scaling condition to scale based on a metric, and then add the rules.`

`Configure a scaling condition to scale based on an instance count, and then set the instance count.`

`Scale out the App Service plan.`

`Scale up the App Service plan.`

`
Scale up the web app by adding more CPU, memory, and disk space to fulfill the requirement. Increase the number of virtual machine instances that run the app. The scale settings take only seconds to apply and affect all the apps in the App Service plan. Then, you must set up a scaling condition with the required metrics to scale up/down and scale out/in when certain thresholds are met.
`


## You have an Azure Resource Manager (ARM) template named deploy.json that is stored in an Azure Blob storage container.

You plan to deploy the template by running the New-AzDeployment cmdlet.

Which parameter should you use to reference the template?

Select only one answer.


`-Tag `

`-Templatefile `

`-TemplateSpecId`

`-TemplateUri`

`The PowerShell deployment cmdlets can be used to deploy JSON templates that are stored locally in a resources group as a template spec, or from a web-based location. You can use the -TemplateUri parameter to specify a web-based location, such as GitHub or an Azure Blob Storage account. You can use -Templatefile to specify a local file. You can use -TemplateSpecId to specify a template that was save to Azure as a template spec.
`


## You need to create an Azure Storage account that supports the Azure Data Lake Storage Gen2 capabilities.

Which two types of storage accounts can you use? Each correct answer presents a complete solution.

Select all answers that apply.

`premium block blobs`

`premium file shares`

`standard general-purpose v2`

`premium page `

`To support Data Lake Storage, the storage account must support blob storage, which is available as standard general-purpose v2 and premium block blobs. Additionally, when you create the storage account, you must enable the hierarchical namespace.
`


## You plan to deploy an Azure virtual machine based on a basic template stored in the Azure Resource Manager (ARM) library.

What can you configure during the deployment of the template?

Select only one answer.

`the disk assigned to virtual machine`

`the operating system`

`the resource group`

`the size of virtual machine`

## Exp: When you deploy a resource by using a template, you can mention the resource group for the deployment. The resource group is a container for Azure resources and makes it easier to manage the resources.


## You have an Azure subscription that contains a resource group named RG1.

You have an Azure Resource Manager (ARM) template for an Azure virtual machine.

You need to use PowerShell to provision a virtual machine in RG1 by using the template.

Which PowerShell cmdlet should you run?

Select only one answer.


`New-AzManagementGroupDeployment`

`New-AzResourceGroupDeployment`

`New-AzSubscriptionDeployment `

`New-AzVM`

## Exp:  Virtual machines are deployed to resource groups, so you must run the New-AzResourceGroupDeployment cmdlet. You can deploy virtual machines to subscriptions or management groups directly, therefore, New-AzManagementGroupDeployment and New-AzSubscriptionDeployment cannot be used. New-AzVM can be used to provision a new virtual machine, but without using a template.


## You plan to use the following two Azure Resource Manager (ARM) templates to provision virtual machines:

Template.json

{ 

  "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#", 

  "contentVersion": "1.0.0.0", 

  "parameters": { 

    "adminUsername": { 

      "type": "string", 

      "metadata": { 

        "description": "User name for the Virtual Machine." 

      } 

    }, 

    "adminPassword": { 

      "type": "securestring", 

      "metadata": { 

        "description": "Password for the Virtual Machine." 

      } 

    }, 

    "dnsLabelPrefix": { 

      "type": "string", 

      "defaultValue": "[concat('vm-', uniqueString(resourceGroup().id))]", 

      "metadata": { 

        "description": "Unique DNS Name for the Public IP used to access the Virtual Machine." 

      } 

    }, 

... 

{ 

      "apiVersion": "2019-12-01", 

      "type": "Microsoft.Compute/virtualMachines", 

      "name": "[variables('vmName')]", 

      "location": "[parameters('location')]", 

      "dependsOn": [ 

        "[variables('storageAccountName')]", 

        "[variables('nicName')]" 

      ], 

      "properties": { 

        "hardwareProfile": { 

          "vmSize": "[parameters('vmSize')]" 

        }, 

        "osProfile": { 

          "computerName": "[variables('vmName')]", 

          "adminUsername": "[parameters('adminUsername')]", 

          "adminPassword": "[parameters('adminPassword')]" 

        }, 

... 
Template.parameters.json

{ 

  "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentParameters.json#", 

  "contentVersion": "1.0.0.0", 

  "parameters": { 

    "adminUsername": { 

      "value": "" 

    }, 

    "adminPassword": { 

             ... 

      } 

    } 

  } 

} 
Which two resources should you provision to ensure that the password can be stored securely?

Select all answers that apply.

Access Policy

an Azure compliance policy

an Azure Storage account

Azure Key Vault

## Exp: You must create a new key vault, create the password from there, and then specify the parameters. You must also create a Key Vault access policy to use in the template.




## You have an Azure subscription that contains hundreds of virtual machines that were migrated from a local datacenter.

You need to identify which virtual machines are underutilized.

Which Azure Advisor settings should you use?

Select only one answer.


Cost

High Availability

Operational Excellence

Performance

## Exp: The Cost blade allows you to optimize and reduce your overall Azure spending. You can use this to identify the virtual machines that are underutilized. The Performance blade allows you to improve the speed of your applications. High availability is unavailable via Azure Advisor. Operational Excellence helps you achieve process and workflow efficiency, resource manageability, and deployment best practices.



## You have an Azure subscription that contains a resource group named RG1. RG1 contains a virtual machine that runs daily reports.

You need to ensure that the virtual machine shuts down when resource group costs exceed 75 percent of the allocated budget.

Which two actions should you perform? Each correct answer presents part of the solution.


Select all answers that apply.


Create an action group of type Runbook, and then select Scale Up VM.

Create an action group of type Runbook, and then select **Stop VM** as an action.

From Cost Management + Billing, create a new cost analysis.

From Cost Management + Billing, modify the Budgets settings.


## Exp: You must go to Cost Management + Billing, and then Budgets to edit the budget associated with the resource group resources. You must also create a new action group of the Runbook type, and then choose Stop VM as an action. The cost analysis will not stop the virtual machine from running and the Scale Up VM action group is not required.


## You have an Azure subscription and a user named User1.

You need to assign User1 a role that allows the user to create and manage all types of resources in the subscription. The solution must prevent User1 from assigning roles to other users.

Which Azure role-based access control (RBAC) role should you assign to User1?

Select only one answer.


API Management Service Contributor

Contributor

Owner

Reader


## Exp: Users with the Contributor role can create and manage all types of resources but cannot delegate new access to other users. Users with the Reader role can view existing Azure resources but cannot perform any action against them. Users with the API Management Service Contributor role can only manage API Management services and APIs. Users with the Owner role provides full access to all resources, including the right to delegate access to others.


## You have the following resource groups, management groups, and Azure subscriptions:

Two resource groups named RG1 and RG2 that are associated with a subscription named 111-222-333 and a management group named MG1
Two resource groups named RG3 and RG4 that are associated with a subscription named 777-888-999 and a management group named MG1
Two resource groups named RG5 and RG6 that are associated with a subscription named 444-555-666 and a management group named MG1
Two resource group named RG10 and RG11 that are associated with a subscription named 222-333-444 and a management group named MG2
Two resource group named RG11 and RG12 that are associated with a subscription named 555-666-888 and a management group named MG2
You need to assign a role to a user to ensure the user can view all the resources in the subscriptions. The solution must use the principle of least privilege.

Which role should you assign?

Select only one answer.


the Billing Reader role for all the subscriptions

the Billing Reader role for MG1 and MG2

the Contributor role for MG1 and MG2

the Reader role for MG1 and MG2


## Exp: Assigning the Reader role for MG1 and MG2 is correct because the simplest way to give user access to all resources is to assign a role at the management group level.


## You have a Microsoft Entra tenant named contoso.com. Microsoft Entra Connect is configured to sync users to the tenant.

You need to assign licenses to the users based on Microsoft Entra ID attributes. The attribute values will be set by the HR department.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.


Assign the licenses to the dynamic groups.

Assign the licenses to the security groups.

Create an automatic assignment policy.

Create dynamic groups.

Create security groups.


## Exp: To assign licenses to users based on Microsoft Entra ID attributes, you must create a dynamic security group and configure rules based on custom attributes. The dynamic group must be added to a license group for automatic synchronization. All users in the groups will get the license automatically. Microsoft Entra evaluates the users in the organization that are in scope for an assignment policy rule and creates assignments for the users who don't have assignments to an access package; automatic assignment policies are not used for licensing.

## You deploy web servers to two virtual machines named VM1 and VM2 in an availability set named AVSet1.

You need to configure Azure Load Balancer with a backend pool of VM1 and VM2. The solution must minimize costs.

Which SKU should you use for the Azure Load Balancer configuration?


Select only one answer.

Azure Standard Load Balancer with Basic SKU public IP

Azure Standard Load Balancer with Standard SKU public IP

Basic Azure Load Balancer with Basic SKU public IP

Basic Azure Load Balancer with Standard SKU public IP


## Exp: Basic Azure Load Balancer supports deployment in a single availability zone. Basic Azure Load Balancer supports only Basic SKU public IP. Azure Standard Load Balancer is zone-redundant, but has a higher cost.






## You have three network security groups (NSGs) named NSG1, NSG2, and NSG3. Port 80 is blocked in NSG3 and allowed in NSG1 and NSG2.

You have four Azure virtual machines that have the following configurations:

VM1:

Subnet: Subnet1
Network card: NIC1
NIC1 is assigned to NSG2.
VM2:

Subnet: Subnet1
Network card: NIC2
NIC2 is assigned to NSG3.
VM3:

Subnet: Subnet3
Network card: NIC3
NIC3 is assigned to NSG3.
VM4:

Subnet: Subnet2
You have the following subnets:

Subnet1 is assigned to NSG1.
Subnet2 is assigned to NSG3.
Subnet 3 does not have an NSG assigned.
Which virtual machine will allow traffic from the internet on port 80?

Select only one answer.


VM1

VM2

VM3

VM4


## Exp: On VM1, both NSGs assigned to Subnet1 and the NIC1 card allow traffic on port 80. On VM2, NSG1 allows traffic, but NSG3 blocks traffic for the network interface. On VM3 and VM4, NSG3 blocks traffic.






## You have an Azure virtual network that contains four subnets. Each subnet contains 10 virtual machines.

You plan to configure a network security group (NSG) that will allow inbound traffic over TCP port 8080 to two virtual machines on each subnet. The NSG will be associated to each subnet.

You need to recommend a solution to configure the inbound access by using the fewest number of NSG rules possible.

What should you use as the destination in the NSG?

Select only one answer.


an application security group

a service tag

the subnets of the virtual machines


## Exp: Application security groups allow you to group together the network interfaces from multiple virtual machines, and then use the group as the source or destination in an NSG rule. The network interfaces must be in the same virtual network. *) You can use the IP address of each virtual machine as the destination, but you must create a rule for each virtual machine. *) Using the subnets will require four rules and will also allow traffic to all the virtual machines on those subnets. *) Service tags are for specific Azure services, such as Azure App Service or Azure Backup.



## You have an Azure subscription that contains a network security group (NSG) named NSG1.

You plan to configure NSG1 to allow the following types of traffic:

Remote Desktop Management
Secured HTTPS
Which two ports should you allow in NSG1? Each correct answer presents part of the solution.

Select all answers that apply.


80

25

443

587

3389


## Exp: You must open port 443 to secured HTTPS traffic, port 3389 for Remote Desktop, and 587 to send outbound email by using authenticated SMTP relay. Port 80 is used for unsecured traffic. Port 25 is used by mail traffic.


## You have an Azure subscription that contains two resource groups named RG1 and RG2.

RG1 contains the following resources:

A virtual network named VNet1 located in the East US Azure region
A network security group (NSG) named NSG1 located in the West US Azure region
RG2 contains the following resources:

A virtual network named VNet2 located in the East US Azure region
A virtual network named VNet3 located in the West US Azure region
You need to apply NSG1.

To which subnets can you apply NSG1?

Select only one answer.


the subnets of all the virtual networks

the subnets of VNet1 only

the subnets of VNet1 and VNet2

the subnets of VNet3 only


## Exp: You can assign an NSG to the subnet of the virtual network in the same region as the NSG and NSG1 is in the West US region.

## You need to create Azure alerts based on metric values and activity log events.

The solution must meet the following requirements:

Set a limit on how many times an alert notification is sent.

Call an Azure function when an alert is triggered.

Configure the alert to have a severity of warning when triggered.

Which two resources should you create? Each correct answer presents part of the solution.

Select all answers that apply.

an action group

an alert rule

a notification

a secure webhook

## Exp: You must create an action group to set up an action and create an alert rule to set the severity of the errors. A notification is only used to send email and you do not need to call a webhook.


## You have an Azure subscription.

You plan to deploy a web app in a Linux-based Docker container.

You need to recommend a solution for the deployment of the web app that meets the following requirements:

Supports a custom domain name
Provides the ability to scale out automatically based on demand.
Minimizes administrative effort
Minimizes costs

Which solution should you recommend?

Select only one answer.

Azure App Service


Azure Container Instances

Azure Kubernetes Service (AKS)

Azure Virtual Machine Scale Sets
## Exp: Azure App Service fulfills all the stated requirements. Azure Virtual Machine Scale Sets, Azure Kubernetes Service (AKS), and Azure Container Instances are more difficult to administer and more costly.



## You need to create an Azure App Service web app that runs on Windows. The web app requires scaling to five instances, 45 GB of storage, and a custom domain name. The solution must minimize costs.

Which App Service plan should you use?

Select only one answer.


Basic

Free

Premium

Standard

## Exp: The Standard service plan can host unlimited web apps, up to 50 GB of disk space, and up to 10 instances. The plan will cost approximately $0.10/hour. The Free plan only offers 1 GB of disk size and 0 instances to host the app. The Premium plan offers 250 GB of disk space and up to 30 instances and will cost approximately $0.20/hour. The Basic plan offers 10 GB of disk space and up to three virtual machines.


## You have a Basic Azure App Service plan that contains a web app.

You need to ensure that the web app can scale automatically when the CPU percentage goes beyond 80 percent for a duration of 15 minutes.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.



Configure a deployment slot.

Configure a scaling condition to scale based on a metric, and then add the rules.

Configure a scaling condition to scale based on an instance count, and then set the instance count.

Scale out the App Service plan.

Scale up the App Service plan.
## Exp: Scale up the web app by adding more CPU, memory, and disk space to fulfill the requirement. Increase the number of virtual machine instances that run the app. The scale settings take only seconds to apply and affect all the apps in the App Service plan. Then, you must set up a scaling condition with the required metrics to scale up/down and scale out/in when certain thresholds are met.



## You have an Azure subscription that contains multiple resource groups and Azure App Service web apps. A resource group named RG1 hosts a web app named appservice1. The App Service uses an imported SSL certificate.

You create a resource group named RG2.

You plan to move all the resources in RG1 to RG2.

Which two actions should you perform? Each correct answer presents part of the solution.



Select all answers that apply.


Create a new App Service plan in RG2.

Create a new web app in RG2.

Delete the SSL Certificate from RG1 and upload it to RG2.

Move all the resources from RG1 to RG2.

## Exp: The SSL certificate must be deleted. You will have to move all other resources to RG2.


## You have an Azure subscription that contains an Azure container app named cont1.

You plan to add scaling rules to cont1.

You need to ensure that cont1 replicas are created based on received messages in Azure Service Bus.

Which scale trigger should you use?


Select only one answer



CPU usage

event-driven

HTTP traffic

memory usage

## Exp: Azure Container Apps allows a set of triggers to create new instances, called replicas. For Azure Service Bus, an event-driven trigger can be used to run the escalation method. The remaining scale triggers cannot use a scale rule based on messages in an Azure service bus.


## You have an Azure subscription that contains a Docker container image named container1.

You create a new Azure web app named WebApp1.

You need to ensure that you can use container1 for WebApp1.

Which WebApp1 setting should you configure?


Select only one answer.


Continuous deployment

Pricing plan

Publish

Runtime stack

## Exp: 

If you want to run a Docker container as an Azure web service, you must configure the Publish option and select Docker container.

Runtime stack specifies the stack that you want to use for the web app. If you want to deploy a Docker container as web app, the runtime stack option is unavailable.

Pricing plan specifies the location, features, and costs of the web app.

Continuous deployment is a strategy for software releases. This option is unavailable when you publish a Docker container as an Azure web app.
  



## You are deploying a virtual machine by using an availability set in the East US Azure region.

You have deployed 18 virtual machines in two fault domains and 10 update domains.

Microsoft performed planned physical hardware maintenance in the East US region.

What is the maximum number of virtual machines that will be unavailable?
``

Select only one answer.


2

8

9

18


## Exp: 18 virtual machines are shared across 10 update domains. The first 10 virtual machines go to 10 update domains, so eight update domains will have two virtual machines. When there is physical hardware maintenance, some virtual machines will be unavailable based on their configuration. If there was a rack failure, then 18 virtual machines will be distributed to two fault domains with nine virtual machines each.


## You have an Azure virtual machine.

## You receive a notification that the virtual machine is going to be affected by an underlying maintenance activity on the physical infrastructure.

## You need to move the virtual machine to a different host to avoid a service interruption.

What should you do?

Select only one answer.



Apply an Azure policy.

Apply an Azure tag.

Move the virtual machine to another Azure subscription.

Redeploy the virtual machine.


## Exp: You must redeploy the virtual machine, which can move the virtual machine to a different host. Azure will shut down the virtual machine and move the virtual machine to a new node within the Azure infrastructure.


## You have an Azure virtual network that contains two subnets named Subnet1 and Subnet2. You have a virtual machine named VM1 that is connected to Subnet1. VM1 runs Windows Server.

You need to ensure that VM1 is connected directly to both subnets.

What should you do first?

Select only one answer.


From the Azure portal, add a network interface.

From the Azure portal, create an IP group.

From the Azure portal, modify the IP configurations of an existing network interface.

Sign in to Windows Server and create a network bridge.

## Exp: A network interface is used to connect a virtual machine to a subnet. Since VM1 is connected to Subnet1, VM1 already has a network interface attached that is connected to Subnet1. To connect VM1 directly to Subnet2, you must create a new network interface that is connected to Subnet2. Next, you must attach the new network interface to VM1. \n An IP group is a user-defined collection of static IP addresses, ranges, and subnets. A network bridge allows you to connect multiple existing network connection in Windows together. Changing the IP configurations of the existing network interface results in VM1 being connected to Subnet2 but not to Subnet1.





## You have a Log Analytics workspace that collects data from various data sources.

You create a new Azure Monitor log query.

You plan to view data pinned as a chart to a shared dashboard.

What is the maximum number of days for which data can be pinned as a chart on the dashboard?

Select only one answer.

14

30

90

180


## You need to create Azure alerts based on metric values and activity log events.

The solution must meet the following requirements:

Set a limit on how many times an alert notification is sent.

Call an Azure function when an alert is triggered.

Configure the alert to have a severity of warning when triggered.

Which two resources should you create? Each correct answer presents part of the solution.

Select all answers that apply.


an action group

an alert rule

a notification

a secure webhook

## EXP: You must create an action group to set up an action and create an alert rule to set the severity of the errors. A notification is only used to send email and you do not need to call a webhook.


## You have an Azure Resource Manager (ARM) template named deploy.json that is stored in an Azure Blob storage container.

You plan to deploy the template by running the New-AzDeployment cmdlet.

Which parameter should you use to reference the template?

Select only one answer.


`-Tag `

`-Templatefile `

-TemplateSpecId

-TemplateUri

## Exp: The PowerShell deployment cmdlets can be used to deploy JSON templates that are stored locally in a resources group as a template spec, or from a web-based location. You can use the -TemplateUri parameter to specify a web-based location, such as GitHub or an Azure Blob Storage account. You can use -Templatefile to specify a local file. You can use -TemplateSpecId to specify a template that was save to Azure as a template spec.


## You plan to deploy an Azure virtual machine based on a basic template stored in the Azure Resource Manager (ARM) library.

What can you configure during the deployment of the template?


Select only one answer.


the disk assigned to virtual machine

the operating system

the resource group

the size of virtual machine

## Exp: When you deploy a resource by using a template, you can mention the resource group for the deployment. The resource group is a container for Azure resources and makes it easier to manage the resources.


## You are creating an Azure virtual machine that will run Windows Server.

You need to ensure that VM1 will be part of a virtual machine scale set.

Which setting should you configure during the creation of the virtual machine?

Select only one answer.

Availability options

Azure Spot instance

Management

Region

## Exp: You must configure the virtual machine scale set from the availability options. Azure spot instance is used to add virtual machines with a discounted price. Region will not affect the configuration of the availability options. The management setting allows you to configure the monitoring and management options for the virtual machine.

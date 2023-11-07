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

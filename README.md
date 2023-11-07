## You have an Azure virtual network that contains two subnets named Subnet1 and Subnet2. You have a virtual machine named VM1 that is connected to Subnet1. VM1 runs Windows Server.

You need to ensure that VM1 is connected directly to both subnets.

What should you do first?

Select only one answer.


From the Azure portal, add a network interface.

From the Azure portal, create an IP group.

From the Azure portal, modify the IP configurations of an existing network interface.

Sign in to Windows Server and create a network bridge.


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

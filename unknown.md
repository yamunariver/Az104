## You plan to provision an Azure subscription that will contain the following virtual networks:

VNet1 in the East US Azure region with two subnets
VNet2 in the East US region with four subnets
VNet3 in the West Europe Azure region with four subnets
VNet4 in the West Europe region with two subnets
How many Azure Network Watcher instances will be provisioned as part of the deployment?

Select only one answer.

` `

`1`

`2`

`4`

`12`


`Azure Network Watcher is a regional service that allows you to monitor and diagnose conditions at a network scenario level in, to, and from Azure. When you create or update a virtual network in a subscription, Network Watcher will be enabled automatically in the virtual network's region. There is no impact on resources or associated charges for automatically enabling Network Watcher.`



## You have an Azure virtual network named VNet1 that is deployed to the Azure East US region.

You need to ensure that email is sent to an administrator when a virtual machine is connected to VNet1.

What should you create?

Select all answers that apply.

` `

`an action group`

`an alert processing rule`

`an alert rule`

`a mail-enabled security group`



`Azure Monitor alerts proactively notify you when important conditions are found in monitoring data. They allow you to identify and address issues in the system before customers notice them. You can set alerts on metrics, logs, and the activity log. Different types of alerts have benefits and drawbacks. Metrics is a feature of Azure Monitor that collects numeric data from monitored resources into a time-series database. Metrics are numerical values that are collected at regular intervals and describe some aspect of a system at a particular time.`

`When Azure Monitor data indicates that there may be an issue with an infrastructure or application, an alert is triggered. Azure Monitor, Azure Service Health, and Azure Advisor then use action groups to notify users about the alert and take action. An action group is a collection of notification preferences defined by the owner of an Azure subscription.`





## You have an Azure subscription that contains two protected virtual machines named VM1 and VM2. VM1 and VM2 are backed up to a Recovery Service vault named Vault1 by using the same backup policy.

Your company plans to create additional virtual machines and Recovery Services vaults. During this process, Vault1 will be decommissioned.

You need to delete Vault1.

Which three actions should you perform before you can delete Vault1? Each correct answer presents part of the solution.

Select all answers that apply.

` `

`Delete VM1 and VM2.`

`Disable the soft delete feature and delete all data.`

`Enable a Read lock on Vault1.`

`Permanently remove any items in the soft delete state.`

`Stop the backup of VM1 and VM2.`



`You must stop the backups so that you can prepare to move to the new policy. The soft delete feature is enabled by default, so it must be disabled. You must remove all the items that are in the soft delete state. Deleting the virtual machines is not required. You cannot delete the policy without deleting the vault and backup, and a new policy is not required.`





## Your company has a main office in Seattle and a branch office in New York.

You have an Azure subscription that contains an application named App1 and a user named User1 located in the Seattle office.

User1 travels to the New York office and receives the following error message when attempting to sign in to App1: “Your sign-in was blocked.”

When located in the Seattle office, the access of User1 functions properly, and no other users report issues with accessing App1.

You need to ensure that User1 can sign in to App1.

What should you do from the Microsoft Azure portal?


Select only one answer.

` `

`Add the New York office as a named location.`

`Configure Sign-in risk policy`

`Disable the Users at risk detected alerts setting for User1.`

`From the Risky sign-ins report, confirm that the sign-in of User1 is safe.`

`From the Risky users report, dismiss the user risk for User1.`

`Identity Protection provides organizations with three reports that they can use to investigate identity risks in their environment. These reports are Risky users, Risky sign-ins, and Risk detections. Investigation of events is key to better understanding and identifying any weak points in your security strategy. When users sign in to Azure from a remote location, Identity protection may identify these users as risky users. Unless the user risk is remediated, they will not be able to sign in. You can dismiss a user risk from the Risky users report in Identity Protection.`

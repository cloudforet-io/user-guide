# \(Azure\) Access Control \(IAM\) Policy Management

## **Access Control** Policy

**SpaceONE** highly recommends to set appropriate permissions to Resource groups for each purpose. 

Please, Set service account, To Create API for each use case:

* [General Collector](azure-access-control-iam-policy-management.md#general-collector)

## General Collector 

Collector requires appropriate authorities to collect cloud resources. We strongly recommend to limit collector's service account its permission to **read only access**. 

Otherwise, you can add more restrictions per resource groups or actions. One of the useful example is to restrict its rights within resource groups.

\*\*\*\*

**Prerequisite**

This user guide tutorial assumes that a `subscription id` is already created.

There are two options for giving permission to Azure resources which SpaceONE is going to collect.

* Grant `Reader role` to **resource group** where resources are located. If you give a role to resource group, _SpaceONE_ can only collect resources located in this resource group.
* Grant `Reader role` to **subscription** where resources are located. If you give a role to the subscription, SpaceONE can collect resources in all resource groups in this subscription.

If you want to know more about Azure's access control policies, visit the link below.

[https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal](https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal)

**Grant Roles to resource groups**

**STEP 1. Log in Azure Portal &gt; Resource groups** 

Select the resource group for which the collector will collect resources.

![](../../.gitbook/assets/image%20%28104%29.png)

**STEP 2. Click `Access control (IAM)` Navigation tab, and click `+Add` button.**

![](../../.gitbook/assets/image%20%28102%29.png)



**STEP 3: Assign the `Reader role`  to the account. The account should  have an access permission in this resource group.**



![](../../.gitbook/assets/image%20%28103%29.png)

## Troubleshooting

### Authorization

Please, follow the steps on troubleshooting guide below if you face any of error messages above.

#### 1. \(AuthorizationFailed\) Client does not have authorization 

{% hint style="warning" %}
The client `client_id` with object id `object_id` does not have authorization to perform action Microsoft.Resources/subscriptions/resourcegroups/read over scope `subscription_id` or the scope is invalid. If access was recently granted, please refresh your credentials
{% endhint %}

**STEP 1: Log in Azure Portal and Drive to &gt; Subscriptions** 

![](../../.gitbook/assets/screen-shot-2021-04-15-at-18.55.14.png)

  
**STEP 2: Click the subscription name where resources are located.**

![](../../.gitbook/assets/image%20%28114%29.png)

**STEP 3: Click `+Add role assignment` button.**

![](../../.gitbook/assets/image-2-.png)

\*\*\*\*

**STEP 4: Add role `Reader` assignment as below. Select the account entered in the service account of the** _**SpaceONE**_ **console.**

![](../../.gitbook/assets/image%20%28115%29.png)


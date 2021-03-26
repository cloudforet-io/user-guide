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

\*\*\*\*

**STEP 1. Log in Azure Portal &gt; Resource groups** 

![](../../.gitbook/assets/image%20%28104%29.png)

**STEP 2. Click `Access control (IAM)` Navigation tab, and click `+Add` button.**

![](../../.gitbook/assets/image%20%28102%29.png)



**STEP 3: Assign the `Reader role`  to the account. The account should  have an access permission in this resource group.**



![](../../.gitbook/assets/image%20%28103%29.png)




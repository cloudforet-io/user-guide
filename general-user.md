---
description: >-
  General user can manage resources by creating a project under the project
  group and registering a cloud account(service account) to created project.
---

# General User

## Sign-in

**STEP 1:** Drive to domain of **SpaceONE** on browser ****and type given ID and Password.

![](.gitbook/assets/signin_as_user2.png)

\*\*\*\*

## Create My Project Group and Project

{% hint style="info" %}
**General User** has a permission to control only the project group which they belong to. 
{% endhint %}

**STEP 1:** Drive to menu **`Project`** at top bar and click **`+ Create`** button as below.

![](.gitbook/assets/screen-shot-2021-02-05-at-14.43.06.png)

\*\*\*\*

**STEP 2:** Name **`Group`** at top bar and click **`+ Create`** button as below.

![](.gitbook/assets/create_project_group_spaceone.png)

**STEP 3:** Select Project Group that you created in previous step and Click **`+ Create Project`** at top right corner of page and then name project and then click **`Confirm`** button. \(sample case: **SpaceONE-DEV**\)

![](.gitbook/assets/create_project_spaceone_dev.png)

**STEP 4:**  Click **`+ Create Project`** at top right corner of page and then name project with different name for your own use and then click **`Confirm`** button. \(sample case: **SpaceONE-PRO**\)

![](.gitbook/assets/create_project_spaceone_prd.png)

**STEP 5:**  Check 2 sample Projects \(**SpaceONE-DEV, SpaceONE-PRO**\) have created under **SpaceONE** project group. 

desc 

![](.gitbook/assets/list_spaceone_projects.png)

## Register Service Account

Service accounts must be registered to run collectors which getting cloud resources from public clouds.

  
**STEP 1:** Drive to menu **`Identity > Service Account`** from top bar and Click AWS from provider panel.  
Click **`+ Add`** button to add AWS service account. 

![](.gitbook/assets/select_service_account_as_aws.png)

**STEP 2:** Fill out name of Service account and Account ID on base information fields. Please, fill our your **AWS Access Key** and **AWS Secret Key** as well. 

{% hint style="info" %}
Please, Click links at Help for AWS Users panel if you have the troubles to get account id, assume role, or AWS access key. 
{% endhint %}

![](.gitbook/assets/screen-shot-2021-02-05-at-15.54.03.png)

**STEP 3:** Please, Select a project that you want to map with your service account. \(Optional\).   
We highly recommend to map a project with service account for cloud resource management purpose.

![](.gitbook/assets/attach_account_to_project.png)

All cloud resources under service account that you registered above will be shown on selected project and  I**nventory** menu.

## Collect Resources

**STEP 1: Drive to Plugin &gt; Collector Menu** 

![](.gitbook/assets/collect_data.png)

\*\*\*\*


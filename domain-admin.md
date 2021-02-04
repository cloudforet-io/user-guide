---
description: >-
  The role of Domain Admin creates the top-level project group, creates users,
  and sets the main collector.
---

# Domain Admin

## Sign-in

**STEP 1:** Drive to domain of **SpaceONE** on browser ****and type given ID and Password as domain admin.  
**\(**E-mail received from the Root Account has stated detailed the connection methods; Single Sign On\(SSO\),  ID/PW, or Google Oauth2**\)**

![](.gitbook/assets/screen-shot-2021-02-04-at-14.39.08.png)

## Create Project Group

All cloud resources **MUST** belong to a certain project for management purpose. You can grouping any projects with Project Group.   
Domain Admin creates the project group based on company's management policy.

{% hint style="info" %}
**Note&gt;** General User **\(Project Admin\)** creates projects only under project group with permission to manage cloud resources.   
{% endhint %}

**STEP 1:** Drive to menu **`Project`** at top bar and click **`+ Create Group button`** at top right corner of panel.

![](.gitbook/assets/create_top_project_group.png)

**STEP 2:** Type project group name \(**sample case: Landing Zone**\) and Click Confirm.

![](.gitbook/assets/create_project_group_landingzone.png)

**STEP 3:** Type project group name \(**sample case: Services**\) and Click Confirm.

![](.gitbook/assets/create_project_group_services.png)

**STEP 4:** Type project group name \(**sample case: Business Support Systems**\) and Click Confirm.

![](.gitbook/assets/create_project_group_businesssupportsystems.png)

**STEP 5:** Check all 3 project groups has created a tree on left menu.

![](.gitbook/assets/show_project_page.png)

## Create User

Create general user and assign the project groups to created user. General users can access only to the project group which they are belonged to.

**STEP 1:** Drive to menu **`Identity > User`** at top bar. 

![](.gitbook/assets/screen-shot-2021-02-04-at-14.16.22.png)

  
**STEP 2:** Click **`+ Add`** button to add a domain Admin user.

![](.gitbook/assets/screen-shot-2021-02-04-at-14.18.45.png)

**STEP 3:** Fill out all required fields ****and click **`Confirm`** button once finish.

![](.gitbook/assets/create_user1%20%281%29.png)

**STEP 4:** Drive to Project ****and Click member icons at right next to **`+ Create Project`** button.

![](.gitbook/assets/screen-shot-2021-02-04-at-16.28.10.png)

**STEP 5:** Fill out all required fields ****and click **`Confirm`** button once finish.

![](.gitbook/assets/add_user2_to_project_group.png)

\*\*\*\*

**STEP 3:** 

\*\*\*\*

![](.gitbook/assets/check_user2_role.png)

## Collect Collectors

desc



![Create collectors](.gitbook/assets/create_collector.png)



### **Create AWS EC2 Collector**

**STEP 1:** 

![](.gitbook/assets/select_aws_ec2_plugin.png)

**STEP 2:**

![](.gitbook/assets/create_aws_ec2_collector.png)

### **Create AWS Cloud Services Collector** 

**STEP 1:** 

![](.gitbook/assets/select_aws_cloud_services_plugin.png)

\*\*\*\*

**STEP 2:** 

![](.gitbook/assets/create_aws_cloud_services_collector.png)

\*\*\*\*

### **Create AWS  Trusted Advisor Collector** 

**STEP 1:** 

![](.gitbook/assets/select_aws_cloud_services_plugin%20%281%29.png)

**STEP 2:** 

![](.gitbook/assets/create_aws_trusted_advisor_collector.png)

\*\*\*\*

### **Create AWS Health Dashboard Collector** 

**STEP 1:** 

![](.gitbook/assets/select_aws_cloud_services_plugin%20%281%29.png)

\*\*\*\*

**STEP 2:** 

![](.gitbook/assets/create_aws_personal_health_dashboard_collector.png)

\*\*\*\*

### **Create AWS Metric Collector** 

**STEP 1:**

![](.gitbook/assets/select_aws_cloud_services_plugin%20%281%29.png)

**STEP 2:** 

![](.gitbook/assets/create_spaceone_monitoring_metric_collector.png)



desc

![](.gitbook/assets/list_all_collectors.png)

## Update Schedule

desc

**STEP 1:** 

![](.gitbook/assets/select_schedule_tab.png)

**STEP 2:** 

 ****

![](.gitbook/assets/add_schedule_to_collector.png)

![](.gitbook/assets/list_collector_schedules.png)

\*\*\*\*

\*\*\*\*


---
description: Quick Guide for user easier to set up Power Scheduler
---

# Power Scheduler Quick Start

![](../.gitbook/assets/pw_img.png)

## How to Set up

Start your Power Scheduler after completing the following steps: 

* [Prerequisites](power-scheduler-quick-start.md#prerequisites)
* [Set up Basic Scheduler Info](power-scheduler-quick-start.md#set-up-basic-scheduler-info)
* [Configure Scheduler Runtime](power-scheduler-quick-start.md#configure-scheduler-runtime)
* [Define Resource Group](power-scheduler-quick-start.md#define-resource-group)

## Prerequisites

You can set up your IAM policy for power scheduler in SpaceONE with pre-defined credentials per cloud-provider to control resources with safety and prevent others to access resources without permission.

Please, assign corresponding access policies to SpaceONE from each provider's console as mentioned below, prior to create a Power Scheduler.

{% page-ref page="../identity/service-account/service-account-policy-management.md" %}

{% page-ref page="../identity/service-account/google-cloud-service-account-policy-management.md" %}



## Set up Basic Scheduler Info

**STEP 1:** Select `Automation` &gt; `Power Scheduler` on top header menu 

![Select Power Scheduler on menu](../.gitbook/assets/image%20%283%29.png)



**STEP 2:** Select a project to set up Power Scheduler on the dashboard. 

![Select a Project on Dashboard](../.gitbook/assets/image%20%2871%29.png)





**STEP 3:**  Click `+ 새 스케줄러 만들기` button at the top left corner. It is automatically changed to the creation mode if there is no previously created scheduler in the project.

![&#xC0C8; &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xB9CC;&#xB4E4;&#xAE30;](../.gitbook/assets/image%20%2822%29.png)





**STEP 4:**  Set the scheduler's name to create a scheduler. You can enter a string including letters and  `-` . Scheduler name is required and blank spaces are not allowed.

![](../.gitbook/assets/image%20%2842%29.png)

### 



## Configure scheduler runtime

![set a time schedule to apply](../.gitbook/assets/image%20%2841%29.png)

Set the time for applying a scheduler.   
  
The calendar grid breaks the week down by day on the horizontal axis and has 24-hour basis segments in portrait orientation.  You can click`이번주` button to set the scheduled time for this week.  

You can move between month through  `< >` at the upper right of the graph. 



There are three types of scheduler mode.

|  Mode | State | Description | Color |
| :---: | :---: | :--- | :---: |
| Repeated Schedule |  | Timer repeated by every weeks. Selected area became On, Otherwise\(Non selected\) became Off. | ![](../.gitbook/assets/image%20%288%29.png) |
| One Time Schedule | ON | Created specified time range. Resource became On selected area. | ![](../.gitbook/assets/image%20%2816%29.png) |
|  | OFF | Created specified time range. Resource became Off selected area. | ![](../.gitbook/assets/image%20%2855%29.png) |



**STEP 1:** Click /drag  to select certain time segments to set time for the scheduler to run.

![Scheduler calendar mouse Click / drag](../.gitbook/assets/image%20%2819%29.png)

> **Please, be advised**   
> Without any setting, it recognizes scheduler as `모두 끄기`all off, which causes all resource to stop working.

## Define Resource Group

Set the resource group for applying defined schedule  

![](../.gitbook/assets/image%20%2840%29.png)

By clicking _**+ Add Group**_ Button. User can move to creating resource group. 

![](../.gitbook/assets/image%20%2834%29.png)

Name Limit

Limitation of Resource Group name is below.

> * Total 128 character 
> * Start with character
> * Character, Number, & Hyphen`-`  available



Selecting resource type. Available types are below

`[ALL] Server / [AWS] RDS / [AWS] Auto Scaling Group`

![](../.gitbook/assets/image%20%2846%29.png)



Entering all information, Then click save button below to save schedule. 

![Save](../.gitbook/assets/image%20%284%29.png)

Scheduler _**creating success**_ message pops up. If all creation process is successful. 

![Pop up](../.gitbook/assets/image%20%2811%29.png)

![Describes created schedule](../.gitbook/assets/image%20%2824%29.png)



## 

> ### " Happy Power Scheduling! "




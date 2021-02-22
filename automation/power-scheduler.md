---
description: Managing Power Status of Cloud Resources in projects
---

# Power Scheduler

## Overall

In Power Scheduler page, User can schedule power status of target cloud resources. 

Power Scheduler page offers listing scheduler information, add/update/delete scheduler.

## Prerequisites

User need to define security policy\(IAM\) before setup power scheduler. 

Before creating Power Scheduler modify your existing policy, For detailed process refer to link below.

{% page-ref page="../identity/service-account/service-account-policy-management.md" %}

{% page-ref page="../identity/service-account/google-cloud-service-account-policy-management.md" %}



## Power Scheduler Dashboard

![](../.gitbook/assets/image%20%2812%29.png)

**Scheduler list by Projects**

User can see Overall status of power scheduling 

**Search Bar**

User can search status of power scheduling by project name.

**Scheduling Dashboard** 

Items of power scheduler information for each projects are below.

![&#xC2A4;&#xCF00;&#xC904; Dashboard](../.gitbook/assets/image%20%2863%29.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Item</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Project Name</td>
      <td style="text-align:left">Name of projects which is linked to power scheduler</td>
    </tr>
    <tr>
      <td style="text-align:left">Number of Resource</td>
      <td style="text-align:left">
        <ul>
          <li>Number of resources : Number of resources that are controlled by power
            scheduler.</li>
          <li>Number of resources available : Total number of resources can be scheduled
            by power scheduler (Server, RDS, Auto Scaling Group).</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Schedule</td>
      <td style="text-align:left">List of running schedule(Up to 3 items)</td>
    </tr>
    <tr>
      <td style="text-align:left">Estimated Reduced Cost</td>
      <td style="text-align:left">Reduced cost by power scheduler in last 1 months(US dollar).</td>
    </tr>
    <tr>
      <td style="text-align:left">Scheduled Job</td>
      <td style="text-align:left">Length of each schedule</td>
    </tr>
  </tbody>
</table>

> **Scheduling Meat Map**
>
> The color of scheduling head map has 2 steps. The color shows how long is scheduled job. Each color means below

> ![](../.gitbook/assets/image%20%2858%29.png)Scheduled time is between 0 ~ 12 hours

> ![](../.gitbook/assets/image%20%2847%29.png)Scheduled time is between 12~24 hours

## Scheduler Management

### Scheduler Calendar

In scheduler Calendar, User can manage this functions



#### Scheduling Time

![weekly calendar](../.gitbook/assets/image%20%2828%29.png)

User can see scheduler timetable. x-axis is date, y-axis is time to be controlled. By clicking _**This weeks**_ jump to power scheduling plan for this weeks.

Move to next/previous weeks by  `< >` buttons right upper side of table.



#### Resource Group

**• Priority by Resource Group**

![](../.gitbook/assets/image%20%289%29.png)

Scheduler is consist of several resource group. Each resource group has step defined by priority.

The lower number gets higher priority. The status change of higher priority finishes first. If the target status is _**ON**_, higher priority _**Resource Group**_ start first. 

Create/Deleting _**Resource Group**_ is done by clicking _**Edit button &gt; + Add Group**_.  

**Resource Groups In Same Priority**

![](../.gitbook/assets/image%20%2857%29.png)

There is sequence of changing status between resource groups in same priority.

Upper position resource group changes first, and Lower position goes second.



_**Details of Resource Group**_

![](../.gitbook/assets/image%20%2852%29.png)

Detailed status resource group is done by clicking _**Name of Resource Group.**_

| Item | Description |
| :--- | :--- |
| Name | Name of Resource Group |
| Resource Type | Type of Resource Group\(Instance, RDS, Autoscaling\) |
| Target List | List of Cloud Resources to be controlled |

### 

### Creating New Scheduler



![&#xC0C8; &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC0DD;&#xC131; &#xD398;&#xC774;&#xC9C0;](../.gitbook/assets/image%20%2850%29.png)

By Clicking _**Creating New Scheduler**_ button, New scheduler editing screen appears. 

If there is no existed scheduler, Creation screen is auto generated.

To create schedule, fill out several items required.



#### Name

Name of Schedule. 

Combination of String, Number, '-' is valid. escape character is not available. 

#### Timestamp

Specifying time for scheduler, x-axis is date, y-axis is detailed time.    

Selecting range of times done by click & drag in calendar.

Schedule has two mode.

| Scheduled mode | State | Description | color |
| :--- | :--- | :--- | :--- |
| Repeated Schedule |  | Repeated by every weeks. Within selected area, Resources are On, Otherwise\(Non selected\) resources became Off. | ![](../.gitbook/assets/image%20%288%29.png) |
| One time | ON | Event time for specific date. At the selected area, resources became on.  | ![](../.gitbook/assets/image%20%2816%29.png) |
| One time | OFF | Event time for specific date. At the selected area, resources became off. | ![](../.gitbook/assets/image%20%2855%29.png) |



#### Resource Group

Creating resource groups to control.

By _**Creating Resource Group**_ button, _**Creating Resource Group Page**_ Pops up.

Informations to be specified are belows

<table>
  <thead>
    <tr>
      <th style="text-align:left">Item</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">
        <p>Enter <em><b>Resource Group</b></em> name.</p>
        <p>Total 128 character is available.</p>
        <p>Name should start with character(not number).</p>
        <p>Name can be a combination of charcter, number, &apos;-&apos;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Resource Type</td>
      <td style="text-align:left">
        <p>Select resource type. Available list of resource group is belows.</p>
        <p>
          <img src="../.gitbook/assets/image (17).png" alt/>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Resource List</td>
      <td style="text-align:left">Target Cloud Resources to be controlled. Selected by search filter.</td>
    </tr>
  </tbody>
</table>

Confirm the input information, then click _**save**_ button.

### Schedule Deletion

![](../.gitbook/assets/image.png)

By clicking _**Trash Can**_ ****button, Scheduler can be deleted.

### Scheduler Edit

<table>
  <thead>
    <tr>
      <th style="text-align:left">item</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Scheduler Name</td>
      <td style="text-align:left">
        <p>By Clicking <em><b>Scheduler Edit</b></em> button right upper of page. Scheduler
          name can be edited.</p>
        <p></p>
        <p>
          <img src="../.gitbook/assets/image (38).png" alt/>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Scheduler Calendar</td>
      <td style="text-align:left">
        <p>By clicking Edit button in calendar. One time schedule, Repeated time
          scheduled can be edited.</p>
        <p>
          <img src="../.gitbook/assets/image (66).png" alt/>
        </p>
        <p></p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Resource Group</td>
      <td style="text-align:left">
        <p><em><b>Resource Group</b></em> can be edited <em><b>edit</b></em> button
          below.</p>
        <p>
          <img src="../.gitbook/assets/image (33).png" alt/>
        </p>
        <p></p>
      </td>
    </tr>
  </tbody>
</table>



## Limitation & Restrictions

Some limitations for power scheduler service are existed, Most of them are inherited from functionality of each cloud providers.

### AWS

Cloud resources which has conditions below can not managed by power scheduler service

* AutoScalingGroup
  * ASG controlled by _**EKS managed group**_
* RDS Instance
  * Instance that member of _**replication**_
  * SQL DB using _**Multi-AZ**_
* RDS Aurora Instance
  * Member of _**Aurora global database**_
  * Cluster that using _**parallel query feature**_
* Other case
  * Does not have stop/start functions






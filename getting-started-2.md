---
description: Quick Guide for first-time users to get started with SpaceONE.
---

# A Compass To SpaceONE Universe Traveler

## How to Start  <a id="overview"></a>

You need little steps to follow to get start on 

* [**User Registr**](getting-started-2.md#adding-user)[**ation**](getting-started-2.md#adding-user)\*\*\*\*
* [**Create a Project**](getting-started-2.md#creating-project)\*\*\*\*
* [**Register Service Account**](getting-started-2.md#creating-service-account)\*\*\*\*
* [**Collect Cloud Resource** ](getting-started-2.md#discovering-cloud-resource)

## User Registration <a id="adding-user"></a>

### Log-in as domain administrator

SpaceONE service assigns a domain per company, and you can access through this assigned domain.  
You will receive log-in ID and password since you applied services.

\(We guide applying process for spaceONE service on certain channels while CBT period\)

![spaceONE console login screen](.gitbook/assets/2020-07-31-3.42.25.png)

               Click 'Sign in root account credentials' button at the bottom to sign-in as domain administrator.

![](.gitbook/assets/2020-07-31-3.43.11.png)

                               Sign in with given ID/Password from SpaceONE service administrator. 

![Domain Administrator Sign-in screen](.gitbook/assets/2020-07-31-3.44.00.png)

### Add a new common user account

Let's add a user in the domain. You can sign into SpaceONE with created user account to proceed to next.

**Step 1:** Click Identity &gt; User on top of Global Navigation Bar

![](.gitbook/assets/2020-07-31-3.46.38.png)

  
**Step 2:** Click ' + Create'  button to add user in your group.   
It's the first time to sign-in as  below, and therefore no user is on list.

![User &amp;gt; Create &#xD074;&#xB9AD;&#xD558;&#xAE30;](.gitbook/assets/2020-07-31-3.48.11.png)

**Step 3:** ID is required fields, and **must** entered in **e-mail** format. For other items, refer to the example below.

Click 'check user id' to check the duplicate name after entering the user name

![User registration screen](.gitbook/assets/2020-07-31-3.50.40.png)

**STEP 4:** Please, sign in with registered user above after sign out 

![&#xC0AC;&#xC6A9;&#xC790; Profile &#xD654;&#xBA74;](.gitbook/assets/2020-07-31-3.52.50.png)

Please, refer to the IDENTITY&gt; USER page for more detailed user management functions.

{% page-ref page="identity/user.md" %}



### Sign in as a common user

Now, let's sign in as the added user and try SpaceONE service.   
  
**STEP 1:** Click 'Sign in with Google' button and select account that was added previously.

![](.gitbook/assets/2020-08-03-11.07.25.png)

You will see an empty dashboard if you sign in first time with added user. Because you don't have any data yet. :-\)

![Domain Dashboard &#xCD5C;&#xCD08; &#xD654;&#xBA74;](.gitbook/assets/2020-08-03-11.12.14.png)

Now let's collect Cloud Resources through SpaceONE.   
Create a your first project with 'Get Started' button.

## Creating a Project   <a id="creating-project"></a>

You can create a _project_ after creating a _Project Group_. 

**STEP 1:** Click '_Create_' button at right next to Project Group to create a project group.

![Project Group &#xC0DD;&#xC131; &#xBC84;&#xD2BC;](.gitbook/assets/2020-08-03-11.18.38.png)

**STEP 2:** Type as below to create a Project Group

![Project Group creation window screen ](.gitbook/assets/2020-08-03-11.20.02.png)

**STEP 3:** Click '_Create Project'_ button to create a project __after select created Project Group.

![](.gitbook/assets/2020-08-03-11.31.43.png)

Project creation window appears as below. Create a project by entering the project name.

![Project creation screen](.gitbook/assets/2020-08-03-11.33.06.png)

Project setting is completed as shown below. 

![Project &#xAD00;&#xB9AC; &#xD654;&#xBA74;](.gitbook/assets/2020-08-03-11.37.38.png)

Please refer to the IDENTITY&gt; Project page for more detailed project management functions. 

Now, let's set up a Service Account. 



## Creating a Service Account <a id="creating-service-account"></a>

Enter Credentials\(APIKey Pair\) to collect Cloud Resource.   
The example service account registration in the Getting Started Guide is based on AWS.

**STEP 1:** Click '_+ Add_' button once selected Identity &gt; Service Account &gt; AWS. 

![](.gitbook/assets/2020-08-03-3.39.10.png)

**STEP 2:** Enter all required fields to add an AWS Service Account in the Add Service Account input form as shown below.

Items marked in red are required fields. The rest of the items aren't mandatory. You can skip optional fields.

![](.gitbook/assets/2020-08-03-3.50.06.png)

**STEP 3:** Select a project in the Project item, and then click the 'Save' button at the bottom, once you fill out all required fields. 

![Service Account &#xC0DD;&#xC131; &#xD398;&#xC774;&#xC9C0; &#xB0B4;&#xC758; Project &#xC120;&#xD0DD; &#xD654;&#xBA74;](.gitbook/assets/2020-08-03-3.47.38.png)

Now you can collect cloud resources by creating a Collector if AWS service account is successfully registered.   
  
Please refer to the link below for more information on Service Account.

{% page-ref page="identity/service-account/" %}

## Collecting Cloud Resources <a id="discovering-cloud-resource"></a>

### Creating Collector

Drive to Plugin &gt; Collector. It is normal for a blank screen to appear as there is no Collector installed when sign in for the first time

**STEP 1:** Select a Collector with clicking '+ Create' button.  

![](.gitbook/assets/2020-08-03-4.18.54.png)

You can find Collector List that can be installed in _**Official MarketPlace**_ as shown below.  
We will proceed to install _**aws-ec2**_ Collector at this time. 

**STEP 2:** Click ****_**aws-ec2**_ collector's '+ create' button. 

![collector &#xC0DD;&#xC131; &#xD654;&#xBA74;](.gitbook/assets/2020-08-03-4.19.39.png)

The Collector Creation Wizard appears on the screen as shown below.

You can name collector and select its version. Other fields don't need to edit by any chance. It is created by entering the name and clicking Confirm.

**STEP 3:** Enter name and then click ****collector's 'confirm' button. 

![Collector setting screen](.gitbook/assets/2020-08-03-4.22.39.png)

You can also create an AWS-Cloud-Service Collector with same process as well.   
You can find collectors on the list once you created.

![](.gitbook/assets/2020-08-03-4.33.11.png)

### 

### Execute Collector 

Now let's collect Cloud Resources.

**STEP 1:** Select the collector created earlier and click '**Action &gt; Collect Data'** to view the Collect Data screen as shown below. Click Confirm to start collecting.

![Collect Data &#xC120;&#xD0DD;&#xD654;&#xBA74;](.gitbook/assets/2020-08-03-4.42.48.png)

![Collector &#xC2E4;&#xD589;&#xD654;&#xBA74;](.gitbook/assets/2020-08-03-4.41.59.png)

You can find current status of the running Collector on the **Domain Dashboard&gt; Collection** screen as follows.

![Collector Running screen](.gitbook/assets/2020-08-03-4.46.13.png)

Collecting process takes approximately 3 minutes to complete. You can find the collected resources at Inventory&gt; Server, Cloud Service, if the collection is completed successfully. 

![Collected Cloud Resource info](.gitbook/assets/2020-08-03-4.51.30.png)

Please refer to the Plugin&gt; Collector page, for further details on Collector.

{% page-ref page="plugin/collector.md" %}



## Next 

So far, you have completed the basic setup to use SpaceONE. 

On next, we will look up each function in details.

  


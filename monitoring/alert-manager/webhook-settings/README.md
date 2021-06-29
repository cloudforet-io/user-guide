---
description: Set up a Webhook for Alert Manager
---

# Webhook Settings

## Overview

**`Webhook`** is based on the **`Project`**  page that allows you the following actions:

* **Set up the Alert Webhook.** 
* **Set up Notification Policy** : View, and Edit 
  * Notification Policy
  * Auto Recovery
  * Event Rule
* **Escalation Policy**

![](../../../.gitbook/assets/screen-shot-2021-06-28-at-10.37.24.png)

Once you Set Escalation Policy you can dealing with Webhook for following Actions

* \*\*\*\*[**Adding Webhook \(Get Webhook URL\)**](./#adding-webhook-get-webhook-url)\*\*\*\*
* \*\*\*\*[**Webhook list**](./#webhook-list)\*\*\*\*

**You can Set Webhook URL for AWS, Grafana, and more**

{% page-ref page="aws-sns.md" %}

{% page-ref page="grafana.md" %}

## Adding Webhook \(Get Webhook URL\)

To set up a **Webhook** for alert and notification requires appropriate url to retrieve from monitoring systems such as AWS SNS, Grafana, etc. 

**STEP 1. Log in SpaceONE &gt; Project &gt; Alert tab**

Go to Project's Alert Tab and Click **`Activate Alert`**  button and then you will see Activate Alert Success 

![](../../../.gitbook/assets/screen-shot-2021-06-28-at-10.45.04.png)

![](../../../.gitbook/assets/screen-shot-2021-06-28-at-10.46.16.png)

**STEP 2. Alert &gt; Webhook &gt; `+ Add`**

![](../../../.gitbook/assets/screen-shot-2021-06-28-at-11.17.17.png)

**STEP 3. Name Webhook, Select Type of Webhook & Version and Click  `Confirm` Button**

{% hint style="info" %}
**Please, Select the latest Version of Webhook  
Latest version automatically will be selected if you click version drop-down.**   
{% endhint %}

**STEP 4. Check registered Webhooks on the list.**

![](../../../.gitbook/assets/screen-shot-2021-06-28-at-13.40.53.png)

## Webhook List

**All Created Webhook list is Alert Tabs Per Project.**

![](../../../.gitbook/assets/screen-shot-2021-06-29-at-16.11.37.png)

{% hint style="info" %}
All **Webhook URLs** that Created through **SpaceONE** is **HTTPS** but **HTTP** works as well**.   
  
Please,** type ****URL ****as **HTTP  like if you need to set url as HTTP `http://monitoring-webhook.dev.spaceone.dev/monitoring/v1/webhook/...`**
{% endhint %}


---
description: >-
  Quick Guide for user to set up Monitoring Metric Collectors for Servers over
  Clouds
---

# Metric Collector Quick Start

## How to Set up

Collect monitoring configured metric data after completing following steps:

* [Prerequisites](power-scheduler-quick-start.md#prerequisites)
* [Get API Key from Billing Service Provider](billing-quick-start.md#get-api-key-from-billing-service-provider)
* [Register Billing Service Account](billing-quick-start.md#register-billing-service-account-ex-hyper-billing)
* [Billing Information](billing-quick-start.md#billing-information)

## Prerequisites

Monitoring Metric Collector requires SpaceOne Service Account to collect various vendor includes AWS, Google Cloud, Azure, etc. 

## Get API Key for Monitoring Metric Collector \(SpaceONE\)

Before adding  Service Account \(SpaceONE\), you needs API Key for SpaceONE. 

{% hint style="info" %}
**We currently provide API-Key via administrator only.   
Please, contact your domain administrator of SpaceONE If you don't have a API-Key for SpaceONE service account or send an e-mail for more support \(**_**support@spaceone.dev**_**\)**
{% endhint %}

## Register SpaceOne Service Account \(Ex. Hyper Billing\)

To register billing service account, you can do in Identity &gt; Service Account.

Select **Hyper Billing** Service Provider, then click **Add**

![Register Billing ServiceAccount](../.gitbook/assets/image%20%2877%29.png)

{% hint style="info" %}
**If you have no "Hyper Billing" in the Service Providers, contact Domain Administrator of SpaceONE.**
{% endhint %}

Register Billing Service Account like following steps,

1. name of service account
2. Put Credentials \(API Key\)
3. Select Project

![1. name of service account](../.gitbook/assets/image%20%2879%29.png)

After set name of service account, you have to configure Credentials which is received from Billing Service Provider. In this example you can get Credentials from Megazone Hyperbilling team.

They will give you Credentials which are consisted with "Account", "Email" and "Key". Put the information correctly.

![2. Credentials \(API Key\)](../.gitbook/assets/image%20%2874%29.png)

{% hint style="info" %}
Assigning Project is mandatory for Billing Service.

DO NOT SKIP THIS STEP.
{% endhint %}

![3. Select Project](../.gitbook/assets/image%20%2875%29.png)

If you have multiple billing account, repeat "Register Billing Service Account".


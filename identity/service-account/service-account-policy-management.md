---
description: >-
  Details of API Security policy to use SpaceONE Power Scheduler service
  (AWS/Google Cloud)
---

# Service Account Policy Management

## Service Account Policy

Before create Service Account, User can modify your existing API policy

This will guarantee isolation your resource from other non power-scheduled items. Also prevent malfunction from mis configuration of power scheduling.



## Collector 

Collector do not need to have authority other than read permission. So we strongly recommend to restrict its permission to **read only access**. 

Otherwise, User can add more restrictions like regional and resource base. One of the useful example is to restrict its rights within region.

In order to experience powerful function of SpaceONE collectors. Use the managed _**ReadOnly policy**_ is preferred. In case of internal regulations, create a policy below then attach when creating API user.



{% tabs %}
{% tab title="AWS" %}
```text

```
{% endtab %}

{% tab title="GCP" %}
```

```
{% endtab %}
{% endtabs %}

 



## Power Scheduler

Suggested IAM policy for each cloud provider to use _**SpaceONE Power Scheduler**_ service are below.



{% tabs %}
{% tab title="AWS" %}
```text

```
{% endtab %}

{% tab title="GCP" %}
```text

```
{% endtab %}
{% endtabs %}




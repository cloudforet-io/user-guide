---
description: Details of API Security policy to use SpaceONE plugin
---

# \(AWS\) Service Account Policy Management

## Service Account Policy

Before create Service Account, User can modify your existing API policy.

This will guarantee isolation your resource from other non power-scheduled items. Also prevent malfunction from mis configuration of power scheduling.

To Create API for each use case. follow directions below

* [General Collector](service-account-policy-management.md#how-to-create-readonly-policy-in-aws)
* [Power Scheduler Service](service-account-policy-management.md#powerscheduler)
* [Personal Health Dashboard/Trusted Advisor Collector](service-account-policy-management.md#aws-personal-health-dashboard-trusted-advisor)

## General Collector 

Collector do not need to have authority other than read permission. So we strongly recommend to restrict its permission to **read only access**. 

Otherwise, User can add more restrictions like regional and resource base. One of the useful example is to restrict its rights within region.

In order to experience powerful function of SpaceONE collectors. Use the managed _**ReadOnly policy**_ is preferred. 



**Step 1. Log in AWS Console &gt; IAM** 

Go to IAM &gt; Users &gt; Add user

![](../../.gitbook/assets/aws_service_account_policy_iam_add_user.png)

\*\*\*\*

**Step 2. Set User Details**

Enter _**User name**_, Set access type to _**Programmatic access**_

![](../../.gitbook/assets/aws_service_account_set_user_details.png)



**Step 3. Set API Permission**

Set Permission to ReadOnlyAccess\(Managed Policy\)

Click _**Attach existing policies directly**_ . Enter _**readonly**_ keyword in policy search bar.

Select _**ReadOnlyAccess**_ managed policy as below.

![](../../.gitbook/assets/aws_service_account_set_permissions.png)

\*\*\*\*

**Step 4. Add tags**

_**You can skip this process**_ and move to next. 

SpaceONE collector does not related to tags in IAM. 

![](../../.gitbook/assets/aws_service_account_iam_add_tag.png)





_**Step 5. Review**_

Check the details you added. Then click _**Create users**_ right down of page

![](../../.gitbook/assets/aws_service_account_iam_review.png)

_**Step 6. Copy Key Pair**_

IAM key pair created, _**Be sure to copy the Access key ID/Secret access key and keep it safely**_.

If you skip to copy, there is no chance to have it again\(Do from step 1 again\).

![](../../.gitbook/assets/aws_service_account_iam_add_user_copy_keypair.png)





### To Create Policy Directly

In case of internal regulations, create a policy below then attach when creating API user. 

{% tabs %}
{% tab title="AWS" %}
```text

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "acm:Describe*",
                "acm:Get*",
                "acm:List*",
                "acm-pca:Describe*",
                "acm-pca:Get*",
                "acm-pca:List*",
                "apigateway:GET",
                "autoscaling:Describe*",
                "autoscaling-plans:Describe*",
                "autoscaling-plans:GetScalingPlanResourceForecastData",
                "athena:List*",
                "athena:Batch*",
                "athena:Get*",
                "cassandra:Select",
                "cloudfront:Get*",
                "cloudfront:List*",
                "cloudwatch:Describe*",
                "cloudwatch:Get*",
                "cloudwatch:List*",
                "connect:List*",
                "connect:Describe*",
                "connect:GetFederationToken",
                "directconnect:Describe*",
                "dynamodb:BatchGet*",
                "dynamodb:Describe*",
                "dynamodb:Get*",
                "dynamodb:List*",
                "dynamodb:Query",
                "dynamodb:Scan",
                "ec2:Describe*",
                "ec2:Get*",
                "ec2:SearchTransitGatewayRoutes",
                "ec2messages:Get*",
                "ecr:BatchCheck*",
                "ecr:BatchGet*",
                "ecr:Describe*",
                "ecr:Get*",
                "ecr:List*",
                "ecs:Describe*",
                "ecs:List*",
                "eks:Describe*",
                "eks:List*",
                "elasticache:Describe*",
                "elasticache:List*",
                "elasticfilesystem:Describe*",
                "elasticloadbalancing:Describe*",
                "es:Describe*",
                "es:List*",
                "es:Get*",
                "es:ESHttpGet",
                "es:ESHttpHead",
                "health:Describe*",
                "iam:Generate*",
                "iam:Get*",
                "iam:List*",
                "iam:Simulate*",
                "kafka:Describe*",
                "kafka:List*",
                "kafka:Get*",
                "lambda:List*",
                "lambda:Get*",
                "rds:Describe*",
                "rds:List*",
                "rds:Download*",
                "redshift:Describe*",
                "redshift:GetReservedNodeExchangeOfferings",
                "redshift:View*",
                "route53:Get*",
                "route53:List*",
                "route53:Test*",
                "route53domains:Check*",
                "route53domains:Get*",
                "route53domains:List*",
                "route53domains:View*",
                "route53resolver:Get*",
                "route53resolver:List*",
                "s3:Get*",
                "s3:List*",
                "secretsmanager:List*",
                "secretsmanager:Describe*",
                "secretsmanager:GetResourcePolicy",
                "sns:Get*",
                "sns:List*",
                "sns:Check*",
                "sqs:Get*",
                "sqs:List*",
                "sqs:Receive*",
                "storagegateway:Describe*",
                "storagegateway:List*",
                "tag:Get*",
                "trustedadvisor:Describe*",
                "workspaces:Describe*"
            ],
            "Effect": "Allow",
            "Resource": "arn:aws:*:{aws region code}:*:*"
        }
    ]
}
```
{% endtab %}
{% endtabs %}

 

## PowerScheduler

Suggested IAM policy for each cloud provider to use _**SpaceONE Power Scheduler**_ service are below.



**Step 1. Create Policy**

Go to IAM &gt; Policies &gt; Create policy

![](../../.gitbook/assets/aws_service_account_iam_power_scheduler_create_policy.png)

\*\*\*\*

**Step 2. Attach Policy Definitions**

Move to JSON tab, attach policy definition below. Then click _**Review policy**_

![](../../.gitbook/assets/aws_service_account_powerscheduler_attach_policy_definitions.png)

{% tabs %}
{% tab title="AWS" %}
```text
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "dynamodb:UpdateGlobalTableSettings",
                "dynamodb:TagResource",
                "dynamodb:UpdateTable",
                "dynamodb:UpdateGlobalTable",
                "rds:StartDBCluster",
                "rds:StopDBCluster",
                "rds:StopDBInstance",
                "rds:StartDBInstance",
                "rds:AddTagsToResource",
                "rds:RebootDBInstance",
                "rds:RemoveTagsFromResource",
                "ec2:StartInstances",
                "ec2:StopInstances",
                "ec2:RebootInstances",
                "ec2:DeleteTags",
                "ec2:CreateTags",
                "autoscaling:SetDesiredCapacity",
                "autoscaling:UpdateAutoScalingGroup",
                "autoscaling:CreateOrUpdateTags",
                "support:DescribeTrustedAdvisorCheckRefreshStatuses",
                "support:DescribeTrustedAdvisorCheckResult",
                "support:DescribeTrustedAdvisorChecks"
            ],
            "Resource": "*"
        }
    ]
}
```
{% endtab %}
{% endtabs %}



**Step 3. Review Policy** 

Enter policy name and description, Then click _**Create policy**_

![](../../.gitbook/assets/aws_service_account_powerscheduler_review_policy.png)



**Step 4. Log in AWS Console &gt; IAM** 

Go to IAM &gt; Users &gt; Add user

![](../../.gitbook/assets/aws_service_account_policy_iam_add_user.png)



**Step 3. Set User Detail** 

Enter _**User name**_, Set access type to _**Programmatic access**_

![](../../.gitbook/assets/aws_service_account_set_user_details.png)

\*\*\*\*

**Step 4. Set API Permission**

 Add all policies below. They should included to guarantee successful action.

* AmazonDynamoDBReadOnlyAccess 
* AmazonEC2ReadOnlyAccess 
* AmazonRDSReadOnlyAccess 
* AutoScalingReadOnlyAccess
* **Policy created in step 3**

![](../../.gitbook/assets/aws_service_account_powerscheduler_set_api_permission.png)



**Step 5. Review**

Make sure all the permission from Step 4. included, Then click _**Create user**_

![](../../.gitbook/assets/aws_service_account_powerscheduler_review.png)



_**Step 6. Copy Key Pair**_

IAM key pair created, _**Be sure to copy the Access key ID/Secret access key and keep it safely**_.

If you skip to copy, there is no chance to have it again\(Do from step 1 again\).

![](../../.gitbook/assets/aws_service_account_iam_add_user_copy_keypair.png)







## AWS Personal Health Dashboard/Trusted Advisor

To use aws advanced collector like AWS _**Personal Health Dashboard/Trusted Advisor**_ 

User account support level should be over business and additional IAM policy need to be attached.





```text
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "support:*"
            ],
            "Resource": "*"
        }
    ]
}
```

 






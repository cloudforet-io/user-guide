---
description: Details of service account policies to use SpaceONE plugin
---

# \(Alibaba Cloud\) Service Account Policy Management

## Service Account Policy

**SpaceONE** highly recommends to set appropriate permissions to **Service Account** for each purpose. 

Please, Set service account, To Create API for each use case:

* [General Collector](alibaba-cloud-service-account-policy-management.md#general-collector)

In case of internal regulations, create a policy below then attach when creating API user. 

* [Overall IAM Policy Superset](alibaba-cloud-service-account-policy-management.md#overall-iam-policy-superset)

## General Collector 

Collector requires appropriate authorities to collect cloud resources. We strongly recommend to limit collector's service account its permission to **read only access**. 

Otherwise, you can add more restrictions per resources or actions. One of the useful example is to restrict its rights.

**STEP 1. Create RAM users**

1. Log on to the [RAM console](https://ram.console.aliyun.com/) by using your Alibaba Cloud account.
2. In the left-side navigation pane, click `Users` under `Identities`.
3. Click `Create User`.
   * To create multiple RAM users at a time, click `Add User`.
4. Specify the _**Logon Name**_ and _**Display Name**_ parameters.
5. Click **`OK`** _****_and return to _Create User screen_.

![](../../.gitbook/assets/alicloud_general_step2%20%281%29.png)

**STEP 2. Create AccessKey pairs for RAM users**

You need AccessKey pairs to enter Alibaba Cloud Credentials in the SpaceOne. If you have authorized a RAM user under your Alibaba Cloud account to manage their own AccessKey pairs, the RAM user can create an AccessKey pair in the RAM console.

1. In the left-side navigation pane, click `Users` under `Identities`.
2. In the User Logon Name/Display Name column, click the username of the _**target**_ RAM user.
3. In the User AccessKey Pairs section, click `Create AccessKey`.
   * You must enter a verification code if you are creating an AccessKey pair for the first time.
4. Click `OK`.
   * The AccessKey Secret is displayed only once when you first create it. You cannot retrieve the AccessKey Secret if you forget it. We recommend that you save the AccessKey Secret for subsequent use.
   * If the AccessKey pair is disclosed or lost, you must create a new one. Currently, you can create a maximum of two AccessKey pairs.

![](../../.gitbook/assets/image%20%28100%29.png)

**STEP 3: Authorize RAM users to access data as read-only.**

1. In the left-side navigation pane, click `Users` under `Identities`.
2. In the User Logon Name/Display Name column, click the username of the _**target**_ RAM user.
3. Click `Add Permissions`. On the page that appears, the principal is automatically filled in.
4. In the Policy Name column, select `ReadOnlyAccess` policy for its _**System Policy**_.
   * You can click X in the section on the right side of the page to delete the selected policy.
5. Click `OK`.
6. Click `Complete`.
7. You will return to _Create User screen_, and can check you _**AccessKey ID**_ and _**AccessKey Secret**_. Alibaba Cloud generates AccessKey Pair by default when you create a user. Click **`Copy`** to copy your authentication information. Go to step 5 if you miss this step.

![](../../.gitbook/assets/image%20%28101%29.png)

**STEP 4: Generate Your AccessKey Pair. \(optional\)**

Go to [RAM Console](https://ram.console.aliyun.com/) &gt; Identities &gt; Users &gt; Choose the user you created for General Collector.

Click **`Create AccessKey`** in the _Authentication_ tap.

![](../../.gitbook/assets/image%20%2898%29.png)

You will receive _Create AccessKey popup_, and click **`Copy`** below the blue box to copy your _**AccessKey Pair**_ information. Click **`Close`** to close the popup window.

![](../../.gitbook/assets/image%20%2895%29.png)

## Overall IAM Policy Superset

If user can use managed policy, Refer to policy below. 

_**Region Code**_ in Resource parameter need to be changed. _**AWS Region Code**_ or _**\***_  character is available.

```text

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "GeneralReadOnlyPolicyForCollectors",
            "Effect": "Allow",
            "Resource": "arn:aws:*:{aws region code}:*:*"
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
            ]
        },
        {
            "Sid": "PowerSchedulerController",
            "Effect": "Allow",
            "Resource": [
                "arn:aws:ec2:{aws region code}:*:instance/*",
                "arn:aws:rds:{aws region code}:*:db:*",
                "arn:aws:rds:{aws region code}:*:cluster:*",
                "arn:aws:autoscaling:{aws region code}:*:autoScalingGroup:*"
            ],
            "Action": [
                "rds:StartDBCluster",
                "rds:StopDBCluster",
                "rds:StartDBInstance",
                "rds:StopDBInstance",
                "rds:RebootDBInstance",
                "ec2:StartInstances",
                "ec2:StopInstances",
                "ec2:RebootInstances",
                "autoscaling:SetDesiredCapacity",
                "autoscaling:UpdateAutoScalingGroup"
            ]
        },
        {
            "Sid": "PHDandTACollector",
            "Effect": "Allow",
            "Resource": "*",
            "Action": [
                "support:DescribeAttachment",
                "support:DescribeCaseAttributes",
                "support:DescribeCases",
                "support:DescribeCommunications",
                "support:DescribeIssueTypes",
                "support:DescribeServices",
                "support:DescribeSeverityLevels",
                "support:DescribeSupportLevel",
                "support:DescribeTrustedAdvisorCheckRefreshStatuses",
                "support:DescribeTrustedAdvisorCheckResult",
                "support:DescribeTrustedAdvisorChecks",
                "support:DescribeTrustedAdvisorCheckSummaries",
                "support:SearchForCases"
            ]
        }        
    ]
}
```






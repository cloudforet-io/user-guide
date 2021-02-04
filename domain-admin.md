# Domain Admin

## Log-in

**`Domain Admin`** 은 일반 Log-in 페이지를 통해 Log-in 합니다. **`Root Account`**에게서 받은 이메일에 ID/Password 또는 Google Oauth2와 같은 Single-Sign-On 방식의 접속정보가 명시되어 있습니다.

**`Domain Admin`** 은 최상위 프로젝트 그룹을 만들고, 사용자를 생성하며, 주요 **`Collector`**를 설정합니다.



**STEP 1: `Domain Admin`Role 이 부여된 User로 Log-in 합니다.** 

![](.gitbook/assets/login_user1.png)

## Create Project Group

SpaceONE의 모든 자원은 특정 **`Project`**에 소속되어 있습니다. 또한,  **`Project Group`**은 **`Project`**를 그룹화합니다. 

Domain Admin은 회사의 관리 정책에 따라서 최상위 **`Project Group`**을 생성합니다. 

{% hint style="info" %}
**`Project`** 생성 권한은 **`Project Admin`**으로 지정된 **`General User`** 에게 있습니다. 
{% endhint %}



**STEP 1: 상단 Navigation에서 Project 선택 후, `Landing Zone`라는 이름으로 `Project Group`을 생성합니다.** 

![](.gitbook/assets/create_top_project_group.png)



![](.gitbook/assets/create_project_group_landingzone.png)



**STEP 2: `Services` 라는 이름으로 `Project Group`을 생성합니다.**

![](.gitbook/assets/create_project_group_services.png)

**STEP 3: `Business Support System` 이라는 `Project Group`을 생성합니다.** 

![](.gitbook/assets/create_project_group_businesssupportsystems.png)

**STEP 4: SpaceONE console의 좌측 navigation 에서 생성된 `Project Group`을 확인할 수 있습니다.**

![](.gitbook/assets/show_project_page.png)

## Create User

일반 사용자를 생성하여 **`Project Group`**에 할당합니다. 

{% hint style="info" %}
일반 사용자는 자신이 소속된 **`Project Group`** 의 리소스에만 접근 가능합니다. 
{% endhint %}



**STEP 1: Project Admin 사용자를 추가합니다.** 

![](.gitbook/assets/create_user1%20%281%29.png)

\*\*\*\*

**STEP 2: User를 Services 프로젝트 그룹에 매핑합니다.**

![](.gitbook/assets/add_user2_to_project_group.png)

**STEP 3: User Management 화면에서 Role과 Authorization Type이 매핑된 것을 확인할 수 있습니다.**

![](.gitbook/assets/check_user2_role.png)

## Collect Collectors

**`Collector`**는 AWS, Google Cloud, Azure 등 클라우드 서비스의 자원을 수집하는 Plugin입니다. 

**`Domain Admin`**이 **`Collector`**에 대한 정보를  설정합니다. 



SpaceONE 상단 navigation의 **`Plugin` -`Collector`** 를 선택한 후, **`Create`** 버튼을 클릭해 Collector를 생성합니다.

![Create collectors](.gitbook/assets/create_collector.png)



### **AWS EC2 Collector 생성**

**STEP 1: Market place 에서 `aws-ec2` 플러그인을 선택합니다.**

![](.gitbook/assets/select_aws_ec2_plugin.png)

**STEP 2: AWS EC2 `collector` 를 생성합니다.**

![](.gitbook/assets/create_aws_ec2_collector.png)

### **AWS Cloud Services Collector 생성**

**STEP 1: Market-place 에서 `aws-cloud-services` 플러그인을 선택합니다.**

![](.gitbook/assets/select_aws_cloud_services_plugin.png)

\*\*\*\*

**STEP 2: AWS Cloud Service Collector 를 생성합니다.** 

![](.gitbook/assets/create_aws_cloud_services_collector.png)

\*\*\*\*

### **AWS  Trusted Advisor Collector 생성**

**STEP 1: Market-place 에서 `aws-cloud-services` 플러그인을 선택합니다.**

![](.gitbook/assets/select_aws_cloud_services_plugin%20%281%29.png)

**STEP 2: AWS trusted advisor `collector`를 생성합니다.** 

![](.gitbook/assets/create_aws_trusted_advisor_collector.png)

\*\*\*\*

### **AWS Health Dashboard Collector 생성**

**STEP 1: Market-place 에서 `aws-cloud-services` 플러그인을 선택합니다.**

![](.gitbook/assets/select_aws_cloud_services_plugin%20%281%29.png)

\*\*\*\*

**STEP 2: AWS Personal Health Dashboard `collector`를 생성합니다.** 

![](.gitbook/assets/create_aws_personal_health_dashboard_collector.png)

\*\*\*\*

### **AWS Metric Collector 생성**

**STEP 1: Market-place 에서 `aws-cloud-services` 플러그인을 선택합니다.**

![](.gitbook/assets/select_aws_cloud_services_plugin%20%281%29.png)

**STEP 2: Spaceone-Monitoring Metric `Collector`를 생성합니다.** 

![](.gitbook/assets/create_spaceone_monitoring_metric_collector.png)



생성된 전체 **`collector`** 목록을 확인합니다.

![](.gitbook/assets/list_all_collectors.png)

## Update Schedule

Schedule 설정을 통해, 생성된 **`Collector`** 들의 수집주기를 설정하고 주기적으로 클라우드 자원을 수집합니다.   



**STEP 1: Schedule을 설정하고 싶은 `Collector`를 선택한 뒤, 하단 `Schedule` 탭의 `Add` 버튼을 클릭합니다.** 

![](.gitbook/assets/select_schedule_tab.png)

\*\*\*\*

**STEP 2: 매 4시간 마다 수집하는 `Collector`를 생성합니다.**

 ****

![](.gitbook/assets/add_schedule_to_collector.png)

![](.gitbook/assets/list_collector_schedules.png)

\*\*\*\*

\*\*\*\*


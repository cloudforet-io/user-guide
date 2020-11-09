---
description: 각 Cloud Provider의 Credential 정보를 관리 합니다.
---

# Service Account

## 둘러보기

Service Account 페이지를 통해 사용자는 다양한 Provider에서 제공하는 Credential을 편리하게 관리할 수 있습니다. 이 정보를 바탕으로 Multi Cloud Resource 정보를 수집 합니다. 

![Service Account &#xAD00;&#xB9AC; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-4.34.53-2%20%281%29.png)

페이지 내에서 사용자는 아래의 작업이 가능 합니다. 

* Service Account 추가
* Service Account 삭제/Project 변경
* AWS Console로 링크
* 상세 조회 및 관리



현재 SpaceONE에서 지원하는 service provider는 다음과 같습니다. 

* AWS
* Google Cloud
* Microsoft Azure
* MEGAZONE
* SpaceONE

## Service Account 추가

Cloud Provider를 선택한 후 _**+ Add**_ 버튼을 클릭하여 Service Account를 새로 추가할 수 있습니다. 

사용자 가이드 에서는 AWS의 IAM을 중심으로 살펴 봅니다. 

Service Account 입력 페이지에서는 \* 로 표기된 항목을 입력하면 간단히 추가가 가능합니다. 

### Base Information

![Ser](../../.gitbook/assets/2020-08-07-5.44.58.png)

* Name : Service Account의 이름을 입력 합니다. 
* Account ID : AWS의 Account ID 정보를 입력 합니다.\(12자리의 숫자로 표시됩니다.\)
* Tag : Service Account의 Tag 정보를 편집 합니다.

### Credentials

SpaceONE에서는 두가지 타입의 Service Account를 지원 합니다. \(aws\_access\_key, aws\_assume\_role\)

각 타입별 입력 항목은 아래와 같습니다.

#### aws\_access\_key  

![aws access key &#xBC29;&#xC2DD;&#xC758; key &#xC785;&#xB825; &#xD3FC;](../../.gitbook/assets/2020-08-07-5.48.28.png)

* Region\(Option\) : 수집 대상인 Region 정보를 입력 합니다. 입력하지 않을 경우 모든 region으로부터 cloud resource를 스캔 합니다. 
* AWS Access Key\(Required\) : IAM의 Access Key를 입력 합니다. 주로  Read Only IAM 계정을 별도 생성하여 입력 합니다.  
* AWS Secret Key\(Required\) : 위에서 입력한 IAM의 Secret key를 입력 합니다. 

#### aws\_assume\_role

![aws\_assume\_role &#xBC29;&#xC2DD;&#xC758; &#xC785;&#xB825; &#xD3FC;](../../.gitbook/assets/2020-08-07-5.53.33.png)

* Region\(Option\) : 수집 대상인 Region 정보를 입력 합니다. 입력하지 않을 경우 모든 region으로부터 cloud resource를 스캔 합니다. 
* AWS Access Key\(Required\) : Assume 받는 IAM 계정의 Access Key를 입력 합니다. 
* AWS Secret Key\(Required\) : Assume 받는 IAM 계정의 Secret Key를 입력 합니다. 
* Role ARN\(Required\) : IAM에서 생성한 Assume Role의 Role ARN 정보를 입력 합니다. 

### Project 선택

Service Account가 속할 Project를 지정합니다. 지정하게 되면, 해당 Service Account에서 수집한 Cloud Resource 정보는 자동으로 Project에 연결되게 됩니다. 

![Project &#xC120;&#xD0DD; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-6.02.19.png)

* Project 생성이 필요할 경우 _**+ Create Project**_ 버튼을 클릭하여 필요한 Project Group/Project를 생성한 후 진행 합니다. Project 생성에 대한 자세한 링크는 아래 페이지를 참고하세요.

{% page-ref page="../../project/project-group-management.md" %}

* 원하는 Project를 선택한 후 _**Save**_ 버튼을 클릭하여 Service Account의 생성 작업을 완료 합니다. 
* Project를 지정하지 않고 싶은 경우 _**Select no Project**_를 선택 합니다. Project는 나중에 다시 지정이 가능 합니다. 

## Service Account 삭제/Project 변경

Service Account를 삭제 하거나/기존에 지정했던 Project를 변경 합니다. 

대상 Service Account를 선택 후 _**Action**_ 메뉴를 클릭한 후 _**Delete**_ 혹은 _**Change Project**_를 선택 합니다. 

![Service Account &#xC0AD;&#xC81C;/&#xBCC0;&#xACBD; &#xBA54;&#xB274;](../../.gitbook/assets/2020-08-07-6.17.37.png)

#### Service Account 삭제

아래와 같이 Service Account 삭제 화면에서 Service Account 이름을 입력한 후 _**Confirm**_ 을 클릭하여 삭제가 가능합니다.   

![Service Account &#xC0AD;&#xC81C; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-6.21.27.png)

#### Project 변경

아래와 같이 Change Project 화면에서 변경하고자 하는 Project를 지정한 후 _**Confirm**_을 클릭하여 삭제가 가능합니다. 

![Project &#xBCC0;&#xACBD; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-6.22.47.png)

## AWS Console로 링크 

대상 Service Account를 선택 후 _**Action**_ 메뉴를 클릭한 후 _**Console**_을 선택 합니다. 

AWS의 콘솔 링크로 이동 합니다. 사전에 AWS Console에 로그인이 되어 있거나, 로그인을 해야 해당 IAM Account로 이동할 수 있습니다. 



## 상세 조회 및 관리

상세 관리 탭을 통해  Service Account의 상세 정보 확인/Tag 관리/Credential 관리/Member 관리가 가능 합니다. 

#### Detail 

Service Account의 Meta 정보를 확인할 수 있습니다.

![Service Account &#xC0C1;&#xC138;&#xC870;&#xD68C;](../../.gitbook/assets/2020-08-07-6.33.27.png)

#### Tag

_**Edit**_ 버튼을 클릭해서 Service Account의 Tag를 추가/삭제할 수 있습니다. 

![Tag &#xCD94;&#xAC00;/&#xC0AD;&#xC81C; ](../../.gitbook/assets/2020-08-07-6.54.13.png)

#### Credentials

Service Account 에서 Key 정보를 보관하고 있는 Credential 을 추가하거나 삭제할 수 있습니다.

####  




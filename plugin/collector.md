---
description: 'Collector를 생성하고, Cloud Resource를 수집합니다.'
---

# Collector

## 둘러보기 

SpaceONE은 Collector Plugin을 통하여 다양한 서비스의 Cloud Resource 수집이 가능 합니다. 

Plugin은 Official Marketplace를 통하거나, 자체 제작한 Plugin을 사용할 수 있습니다. 

![Collector &#xAD00;&#xB9AC; &#xD398;&#xC774;&#xC9C0;](../.gitbook/assets/2020-08-06-7.48.58-.png)



## Collector 생성 

아래 화면과 같이 Official Marketplace를 선택하면, 사용 가능한 plugin list가 조회 됩니다. 

설치 하고 싶은 Plugin을 선택하고, 화면 내 _**+ Create**_ 버튼을 클릭 하는 것으로 Collector 생성을 시작할 수 있습니다. 

![Collector Plugin &#xC120;&#xD0DD; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-10.23.39.png)

Collector의 이름만 입력 후 다른 부분은 Default 값으로 두셔도 무방 합니다. Plugin 버전을 선택 가능하나, 주로 latest로 합니다. 

![Collector &#xC0DD;&#xC131; &#xD654;&#xBA74; \#1](../.gitbook/assets/2020-08-07-11.10.04.png)

Collector가 사용할 Credentials 정보를 선택 합니다. 기존에 사용중인 Credentials 정보를 제외 하여 자동으로 mapping 해주므로, _**Availability**_ 항목이 정상으로 표시된 경우 다음 화면으로 넘어갑니다. 

![Collector &#xC0DD;&#xC131; &#xD654;&#xBA74; \#2](../.gitbook/assets/2020-08-07-11.10.58.png)

Tag 입력 화면입니다. Collector에 Tag 입력이 필요하다면 추가하고 아니라면 _**Confirm**_ 을 입력하여 생성을 완료 합니다. 

![Collector &#xC0DD;&#xC131; &#xD654;&#xBA74; \#3](../.gitbook/assets/2020-08-07-11.14.05.png)

만약 생성이 정상적으로 진행되지 않는다면, Collector 생성 화면내 붉은색으로 표시된 순서가 있는지 확인 해야 합니다. 

![](../.gitbook/assets/2020-08-07-11.16.29.png)



## Collector 변경/삭제/활성화/비활성화

생성을 제외한 collector 작업은 Action 리스트 메뉴를 통해서 가능 합니다. Collector를 선택한 후 Action 버튼을 클릭하게 되면 아래와 같이 작업 가능한 리스트가 조회 됩니다.

![Collector &#xB9AC;&#xC2A4;&#xD2B8; &#xBA54;&#xB274;](../.gitbook/assets/2020-08-07-11.18.32.png)

#### 변경 

변경 사항을 수정한 후 _**Confirm**_ 버튼을 클릭하여 완료 합니다. 

![Collector &#xBCC0;&#xACBD; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-11.20.18.png)

#### 삭제 

아래와 같이 삭제 팝업이 보이게 되는데, _**Confirm**_ 으로 진행 합니다. 

![Collector &#xC0AD;&#xC81C; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.06.46.png)

#### 활성화

_**DISABLE**_ 상태인 Collector를 _**ENABLE**_ 상태로 변경 합니다. Cloud Resource 수집 작업이 가능 해집니다.

![Collector &#xD65C;&#xC131;&#xD654; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.10.04.png)



#### 비활성화 

Collector를 _**DISABLE**_로 변경 하여 Cloud Resource 수집 작업이 일어나지 않게 설정할 수 있습니다.

![Collector &#xBE44;&#xD65C;&#xC131;&#xD654; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.09.45.png)



## Collector 조회/상세조회



![](../.gitbook/assets/2020-08-07-2.16.13.png)

Collector 리스트에서는 아래와 같은 정보 확인이 가능 합니다. 

* Name : Collector의 이름
* State : Enable/Disable 상태로 구분하여, Collector의 사용 여부를 결정 합니다. 
* Priority : 다수의 Collector로 부터 수집된 정보가 중복 되었을 경우, 우선순위를 결정 합니다. Priority가 낮을수록 우선순위가 높습니다.
* Last Collected : Collector가 구동된 마지막 시간을 기록 합니다.
* Created : Collector가 생성된 시간을 기록 합니다. 

Collector의 상세 동작은 하단 탭에서 관리 가능 합니다. 



### Detail

Collector의 상세 설정을 나타냅니다. 

Collector가 수집하는 데이터의 Filter를 조회할 수 있습니다.

![Collector Detail &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.25.22.png)

### Tag

Collector의 Tag를 관리할 수 있습니다. _**Edit**_ 버튼을 클릭하여 Tag 를 편집할 수 있습니다.

![Tag &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.27.56.png)

편집 화면에서 _**Add Tag**_ 버튼과 _**x**_ 버튼을 사용하여 추가/삭제 할 수 있습니다.  편집이 완료된 후 우측 하단의 _**Save**_ 버튼을 통해 편집을 완료 합니다. 

![Tag &#xD3B8;&#xC9D1; &#xD398;&#xC774;&#xC9C0;](../.gitbook/assets/2020-08-07-3.25.03.png)

### Credentials

Collector가 사용하는 인증 정보를 나타 냅니다. 해당 인증 정보는 SpaceONE의 Service Account와 연결 됩니다. 

_**Collect Data**_ 버튼을 클릭하여 해당 Credentials로 Cloud Resource의 즉시 수집이 가능 합니다. 

![Credential &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-3.28.14.png)

![Cloud Resource &#xC989;&#xC2DC; &#xC218;&#xC9D1;](../.gitbook/assets/2020-08-07-3.34.33.png)

### Schedules

Collector가 데이터를 수집하는 주기를 지정 합니다. 

Schedule 지정시 매일 지정된 시간에 Collector를 통한 Cloud Resource 수집이 이루어집니다. 

![Collector Schedule &#xAD00;&#xB9AC; &#xD0ED;](../.gitbook/assets/2020-08-07-3.39.39.png)

**추가** 

+ Add 버튼을 클릭할 경우 스케쥴 추가 화면이 나타납니다. 

이름/Timezone/수집 시간을 선택할 수 있습니다. 

Collecting Time은 24시간 기준으로 지정하고 1시간 단위로 선택 가능합니다. 

![Collector Schedule &#xCD94;&#xAC00; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-3.46.11.png)

#### 스케쥴 변경, 삭제

스케쥴을 선택 후 _**Action**_ **&gt; Update/Delete** 버튼을 통해 기존 스케쥴을 변경하거나 삭제가 가능합니다.   

![Collector Schedule &#xBCC0;&#xACBD;](../.gitbook/assets/2020-08-07-3.58.22.png)



## Cloud Resource 수집

Collector를 통하여 원하는 시점에 Cloud Resource 수집이 가능 합니다. 사용자는 다양한 방식으로 Project 내의 Inventory 데이터가 최신화 될 수 있도록 할 수 있습니다. 

### 즉시수집

Collector를 선택 후 _**Action &gt; Collect Data**_ 메뉴를 클릭하여 수집 합니다. 

![Collect Data &#xBA54;&#xB274;](../.gitbook/assets/2020-08-07-4.02.39.png)

아래와 같이 Collect Data 화면이 출력 되는데, _**Confirm**_ 버튼을 클릭하여 수집을 시작 합니다. 

![&#xC989;&#xC2DC; &#xC218;&#xC9D1; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-4.03.34.png)

Collect가 진행중인 상황은 Main Dashboard에서 확인 가능합니다. 화면이 자동으로 Refresh 되지 않으므로, 주기적으로 화면내 _**Reload**_ 버튼을 클릭합니다. 

![Collector &#xC218;&#xC9D1; &#xC9C4;&#xD589;&#xC0C1;&#xD669;](../.gitbook/assets/2020-08-07-4.04.46.png)

### 스케쥴 수집  

위의 _**Schedules**_ 에  등록된 일정으로 SpaceONE 내부에서 자동으로 Cloud Resource 수집을 진행 합니다. 

최종 수행 시간을 Collector 리스트에서 확인할 수 있습니다. 

![Schedule &#xCD5C;&#xC885; &#xC218;&#xD589;&#xC2DC;&#xAC04; &#xD655;&#xC778;](../.gitbook/assets/2020-08-07-4.08.17-.png)

 


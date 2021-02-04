---
description: Creating Collector. Collecting Cloud Resources.
---

# Collector

## Overview

With _**Collector Plugins**_ in SpaceONE marketplace, Cloud resources from various cloud providers can be collected easily.

Plugins are offered by both SpaceONE Official marketplace and private repository.

![](../.gitbook/assets/2020-08-06-7.48.58-.png)



## Create Collector

Available plugin list is printed by select _**Official Marketplace.**_

Select plugin to install, Click _**+ Create**_ button will starts collector creation wizard.

![](../.gitbook/assets/2020-08-07-10.23.39.png)

Fill out name of collector and choose version of plugin. Higher plugin version is generally suggested.

![](../.gitbook/assets/2020-08-07-11.10.04.png)

Selecting credentials information for collector. This step will be done automatically.

![](../.gitbook/assets/2020-08-07-11.10.58.png)

User can add tags for collector. Tags can be added by clicking _**+ Add**_ button

You don\`t need to delete existing tags\(For system use\)

![](../.gitbook/assets/2020-08-07-11.14.05.png)

If creation is not proceeds, Check red marked steps in _**Collector creation wizards**_

![](../.gitbook/assets/2020-08-07-11.16.29.png)



## Collector Update/Delete/Enable/Disable

Controlling _**Collector**_ can be done by _**Action**_ list menu. 

Select _**Collector**_ then click _**Action button**_. Available list of actions will be shown.

![](../.gitbook/assets/2020-08-07-11.18.32.png)

#### Update 

Change items to be updated, then click _**Confirm**_ button. 

![](../.gitbook/assets/2020-08-07-11.20.18.png)

#### Delete 

Deletion pop up will be printed, Proceeds through _**Confirm**_ button

![](../.gitbook/assets/2020-08-07-2.06.46.png)

#### Enable

Changing Collector status from _**DISABLE**_ status to _**ENABLE**_. This allows collecting job with _**collector.**_

![](../.gitbook/assets/2020-08-07-2.10.04.png)



#### DISABLE 

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

 


---
description: Quick Guide for user easier to set up Power scheduler
---

# Power Scheduler Quick Start

## How to Set up

You can start your Power Scheduler after completing following steps: 

* [Prerequisites](power-scheduler-quick-start.md#prerequisites)
* [Set up Basic Scheduler Info](power-scheduler-quick-start.md#set-up-basic-scheduler-info)
* [스케줄러 작동 시간 설정하기](power-scheduler-quick-start.md#undefined-1)
* [리소스 그룹 정의하기](power-scheduler-quick-start.md#undefined-2)

## Prerequisites

You can set up your IAM policy for power scheduler in SpaceONE with pre-defined credentials per cloud-provider to control over resources with safety and prevent other to access resources without permissions.

Please, assign corresponding access policies to SpanceONE from each provider's console as mentioned below, prior to create a Power Scheduler.

{% page-ref page="../identity/service-account/service-account-policy-management.md" %}

## Set up Basic Scheduler Info

**STEP 1:** Select `Automation` &gt; `Power Scheduler` on top header menu 

![Select Power Scheduler on menu](../.gitbook/assets/image%20%283%29.png)



**STEP 2:** Select a project to set up power scheduler on dashboard. 

![Select a Project on Dashboard](../.gitbook/assets/image%20%2871%29.png)





**STEP 3:**  Click `+ 새 스케줄러 만들기` button at top left corner. It is automatically changed to the creation mode if there is no previously created scheduler in the project.

![&#xC0C8; &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xB9CC;&#xB4E4;&#xAE30;](../.gitbook/assets/image%20%2822%29.png)





**STEP 4:** 스케줄러 생성을 위해 스케줄러의 이름을 설정합니다. 문자와 `-` 를 포함한 문자열을 입력할 수 있습니다. 띄어쓰기가 불가합니다. 스케줄러 이름은 입력 필수 항목으로, 누락 시 스케줄러가 생성되지 않습니다.  

![](../.gitbook/assets/image%20%2842%29.png)

### 



## 스케줄러 작동 시간 설정하기

![&#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC801;&#xC6A9; &#xC2DC;&#xAC04; &#xC124;&#xC815;](../.gitbook/assets/image%20%2841%29.png)

스케줄러가 적용되는 시간을 설정합니다. Calendar의 가로축은 날짜, 세로축은 스케줄러가 적용될 시간입니다. `이번주` 버튼을 클릭하면 이번주의 스케줄 시간을 설정할 수 있습니다.  

그래프 오른쪽 상단의 `< >` 를 통해 달을 이동할 수 있습니다. 



스케줄에는 3가지의 scheduled mode가 있습니다.

| Scheduled mode | State | Description | color |
| :--- | :--- | :--- | :--- |
| 반복 스케줄 |  | 매주 반복되는 타이머로 선택된 영역은 resource가 켜지며, 해제된 영역은 resource가 꺼집니다.  | ![](../.gitbook/assets/image%20%288%29.png) |
| 1회성 스케줄 | 켜기 | 특정 날짜에 생성되는 일회성 타이머로, 선택된 영역은 resource가 켜집니다. | ![](../.gitbook/assets/image%20%2816%29.png) |
|  | 끄기 | 특정 날짜에 생성되는 일회성 타이머로, 선택된 영역에서 resource가 꺼집니다.  | ![](../.gitbook/assets/image%20%2855%29.png) |



마우스를 클릭 / 드래그 해서 스케줄러가 작동할 시간을 설정합니다.

![&#xC2A4;&#xCF00;&#xC904;&#xB7EC; calendar &#xB9C8;&#xC6B0;&#xC2A4; &#xD074;&#xB9AD; / &#xB4DC;&#xB798;&#xADF8;](../.gitbook/assets/image%20%2819%29.png)

> 설정이 없으면 `모두 끄기`로 인식되어 리소스의 작동이 멈추게 되므로 주의해야 합니다.

## 리소스 그룹 정의

스케줄러를 적용할 리소스 그룹을 정의합니다. 

![](../.gitbook/assets/image%20%2840%29.png)

`+ 그룹 추가` 버튼을 클릭해 리소스 그룹 만들기 페이지로 이동해 스케줄러를 적용할 리소스 그룹의 이름을 입력합니다.

![](../.gitbook/assets/image%20%2834%29.png)

리소스 그룹의 이름을 입력할 때의 제약사항은 다음과 같습니다

> * 최대 128자 입력 가능 \(리소스그룹 카드에는 16자까지 표기\)
> * 문자로 시작
> * 문자, 숫자 및 `-`  사용 가능



리소스 타입을 선택합니다. 리소스 타입이란 스케줄러를 통해 on-off 를 적용하고 싶은 리소스 종류이며, 리소스 그룹을 구분하는 기준이 됩니다. 

현재 SpaceONE power scheduler 에서 지원하는 리소스 타입은 

`[ALL] Server / [AWS] RDS / [AWS] Auto Scaling Group`의 3가지입니다. 

![](../.gitbook/assets/image%20%2846%29.png)



모든 정보를 입력한 후 페이지 오른쪽 하단의 저장 버튼을 눌러 스케줄러 정보를 저장합니다. 

![&#xC800;&#xC7A5; &#xBC84;&#xD2BC;](../.gitbook/assets/image%20%284%29.png)

모든 정보가 알맞게 저장된 경우 스케줄러 생성 완료 팝업이 뜨며 

![&#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC0DD;&#xC131; &#xC644;&#xB8CC; &#xD31D;&#xC5C5;](../.gitbook/assets/image%20%2811%29.png)

![&#xC0DD;&#xC131;&#xD55C; &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC815;&#xBCF4; &#xD655;&#xC778;](../.gitbook/assets/image%20%2824%29.png)

생성한 스케줄러의 정보 조회 페이지로 이동합니다.

## 

> ### " Happy Power Scheduling! "




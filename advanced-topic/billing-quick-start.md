---
description: 쉽고 빠르게 Billing 서비스를 설정하기 위한 Quick Guide 입니다.
---

# Billing Quick Start

## 전체 순서

Billing 서비스를 사용하기 위해서는 아래와 같은 절차가 필요 합니다.   

* [Prerequisites](billing-quick-start.md#prerequisite)
* [API Key 를 얻기](billing-quick-start.md#api-key)
* [Billing Service Account를 등록](billing-quick-start.md#billing-service-account-ex-hyper-billing)
* [Billing 정보 조회하기](billing-quick-start.md#undefined-1)

## 사전 준비 <a id="prerequisite"></a>

Billing 정보는 AWS, Google Cloud, Azure 혹은 Hyperbilling을 통해 제공 됩니다.

Billing 서비스를 enable 하기 위해서는 SpaceONE의 도메인 관리자에게 문의 해야 합니다.   

{% hint style="info" %}
1.5.3 버전 이후로는 Hyperbilling backend 가 자동으로 enable 됩니다. 
{% endhint %}

Billing backend가 지원되는 버전은 아래와 같습니다. 

| Version | Backend |
| :--- | :--- |
| 1.5.3 | Hyperbilling for AWS |

  

## API key 를 얻기  

Billing Service Account 추가하기 위해 API Key가 필요 합니다. 각 벤더에 필요한 API Key를 문의 하세요.  

Billing 백앤드 담당자 연락처는 아래와 같습니다. 

| Backend | Contact |
| :--- | :--- |
| Hyperbilling for AWS | MEGAZONE CLOUD \(Innoworks Team\) |

## Billing Service Account를 등록 \(Ex. Hyper Billing\)

Billing Service Account는 Identity &gt; Service Account에서 가능 합니다. 

Hyper Billing Service Provider를 선택 한 후, 'Add' 버튼을 클릭 하세요. 

![Register Billing ServiceAccount](../.gitbook/assets/image%20%2877%29.png)

{% hint style="info" %}
**Service Provider에서 Hyper Billing 버튼이 조회되지 않는 경우, SpaceONE의 Domain 관리자에게 문의 하세요.**
{% endhint %}

Billing Service Account는 아래와 같은 순서로 생성 합니다.

1. Service Account 이름
2. Credential 입력 \(API Key\)
3. Project 선택

![1. Service Account &#xC774;&#xB984;](../.gitbook/assets/image%20%2879%29.png)

Service Account 이름을 설정 한 이후에는 Billing Service Provider 로 부터 전달 받은 Credential 정보를 입력 해야 합니다. 이번 예제에서는 Megazone Cloud의 Hyperbilling Team 으로부터 전달 받았습니다. 

전달 받은 값은 "Account", "Email", "Key" 값으로, 각 항목에 맞는 데이터를 정확히 입력 합니다.    

![2. Credential &#xC785;&#xB825;\(API Key\)](../.gitbook/assets/image%20%2874%29.png)

{% hint style="info" %}
Project를 등록 하는것은 Billing Service의 필수 항목 입니다. 

해당 절차를 Skip 하면 안됩니다.
{% endhint %}

![3. Project &#xC120;&#xD0DD;](../.gitbook/assets/image%20%2875%29.png)

If you have multiple billing account, repeat "Register Billing Service Account".

여러개의 Billing 계정을 가지고 있는 경우, [Billing Service Account를 등록](billing-quick-start.md#billing-service-account-ex-hyper-billing) 절차를 반복 합니다. 

## Billing 정보 조회하기 

모든 설정이 완료 되었습니다. 이제 Main Dashboard 와 Project Page에서 Billing 정보를 조회할 수 있습니다.    

도메인 내 모든 Billing의 통합 정보는 Main Dashboard를 통해 조회 할 수 있습니다. 이것은 각각의 Billing 계정 내용의 합계로 제공합니다. 

![Domain&#xC758; Billing &#xD1B5;&#xACC4;](../.gitbook/assets/image%20%2878%29.png)

Project Dashboard에서는 각 Project 별 사용중인 Billing 정보를 제공 합니다. 

![Project &#xBCC4; Billing &#xD1B5;&#xACC4;](../.gitbook/assets/image%20%2873%29.png)


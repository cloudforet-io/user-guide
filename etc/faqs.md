---
description: 스페이스원에 대해 자주 문의되는 사항들을 정리 했습니다.
---

# FAQs



## Identity 

Project/인증/권한관련 문의

#### Q. 스페이스원의 사용자 권한 Role 은 어떤 종류가 있나요?

권한은 Managed Role과 Custom Role을 가지고 있습니다.  

기본적으로 사용자가 편리하게 설정할 수 있는 Managed Role의 경우 Root Account, Domain Admin, Project Admin 을 가지고 있습니다. 

Custom Role의 경우 사용자가 SpaceONE의 각 기능에 대한 권한을 자유롭게 설정 가능하나, SpaceONE console로는 설정이 불가능 하고, spacectl을 통해 자체 설정 및 사용자에게 Role 할당을 해야 합니다. 



#### Q. Managed Role별로 구체적으로 할 수 있는 일은 어떤것이 있나요?

* Root Account : 최초 도메인 생성시 함께 생성되는 계정으로 도메인내의 모든 자원에 대한 접근이 가능, 모든 계정 생성 및 권한 변경이 가능. 
* Domain Admin : Root Account와 같은 레벨의 권한을 가짐, Root Account가 생성하여 관리 해야함
* Project Admin : 각각의 Project 내의 리소스를 조회할 권한을 가짐

#### Q. 사내에 Google Workspace를 사용중에 있어 Google ID를 연동하고 싶습니다. 가능 할까요?

네, 가능합니다. SpaceONE은 ID/PW를 통한 Local 인증과 Google oAuth Plugin을 통한 외부 인증 방식을 모두 지원합니다. oAuth Client ID 발급과 Redirect URI 등록절차만 해주시면 편리하게 가능 합니다. 



## Statistics

통계 데이터 관련 문의

#### Q. Main Dashboard/Project Dashboad 상의 History 데이터는 구체적으로 언제 저장 되나요?

매일 01:00\(UTC\)에 도메인별/프로젝트 별로 사용량에 대한 통계를 수집해서, 저장합니다. Cloud Resource에 대한 데이터만 통계 수집으로 저장하고, Billing 데이터의 경우 별도 적재없이, 실시간으로 외부 Billing Data Source에 적재된 데이터를 보여줍니다. 



## Plugin

Collector의 플러그인 관리

#### Q. Collector의 플러그인 버전 관리는 어떻게 하나요? 

Collector 플러그인의 경우 회사 내 관리자가 Self로 변경하실 수 있는 기능을 제공합니다. \(Plugin &gt; Collector 선택 &gt; Edit\)

SpaceONE은 내부적으로 두 가지 버전을 가지고 있습니다. 첫번째는 SpaceONE Core 서비스에 대한 버전이고, 두번째는 각 Plugin에 대한 버전입니다. Core 서비스에 대한 버전은 Console Login 화면 왼쪽 하단에 기록 되어있습니다. Inventory Plugin에 대한 버전은 Collector 리스트에서 조회하실 수 있습니다. 

Core 서비스와 Plugin 버전에 대해 검증된 호환성 리스트를 매 Release Note에 안내 드리고 있습니다. Release Note 리스트는 아래 링크를 참고해주세요. 

{% embed url="https://www.spaceone.org/release-note" %}

{% embed url="https://github.com/spaceone-dev/spaceone/tree/master/release\_notes" %}










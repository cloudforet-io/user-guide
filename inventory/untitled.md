---
description: Server Resource를 관리하는 기능 입니다.
---

# Server

## 둘러보기  

Server 메뉴에서는 다양한 지역 및 프로젝트 별로 흩어져 있는 Server 자원들을 통합 관리할 수 있습니다. 

이 기능을 통해 매번 계정 및 Region을 변경해가며 Cloud Console에 반복 접속하거나, 터미널을 통한 접속을 하지않아도, 서버의 상태를 편리하게 확인 할 수 있습니다.  

![Server &#xAD00;&#xB9AC; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-05-5.50.33-.png)

  Server 메뉴는 크게 아래와 같이 구성되어 있습니다. 

* 서버 리스트 : 서버의 전체 리스트를 확인할 수 있습니다. 
* 상세 현황 탭 : 각 서버별 상세 정보를 조회할 수 있습니다. 
* 검색 바 : 다수의 서버 상태를 편리하게 검색할 수 있습니다.

## 서버 리스트

Multi Cloud 기반으로 수집된 서버정보를 조회할 수 있습니다. 

![](../.gitbook/assets/2020-08-05-5.50.33-2.png)

서버의 각 항목별 정보는 아래와 같습니다.  

<table>
  <thead>
    <tr>
      <th style="text-align:left">Item</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">
        <p></p>
        <p>&#xC11C;&#xBC84;&#xC758; &#xC774;&#xB984;&#xC744; &#xC758;&#xBBF8; &#xD569;&#xB2C8;&#xB2E4;.
          OS &#xB0B4;&#xBD80;&#xC758; hostname&#xC774;&#xC678;&#xC758; &#xAC01; Cloud
          &#xC0AC;&#xC5D0;&#xC11C; &#xC81C;&#xACF5;&#xD558;&#xB294; &#xC774;&#xB984;
          &#xAC12;(Name Tag)&#xC744; &#xCC38;&#xC870; &#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Instance Type</td>
      <td style="text-align:left">&#xC11C;&#xBC84;&#xC758; spec. &#xC815;&#xBCF4;&#xB97C; &#xD45C;&#xD604;
        &#xD569;&#xB2C8;&#xB2E4;. spec. &#xAC01; Cloud Provider&#xC758; Compute
        &#xC11C;&#xBE44;&#xC2A4;&#xC5D0;&#xC11C; &#xC81C;&#xACF5;&#xD558;&#xB294;
        &#xBA85;&#xCE6D;&#xC744; &#xB530;&#xB985;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Core/Memory</td>
      <td style="text-align:left">&#xC11C;&#xBC84;&#xC758; Core/Memory(GB)&#xB97C; &#xB098;&#xD0C0;&#xB0C5;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Availability Zone</td>
      <td style="text-align:left">&#xC11C;&#xBC84;&#xAC00; &#xC704;&#xCE58;&#xD55C; Zone &#xC815;&#xBCF4;&#xB97C;
        &#xB098;&#xD0C0;&#xB0C5;&#xB2C8;&#xB2E4;</td>
    </tr>
    <tr>
      <td style="text-align:left">Instance State</td>
      <td style="text-align:left">&#xC11C;&#xBC84;&#xC758; &#xC0C1;&#xD0DC;&#xB97C; &#xC758;&#xBBF8; &#xD569;&#xB2C8;&#xB2E4;.
        &#xAC01; cloud provider&#xC5D0;&#xC11C; &#xC81C;&#xACF5;&#xD558;&#xB294;
        running/stopped &#xB4F1; &#xC0C1;&#xD0DC; &#xC815;&#xBCF4;&#xB97C; &#xADF8;&#xB300;&#xB85C;
        &#xB530;&#xB985;&#xB2C8;&#xB2E4;</td>
    </tr>
    <tr>
      <td style="text-align:left">Collection State</td>
      <td style="text-align:left">
        <p></p>
        <p>Collector&#xB97C; &#xD1B5;&#xD55C; &#xC11C;&#xBC84;&#xC758; &#xC218;&#xC9D1;
          &#xC0C1;&#xD0DC;&#xB97C; &#xC758;&#xBBF8; &#xD569;&#xB2C8;&#xB2E4;. ACTIVE/DISCONNECTED
          &#xC0C1;&#xD0DC;&#xAC00; &#xC874;&#xC7AC;&#xD558;&#xBA70;, &#xB300;&#xC0C1;
          &#xC11C;&#xBC84;&#xC815;&#xBCF4;&#xAC00; collector&#xB97C; &#xD1B5;&#xD574;
          &#xC815;&#xC0C1;&#xC801;&#xC73C;&#xB85C; &#xC218;&#xC9D1;&#xB418;&#xACE0;
          &#xC788;&#xB294;&#xC9C0; &#xC5EC;&#xBD80;&#xB97C; &#xB098;&#xD0C0;&#xB0C5;&#xB2C8;&#xB2E4;.</p>
        <ul>
          <li>Disconnected &#xC0C1;&#xD0DC;&#xB294; collector&#xB97C; &#xD1B5;&#xD55C;
            &#xC218;&#xC9D1;&#xC774; &#xB418;&#xACE0; &#xC788;&#xC9C0; &#xC54A;&#xB294;
            &#xC0C1;&#xD669;&#xC73C;&#xB85C;, 48&#xC2DC;&#xAC04; &#xC774;&#xC0C1; &#xC815;&#xC0C1;&#xC801;&#xC73C;&#xB85C;
            &#xC218;&#xC9D1;&#xB418;&#xC9C0; &#xC54A;&#xC744; &#xACBD;&#xC6B0; &#xD574;&#xB2F9;
            &#xC11C;&#xBC84;&#xB97C; &#xB9AC;&#xC2A4;&#xD2B8;&#xC5D0;&#xC11C; &#xC0AD;&#xC81C;&#xD569;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">OS</td>
      <td style="text-align:left">ubuntu/amazonlinux/centos/win2019 &#xC744; &#xC11C;&#xBC84;&#xC758; OS
        &#xC815;&#xBCF4;&#xB97C; &#xD45C;&#xC2DC;&#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Public IP</td>
      <td style="text-align:left">&#xACF5;&#xC778; IP(ex. AWS EIP &#xB4F1;)&#xAC00; instance&#xC5D0; mount
        &#xB41C; &#xACBD;&#xC6B0; &#xD45C;&#xC2DC;&#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Provider</td>
      <td style="text-align:left">Cloud Provider&#xB97C; &#xB098;&#xD0C0;&#xB0C5;&#xB2C8;&#xB2E4;. aws,
        azure, gcp, openstack, vmware &#xB4F1;&#xC758; cloud &#xC81C;&#xACF5;&#xC790;&#xB97C;
        &#xB098;&#xD0C0;&#xB0C5;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Account ID</td>
      <td style="text-align:left">AWS&#xC5D0;&#xC11C; &#xC0AC;&#xC6A9;&#xB418;&#xB294; 12&#xC790;&#xB9AC;
        account id &#xC22B;&#xC790;&#xB97C; &#xD45C;&#xD604; &#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Project</td>
      <td style="text-align:left">&#xB300;&#xC0C1; &#xC11C;&#xBC84;&#xAC00; &#xC18C;&#xC18D;&#xB41C; project&#xB97C;
        &#xD45C;&#xD604;&#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Updated at</td>
      <td style="text-align:left">&#xC11C;&#xBC84; &#xC815;&#xBCF4;&#xAC00; &#xC218;&#xC9D1;&#xB41C; &#xAC00;&#xC7A5;
        &#xB9C8;&#xC9C0;&#xB9C9; &#xC2DC;&#xAC04;&#xC744; &#xB098;&#xD0C0;&#xB0C5;&#xB2C8;&#xB2E4;.</td>
    </tr>
  </tbody>
</table>

### Action

각 서버를  선택 후 상단의 Action 버튼을 클릭하면, 서버의 상태를 변경할 수 있습니다.

![Action &#xB9AC;&#xC2A4;&#xD2B8;](../.gitbook/assets/2020-08-06-4.13.08.png)

* Delete : 서버 리스트에서 삭제 합니다. 서버를 실제 삭제하지는 않습니다. Collector를 통한 수집 재개시 다시 추가됩니다.
* Set In-Service/Maintenance/Close : 서버의 상태를 변경 합니다. 
* Change Project : 서버가 속해있는 Project 를 변경 합니다. 
* Console : 대상 서버가 속해있는 AWS Console 링크로 바로 연결 합니다. 

### Export

수집된 서버 리스트의 정보를 Excel로 Export 할 수 있습니다. 

![Excel Export](../.gitbook/assets/2020-08-06-4.11.27-.png)



## 상세 현황 탭

서버에 대한 상세 정보를 제공합니다. 아래와 같은 Tab 으로 구성되어 있습니다.

* Details : 서버 리스트에서 확인할 수 있는 기본 정보이외에, 서버 Spec. 이나 Image 명, Security Group 등의 추가 상세 정보를 제공합니다.

![Details &#xD0ED;](../.gitbook/assets/2020-08-06-5.09.53.png)

* Tag : 서버를 Tag로 별도 그룹화 하여 관리할 수 있도록 합니다. 
* Member : 서버의 담당자를 관리할 수 있습니다. 
* History : 서버의 상태/Spec. 등 모든 변경 이력을 관리할 수 있습니다. 
* Monitoring : 서버의 모니터링 정보를 조회 할 수 있습니다. 외부의 모니터링 솔루션과 연계하여 대상 서버의 상태를 실시간으로 조회할 수 있습니다. 

![Monitoring &#xD0ED;](../.gitbook/assets/2020-08-06-5.11.19.png)

## 검색 바 

수집된 서버를 Key Word 기반으로 편리하게 검색할 수 있습니다.

SpaceONE에서는 Collector로부터 수집된 정보들을 사용자들이 편리하게 검색할 수 있게 주요 keyword 기반으로 자동 분류 합니다.

![Server &#xAC80;&#xC0C9;&#xBC14;](../.gitbook/assets/2020-08-06-5.12.57-.png)

제공 되는 keyword는 Server에 정의된 거의 모든 항목을 포함 합니다. \(총 31항목\)

![&#xAC80;&#xC0C9; keyword list](../.gitbook/assets/2020-08-06-5.16.04.png)




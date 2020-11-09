---
description: 프로젝트 리소스들을 자동으로 스케줄링해 관리하는 기능입니다.
---

# Power Scheduler

## 둘러보기

Power scheduler 페이지에서는 프로젝트의 resource를 자동으로 on-off 하는 scheduling을 관리합니다. 스케줄러 정보를 확인하고, 새 스케줄러를 생성, 수정 또는 삭제하는 기능을  제공합니다. 



## Prerequisites

SpaceONE의 power scheduler 서비스 이용에 필요한 IAM 정책을 각 cloud-provider 별로 해당 credential에 미리 정의해 SpaceONE의 사용자 리소스 액세스를 안전하게 제어하고, 다른 리소스에 대한 액세스를 방지할 수 있습니다.  

Power Scheduler를 생성하기 전  아래  페이지에 명시된 방법 통해 각 cloud provider의 콘솔에서 해당 정책을 SpaceONE에 할당해주시기 바랍니다. 

{% page-ref page="../identity/service-account/service-account-policy-management.md" %}

## Power scheduler 조회

![](../.gitbook/assets/image%20%2812%29.png)

**스케줄러 조회** 

프로젝트 목록과 함께 설정된 스케줄러의 목록  한눈에 조회할 수 있는 페이지입니다. 

**검색**

검색 바를 통해 프로젝트 이름으로 검색할 수 있습니다.

**스케줄링 Dashboard** 

하나의 스케줄 Dashboard 에 표현되는 정보는 다과 같습니다.  

![&#xC2A4;&#xCF00;&#xC904; Dashboard](../.gitbook/assets/image%20%2863%29.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Item</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xD504;&#xB85C;&#xC81D;&#xD2B8; &#xC774;&#xB984;</td>
      <td style="text-align:left">&#xD574;&#xB2F9; &#xC2A4;&#xCF00;&#xC904;&#xB7EC;&#xAC00; &#xB9CC;&#xB4E4;&#xC5B4;&#xC9C4;
        &#xD504;&#xB85C;&#xC81D;&#xD2B8; &#xC774;&#xB984;&#xACFC; &#xADF8;&#xB8F9;&#xC774;&#xB984;</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC790;&#xC6D0; &#xC218;</td>
      <td style="text-align:left">
        <ul>
          <li>&#xC801;&#xC6A9;&#xB41C; &#xC790;&#xC6D0; &#xC218; : power scheduler&#xC5D0;&#xC11C;
            &#xAD00;&#xB9AC;&#xD558;&#xACE0; &#xC788;&#xB294; &#xC790;&#xC6D0;&#xC758;
            &#xC218;</li>
          <li>&#xC801;&#xC6A9; &#xAC00;&#xB2A5;&#xD55C; &#xC790;&#xC6D0; &#xC218; :
            power scheduler&#xC5D0;&#xC11C; &#xAD00;&#xB9AC; &#xAC00;&#xB2A5;&#xD55C;
            &#xC790;&#xC6D0;&#xC758; &#xC218; (Server, RDS, Auto Scaling Group)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC2A4;&#xCF00;&#xC904; &#xBAA9;&#xB85D;</td>
      <td style="text-align:left">&#xC2A4;&#xCF00;&#xC904;&#xC758; &#xBAA9;&#xB85D;&#xC774;&#xBA70;, &#xB300;&#xC2DC;&#xBCF4;&#xB4DC;&#xC5D0;&#xB294;
        &#xCD5C;&#xB300; 3&#xAC1C;&#xAE4C;&#xC9C0; &#xD45C;</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC608;&#xC0C1; &#xC808;&#xAC10; &#xBE44;</td>
      <td style="text-align:left">&#xC9C0;&#xB09C; 1&#xAC1C;&#xC6D4;&#xAC04; Power scheduler&#xC744; &#xD1B5;&#xD574;
        &#xC808;&#xAC10;&#xB41C; &#xBE44;&#xC758; &#xD569;&#xC744; &#xB2EC;&#xB7EC;&#xB85C;
        &#xD45C;</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC2A4;&#xCF00;&#xC904;&#xB9C1; &#xD788;&#xD2B8;&#xB9F5;</td>
      <td style="text-align:left">&#xC2A4;&#xCF00;&#xC904;&#xC774; &#xBA87;&#xC2DC;&#xAC04;&#xC529; &#xD560;&#xB2F9;&#xB418;&#xC5C8;&#xB294;&#xC9C0;&#xC758;
        &#xC815;&#xB3C4;&#xB97C; &#xC0C9;&#xC73C;&#xB85C; &#xD45C;&#xC2DC;</td>
    </tr>
  </tbody>
</table>

> **스케줄링 히트맵** 
>
> 스케줄링 히트맵에 표시되는 색에는 2단계가 있습니다. 색은 스케줄이 몇시간씩 할당되었는지의 정도를 보여주며, 각 색이 나타내는 의미는 다음과 같습니다.

> ![](../.gitbook/assets/image%20%2858%29.png)스케줄러에 의해 스케줄링 된 시간이 0 ~ 12 시간

> ![](../.gitbook/assets/image%20%2847%29.png)스케줄러에 의해 스케줄링 된 시간이 12~24 시간

## Power scheduler 상세 조회

### 스케줄러 상세조

스케줄러  상세화면에서는 다음과 같은 기능을 조회합니다. 

#### 

#### 시간

![weekly calendar](../.gitbook/assets/image%20%2828%29.png)

scheduler가 적용되는 시간을 한눈에 볼 수 있습니다. calendar의 가로축은 날짜, 세로축은 scheduler가 적용될 시간입니다.  `이번주` 버튼을 클릭하면 이번주의 scheduler 플랜을 볼 수 있습니다.

그래프 오른쪽 상단의 `< >`  를 통해 달을 이동할 수 있습니다.  

스케줄에는 3가지의 scheduled mode가 있습니다.

| Scheduled mode | State | Description | color |
| :--- | :--- | :--- | :--- |
| 반복 스케줄 |  | 매주 반복되는 타이머로 선택된 영역은 resource가 켜지며, 해제된 영역은 resource가 꺼집니다.  | ![](../.gitbook/assets/image%20%288%29.png) |
| 1회성 스케줄 | 켜기 | 특정 날짜에 생성되는 일회성 타이머로, 선택된 영역은 resource가 켜집니다. | ![](../.gitbook/assets/image%20%2816%29.png) |
|  | 끄 | 특정 날짜에 생성되는 일회성 타이머로, 선택된 영역에서 resource가 꺼집니다.  | ![](../.gitbook/assets/image%20%2855%29.png) |

#### 리소스 그룹 

**• 스케줄러 우선순위 단계**

![&#xB9AC;&#xC18C;&#xC2A4; &#xADF8;&#xB8F9;](../.gitbook/assets/image%20%289%29.png)

스케줄러는 여러개의 Resource Group으로 이루어지며, 각 스케줄러 간에 단계를 설정할 수 있습니다.  

스케줄러의 우선순위가 높을수록 숫자가 작아집니다. 스케줄러 우선순위를 5개 이상 지정하고 싶은 경우,  `편집하기` 버튼을 누른 후   `+ 우선순위 추가` 버튼을 누르면 스케줄러 그룹이 추가됩니다.  

스케줄러에 리소스그룹이 지정되어 있으면 스케줄러 단계 삭제되지 않습니다. 



**• 리소스 그룹 우선순위**

![](../.gitbook/assets/image%20%2857%29.png)

하나의 스케줄러 내 리소스그룹 간의 우선순위를 설정할 수  있습니다.  리소스 그룹의 우선순위란 Booting 순서를 의미합니다. 스케줄러에 `N`개의 리소스 그룹이 있다고 가하면, `1`번부터 `N`번 순서로 리소스가 켜지고, `N`번부터 `1`번 순서로 리소스가 종료됩니다. 



**• 리소스 그룹 보기**

![](../.gitbook/assets/image%20%2852%29.png)

스케줄러 페이지에서 리소스 그룹에 대한 정보를 조회합니다. `리소스그룹의 이름`을 클릭하면 다음과 같은 그룹 정보를 볼 수 있습니다.

| Item | Description |
| :--- | :--- |
| 그룹 이름 | 스케줄러 생성 시 입력했던 리소스 그룹의 이름 |
| 리소스 타 | 스케줄러 생성 시 입력했던 그룹기준 &gt; 리소스 타입  |
| 리소스 목 | 해당 그룹에 속하는 리소스 목 |

### 

### 새 scheduler 생성



![&#xC0C8; &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC0DD;&#xC131; &#xD398;&#xC774;&#xC9C0;](../.gitbook/assets/image%20%2850%29.png)

페이지 왼쪽 상단의 `새 스케줄러 만들기`  버튼을 눌러 Power scheduler를 생성합니다. 프로젝트에 기존에 생성한 스케줄러가 없는 경우 자동으로 생성모드로 변경됩니다.  

스케줄 생성하기 위해서는 다음과 같은 정보를 설정해야합니다. 

#### 이름

생성할 Power scheduler의 이름이며, 문자와 `-` 를 포함한 문자열 입력할 수 있습니다. 띄어쓰기가 불가합니다. 이름 입력이 누락되면 스케줄러 생성되지 않습니다. 

#### 시간

스케줄이 적용되는 시간을 설정합니. calendar의 가로축은 날짜, 세로축은 스케줄러가 적용될 시간입니다.  `이번주` 버튼을 클릭하면 이번주의 스케줄 플랜을  입력합니다.  날짜와 시간을 클릭/ 드래그 하여 편리하게 타이머를 적용할 수 있습니다. 한번 더 클릭하면 타이머를 해제할 수 있습니다. 

스케줄에는 3가지의 scheduled mode가 있습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Scheduled mode</th>
      <th style="text-align:left">State</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">icon</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xBC18;&#xBCF5; &#xC2A4;&#xCF00;&#xC904;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xB9E4;&#xC8FC; &#xBC18;&#xBCF5;&#xB418;&#xB294; &#xD0C0;&#xC774;&#xBA38;&#xB85C;
        &#xC120;&#xD0DD;&#xB41C; &#xC601;&#xC5ED;&#xC740; resource&#xAC00; &#xCF1C;&#xC9C0;&#xBA70;,
        &#xD574;&#xC81C;&#xB41C; &#xC601;&#xC5ED;&#xC740; resource&#xAC00; &#xAEBC;&#xC9D1;&#xB2C8;&#xB2E4;.</td>
      <td
      style="text-align:left">
        <p></p>
        <p>
          <img src="../.gitbook/assets/image (8).png" alt/>
        </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">1&#xD68C;&#xC131; &#xC2A4;&#xCF00;</td>
      <td style="text-align:left">&#xCF1C;&#xAE30;</td>
      <td style="text-align:left">&#xD2B9;&#xC815; &#xB0A0;&#xC9DC;&#xC5D0; &#xC0DD;&#xC131;&#xB418;&#xB294;
        &#xC77C;&#xD68C;&#xC131; &#xD0C0;&#xC774;&#xBA38;&#xB85C;, &#xC120;&#xD0DD;&#xB41C;
        &#xC601;&#xC5ED;&#xC740; resource&#xAC00; &#xCF1C;&#xC9D1;&#xB2C8;&#xB2E4;.</td>
      <td
      style="text-align:left">
        <img src="../.gitbook/assets/image (16).png" alt/>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xB044;</td>
      <td style="text-align:left">&#xD2B9;&#xC815; &#xB0A0;&#xC9DC;&#xC5D0; &#xC0DD;&#xC131;&#xB418;&#xB294;
        &#xC77C;&#xD68C;&#xC131; &#xD0C0;&#xC774;&#xBA38;&#xB85C;, &#xC120;&#xD0DD;&#xB41C;
        &#xC601;&#xC5ED;&#xC740; resource&#xAC00; &#xAEBC;&#xC9D1;&#xB2C8;&#xB2E4;.</td>
      <td
      style="text-align:left">
        <p></p>
        <p>
          <img src="../.gitbook/assets/image (55).png" alt/>
        </p>
        </td>
    </tr>
  </tbody>
</table>



#### 리소스 그룹

스케줄러를 적용할 리소스 그룹을 정의합니다.  `리소스 그룹 추가` 버튼을 누르면 `리소스 그룹 만들기` 페이지가 나타납니다. 

리소스 그룹 생성 시 설정해야 하는 정보는 다음과 같습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Item</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xADF8;&#xB8F9; &#xAE30;&#xBCF8; &#xC815;&#xBCF4;</td>
      <td style="text-align:left">&#xADF8;&#xC774;&#xB984;&#xC744; &#xC785;&#xB825;&#xD569;&#xB2C8;&#xB2E4;.
        &#xCD5C;&#xB300; 128&#xC790; &#xAE4C;&#xC9C0; &#xC785;&#xB825; &#xAC00;&#xB2A5;&#xD558;&#xBA70;,
        &#xBA54;&#xC778;&#xD654;&#xBA74;&#xC758; &#xB9AC;&#xC18C;&#xC2A4; &#xADF8;&#xB8F9;
        &#xCE74;&#xB4DC;&#xC5D0;&#xB294; 16&#xC790; &#xAE4C;&#xC9C0; &#xD45C;&#xC2DC;&#xB429;&#xB2C8;&#xB2E4;.
        &#xBB38;&#xC790;&#xB85C; &#xC2DC;&#xC791;&#xD574;&#xC57C;&#xD558;&#xACE0;,
        &#xBB38;&#xC790;/&#xC22B;&#xC790;/ <code>- </code> &#xC744; &#xD3EC;&#xD568;&#xD55C;
        &#xBB38;&#xC790;&#xC5F4;&#xB85C; &#xC785;&#xB825;&#xD574;&#xC57C;&#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xADF8;&#xB8F9; &#xAE30;&#xC900;</td>
      <td style="text-align:left">
        <p>&#xB9AC;&#xC18C;&#xC2A4; &#xD0C0;&#xC785;&#xC744; &#xC120;&#xD0DD;&#xD569;&#xB2C8;&#xB2E4;.
          &#xB9AC;&#xC18C;&#xC2A4; &#xD0C0;&#xC785;&#xC744; &#xC120;&#xD0DD;&#xD558;&#xBA74;
          &#xADF8;&#xC5D0; &#xB530;&#xB978; &#xB9AC;&#xC18C;&#xC2A4; &#xBAA9;&#xB85D;&#xC774;
          &#xC544;&#xB798;&#xC5D0; &#xD45C;&#xC2DC;&#xB429;&#xB2C8;&#xB2E4;.</p>
        <p>
          <img src="../.gitbook/assets/image (17).png" alt/>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xB9AC;&#xC18C;&#xC2A4; &#xBAA9;</td>
      <td style="text-align:left">&#xB9AC;&#xC18C;&#xC2A4; &#xBAA9;&#xB85D;&#xC5D0;&#xC11C; &#xBCF4;&#xC5EC;&#xC9C0;&#xB294;
        &#xB9AC;&#xC18C;&#xC2A4;&#xB4E4;&#xC774; scheduling &#xB429;&#xB2C8;&#xB2E4;.</td>
    </tr>
  </tbody>
</table>

설정한 정보를 확인한 후, 페이지 우측 하단의 `저장`버튼을 클릭해 저장합니다.  



### 스케줄 삭제

![](../.gitbook/assets/image.png)

상단의 `휴지통` 버튼으로 스케줄러를 삭제할 수 있습니다. 

### 스케줄러 수정

<table>
  <thead>
    <tr>
      <th style="text-align:left">item</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC774;&#xB984; &#xC218;</td>
      <td style="text-align:left">
        <p>&#xD398;&#xC774;&#xC9C0; &#xC0C1;&#xB2E8;&#xC5D0; &#xC704;&#xCE58;<code>&#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xD3B8;&#xC9D1;</code>&#xBC84;&#xD2BC;&#xC73C;&#xB85C;
          &#xC2A4;&#xCF00;&#xC904;&#xB7EC;&#xC758; &#xC774;&#xB984;&#xC744; &#xD3B8;&#xC9D1;&#xD560;
          &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p></p>
        <p>
          <img src="../.gitbook/assets/image (38).png" alt/>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC2DC;&#xAC04; &#xC218;</td>
      <td style="text-align:left">
        <p>calendar&#xC758; <code>&#xD3B8;&#xC9D1;&#xD558;&#xAE30;</code> &#xBC84;&#xD2BC;&#xC73C;&#xB85C;
          &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC9C0;&#xC815; &#xC2DC;&#xAC04;&#xB300;,
          &#xBC18;&#xBCF5; &#xC2A4;&#xCF00;&#xC904; &#xBC0F; 1&#xD68C;&#xC131; &#xC2A4;&#xCF00;&#xC904;&#xC744;
          &#xAC01;&#xAC01; &#xC218;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p></p>
        <p>
          <img src="../.gitbook/assets/image (66).png" alt/>
        </p>
        <p></p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xB9AC;&#xC18C;&#xC2A4; &#xADF8;&#xB8F9; &#xC218;</td>
      <td style="text-align:left">
        <p>&#xB9AC;&#xC18C;&#xC2A4; &#xADF8;&#xB8F9; &#xC704;<code>&#xD3B8;&#xC9D1;&#xD558;&#xAE30;</code> &#xBC84;&#xD2BC;&#xC73C;&#xB85C;
          &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC9C0;&#xC815; &#xC2DC;&#xAC04;&#xB300;&#xB97C;
          &#xC218;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>
          <img src="../.gitbook/assets/image (33).png" alt/>
        </p>
        <p></p>
      </td>
    </tr>
  </tbody>
</table>






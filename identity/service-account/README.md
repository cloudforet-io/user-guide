---
description: 각 Cloud Provider의 Credential 정보를 관리 합니다.
---

# Service Account

## 概要

Service Accountページからユーザーは様々なProviderが提供するCredentialを楽に管理することができます。この情報をベースにしてMulti Cloud Resource 情報を収集します。

![Service Account &#xAD00;&#xB9AC; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-4.34.53-2%20%281%29.png)

ページでユーザーは次の作業ができます。

* Service Account追加
* Service Account削除/Project変更
* AWS Consoleとリンク
* 詳細照会及び管理



現在SpaceONEが支援するservice providerは次の通りです。

* AWS
* Google Cloud
* Microsoft Azure
* MEGAZONE
* SpaceONE

## Service Account追加

Cloud Providerを選択した後、_**+ Add**_ をクリックしてService Accountが新しく追加できます。

ユーザーガイドではAWSのIAMを例としています。

Service Account入力ページは\* で表記されている項目を入力すれば簡単に追加できます。

### Base Information

![Ser](../../.gitbook/assets/2020-08-07-5.44.58.png)

* Name : Service Account名を入力します。
* Account ID : AWSのAccount ID情報を入力します。\(12桁の数字で表示されます。\)
* Tag : Service AccountのTag情報を編集します。

### Credentials

SpaceONEでは二つのタイプのService Accountをサポートします。\(aws\_access\_key, aws\_assume\_role\)

各タイプ別入力項目は次のようです。

#### aws\_access\_key  

![aws access key &#xBC29;&#xC2DD;&#xC758; key &#xC785;&#xB825; &#xD3FC;](../../.gitbook/assets/2020-08-07-5.48.28.png)

* Region\(Option\) : 収集対象のRegion情報を入力します。入力しない場合、すべてのregionからcloud resourceをスキャンします。
* AWS Access Key\(Required\) : IAMのAccess Keyを入力します。主にRead Only IAMアカウントを別途作成して入力します。  
* AWS Secret Key\(Required\) : 上で入力したIAMのSecret keyを入力します。

#### aws\_assume\_role

![aws\_assume\_role &#xBC29;&#xC2DD;&#xC758; &#xC785;&#xB825; &#xD3FC;](../../.gitbook/assets/2020-08-07-5.53.33.png)

* Region\(Option\) : 収集対象のRegion情報を入力します。入力しない場合、すべてのregionからcloud resourceをスキャンします。
* AWS Access Key\(Required\) : Assumeを受けるIAMアカウントのAccess Keyを入力します。
* AWS Secret Key\(Required\) : Assumeを受けるIAMアカウントのSecret Keyを入力します。
* Role ARN\(Required\) : IAMで作成したAssume RoleのRole ARN情報を入力します。

### Project選択

Service Accountが属されるProjectを指定します。プロジェクトを指定すれば、そのService Accountで収集されたCloud Resource情報は自動的にProjectと連動されます。

![Project &#xC120;&#xD0DD; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-6.02.19.png)

* Project作成が必要な場合、_**+ Create Project**_ をクリックして必要なProject Group/Projectを作成した後進めます。Project作成に対する詳細内容は下記のリングをご参照ください。

{% page-ref page="../../project/project-group-management.md" %}

* Projectを選択した後_**Save**_ をクリックすれば、Service Account作成が完了されます。
* Projectを指定したくない場合、_**Select no Project**_を選択します。Projectは後程指定できます。

## Service Account削除/Project変更

Service Accountを削除若しくは以前指定したProjectを変更します。

対象のService Accountを選択した後、_**Action**_メニューをクリックした後、_**Delete**_ 若しくは_**Change Project**_を選択します。

![Service Account &#xC0AD;&#xC81C;/&#xBCC0;&#xACBD; &#xBA54;&#xB274;](../../.gitbook/assets/2020-08-07-6.17.37.png)

#### Service Account削除

下記のようにService Account削除画面でService Account名を入力した後、_**Confirm**_ をクリックして削除できます。

![Service Account &#xC0AD;&#xC81C; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-6.21.27.png)

#### Project変更

下記のようにChange Project画面で変更したいProjectを指定した後、_**Confirm**_をクリックして削除できます。

![Project &#xBCC0;&#xACBD; &#xD654;&#xBA74;](../../.gitbook/assets/2020-08-07-6.22.47.png)

## AWS Consoleへリンク

対象のService Accountを選択した後、_**Action**_メニューをクリックして_**Console**_を選択します。

AWSのコンソールリンクへ移動します。事前にAWS Consoleへログインするか、ログインしてからそのIAM Accountへ移動できます。



## 詳細照会及び管理

詳細管理タグを通して Service Accountの詳細情報の確認/Tag管理/Credential管理/Member管理ができます。

#### Detail 

Service AccountのMeta情報が確認できます。

![Service Account &#xC0C1;&#xC138;&#xC870;&#xD68C;](../../.gitbook/assets/2020-08-07-6.33.27.png)

#### Tag

_**Edit**_をクリックしてService AccountのTagが追加/削除できます。

![Tag &#xCD94;&#xAC00;/&#xC0AD;&#xC81C; ](../../.gitbook/assets/2020-08-07-6.54.13.png)

#### Credentials

Service AccountではKey情報を保存しているCredentialを追加/削除できます。

####  




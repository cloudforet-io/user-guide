---
description: 簡単で素早くPower Schedulerが利用できるQuick Guideです。
---

# Power Scheduler Quick Start

## 全体の手順

下記のような手順で設定した後、Power schedulerが利用できます。

* [Prerequisites](power-scheduler-quick-start.md#prerequisites)
* [スケージュールの基本情報設定](power-scheduler-quick-start.md#scheduler)
* [スケジューラの動作時間設定](power-scheduler-quick-start.md#undefined-1)
* [リソースグループの定義](power-scheduler-quick-start.md#undefined-2)

## Prerequisites

SpaceONEのpower schedulerサービスを利用する際に必要なIAM政策を各cloud-providerごとにcredentialに事前に定義しておけば、SpaceONEがユーザーのリソースに対するアクセスを安全に制御でき、他のリソースへのアクセスを防止することができます。

Power Schedulerを作成する前に、下記のページに明示されている方法を通して各Cloud providerのコンソールから該当する政策をSpaceONEに割り当ててください。

{% page-ref page="../identity/service-account/service-account-policy-management.md" %}

## Scheduler基本情報の設定

上部の`Automation` &gt; `Power Scheduler` をクリックします。

![power scheduler &#xB9E4;&#xB274; &#xC120;&#xD0DD;](../.gitbook/assets/image%20%283%29.png)



スケジューラを設定するプロジェクトのdashboardを選択します。

![&#xD504;&#xB85C;&#xC81D;&#xD2B8; Dashboard &#xC120;&#xD0DD;](../.gitbook/assets/image%20%2871%29.png)





左側の `+ 新しいスケジューラの作成` をクリックします。プロジェクトに以前作成したスケジューラがない場合、自動的に作成モードに変更されます。

![&#xC0C8; &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xB9CC;&#xB4E4;&#xAE30;](../.gitbook/assets/image%20%2822%29.png)





スケジューラ名を設定します。文字と `-` を含む文字列が入力できます。間隔は入れません。スケジューラ名は必須項目で、名前が入ってない場合、スケジューラは作成できません。 

![](../.gitbook/assets/image%20%2842%29.png)

### 



## スケジューラの動作時間の設定

![&#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC801;&#xC6A9; &#xC2DC;&#xAC04; &#xC124;&#xC815;](../.gitbook/assets/image%20%2841%29.png)

スケジューラが適用される時間を設定します。 Calendarの横軸は日付、縦軸はスケジューラが適用される時間です。 `今週` ボタンをクリックしすれば、今週のスケジュールが設定できます。

グラフの右上の `< >` をクリックしすれば月の移動ができます。



スケジュールには3つのscheduled modeがあります。

| Scheduled mode | State | Description | color |
| :--- | :--- | :--- | :--- |
| 繰り返しスケジュール |  | 毎週繰り返されるタイマーで、選択した時間にはresourceが作動し、それ以外の時間にはresourceはオフになります。 | ![](../.gitbook/assets/image%20%288%29.png) |
| ワンタイムスケジュール | オン | 特定日に作成されるワンタイムスケジュールで、選択した時間にresource作動します。 | ![](../.gitbook/assets/image%20%2816%29.png) |
|  | オフ | 特定日に作成されるワンタイムスケジュールで、選択した時間にresourceがオフになります。 | ![](../.gitbook/assets/image%20%2855%29.png) |



マウスでクリック/ドラッグしてスケジュールが作動する時間を設定します。

![&#xC2A4;&#xCF00;&#xC904;&#xB7EC; calendar &#xB9C8;&#xC6B0;&#xC2A4; &#xD074;&#xB9AD; / &#xB4DC;&#xB798;&#xADF8;](../.gitbook/assets/image%20%2819%29.png)

> 設定がなければ `모두 끄기`として認識され、リソースがオフになるので、ご注意ください。

## リソースグループの定義

スケジュールを適用するリソースグループを定義します。

![](../.gitbook/assets/image%20%2840%29.png)

`+ グループ追加` をクリックしてリソースグループ作成ページに移動してスケジューラを適用するリソースグループ名を入力します。

![](../.gitbook/assets/image%20%2834%29.png)

下記のリソースグループ名作成の制約事項をご参照ください。

> * 最大128字入力可能 \(リソースグループカードでは16字まで表示\)
> * 文字から始まる
> * 文字、数字、及び `-`  利用可能



リソースタイプを選択します。リソースタイプとは、スケジューラを通してリソースのon-offを適用したいもので、リソースグループ区分する基準になります。

現在、SpaceONE power schedulerが支援するリソースタイプは

`[ALL] Server / [AWS] RDS / [AWS] Auto Scaling Group`3つです。

![](../.gitbook/assets/image%20%2846%29.png)



全ての情報を入力した後、ページの右下の保存ボタンをクリックしてスケジューラ情報を保存します。

![&#xC800;&#xC7A5; &#xBC84;&#xD2BC;](../.gitbook/assets/image%20%284%29.png)

全ての情報が正しく保存された場合、スケジューラの作成完了メッセージが表示され、

![&#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC0DD;&#xC131; &#xC644;&#xB8CC; &#xD31D;&#xC5C5;](../.gitbook/assets/image%20%2811%29.png)

![&#xC0DD;&#xC131;&#xD55C; &#xC2A4;&#xCF00;&#xC904;&#xB7EC; &#xC815;&#xBCF4; &#xD655;&#xC778;](../.gitbook/assets/image%20%2824%29.png)

作成したスケジューラの情報照会ページへ移動します。

## 

> ### " Happy Power Scheduling! "




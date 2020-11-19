---
description: Collectorを作成して、Cloud Resourceを収集します。
---

# Collector

## 概要

SpaceONEはCollector Pluginを通して様々なサービスのCloud Resourceが収集できます。

Pluginは、Official MarketplaceやカスタムPluginが利用できます。

![Collector &#xAD00;&#xB9AC; &#xD398;&#xC774;&#xC9C0;](../.gitbook/assets/2020-08-06-7.48.58-.png)

## Collector作成

下記の画面のように、Official Marketplaceで利用できるplugin listが照会できます。

インストールしたいPluginを選択し、_**+ Create**_ をクリックして、Collector作成できます。

![Collector Plugin &#xC120;&#xD0DD; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-10.23.39.png)

Collector名だけを入力し、他のところはDefaultで、変更しなくてもご利用に問題ありません。Pluginバージョンの選択はできますが、主にlatestにします。

![Collector &#xC0DD;&#xC131; &#xD654;&#xBA74; \#1](../.gitbook/assets/2020-08-07-11.10.04.png)

Collectorが利用するCredentials情報を選択します。以前利用していたCredentials情報を除いて自動的にmappingするので、_**Availability**_ 項目が正常的に表示されたばあ、次の画面に移動します。

![Collector &#xC0DD;&#xC131; &#xD654;&#xBA74; \#2](../.gitbook/assets/2020-08-07-11.10.58.png)

Tagの入力画面です。CollectorにTag入力が必要ン場合追加し、そうでない場合、 _**Confirm**_ を入力して作成を完了します。

![Collector &#xC0DD;&#xC131; &#xD654;&#xBA74; \#3](../.gitbook/assets/2020-08-07-11.14.05.png)

もし、作成が正しく進めない場合、Collector作成の画面に赤く表示されるところがあるか確認します。

![](../.gitbook/assets/2020-08-07-11.16.29.png)

## Collector変更/削除/有効化/非活性化

作成を除くcollector 作業はAction リストメニューを通して確認できます。 Collectorを選択し Action をクリックして下記のような作業可能なリストが照会されます。

![Collector &#xB9AC;&#xC2A4;&#xD2B8; &#xBA54;&#xB274;](../.gitbook/assets/2020-08-07-11.18.32.png)

#### 変更

変更事項を修正した後、 _**Confirm**_ をクリックして完了します。

![Collector &#xBCC0;&#xACBD; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-11.20.18.png)

#### 削除

下記のように削除ページが表示されますが、 _**Confirm**_ をクリックします。

![Collector &#xC0AD;&#xC81C; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.06.46.png)

#### 有効化

_**DISABLE**_ 状態の Collectorを _**ENABLE**_ に変更します。Cloud Resource 収集作業ができるようになります。

![Collector &#xD65C;&#xC131;&#xD654; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.10.04.png)

#### 非有効化

Collectorを _**DISABLE**_に変更して Cloud Resource 収集作業が中止できます。

![Collector &#xBE44;&#xD65C;&#xC131;&#xD654; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.09.45.png)

## Collector照会/詳細照会

![](../.gitbook/assets/2020-08-07-2.16.13.png)

Collectorリストでは下記の情報が確認できます。

* Name : Collector名
* State : Enable/Disableで Collectorの収集が制御できます。
* Priority : 多数のCollectorから収集された情報が重複される場合、優先順位を決定します。Priorityが低いほど優先順位が高いです。
* Last Collected : Collectorが稼働された最後の時間を記録します。
* Created : Collectorが作成された時間を記録します。

Collectorの詳細動作は下記のタグで管理できます。

### Detail

Collectorの詳細設定を表示します。

Collectorが収集するデータのFilterが照会できます。

![Collector Detail &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.25.22.png)

### Tag

CollectorのTagが管理きます。_**Edit**_ をクリックしてTagが編集できます。

![Tag &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-2.27.56.png)

編集画面で _**Add Tag**_ と _**x**_ を利用して追加/削除できます。編集が完了された後、右下の _**Save**_ をクリックします。

![Tag &#xD3B8;&#xC9D1; &#xD398;&#xC774;&#xC9C0;](../.gitbook/assets/2020-08-07-3.25.03.png)

### Credentials

Collectorが利用している認証情報を表示します。その認証情報はSpaceONEのService Accountと連動されます。

_**Collect Data**_ をクリックして該当するCredentialsへ Cloud Resourceが即時に収集できます。

![Credential &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-3.28.14.png)

![Cloud Resource &#xC989;&#xC2DC; &#xC218;&#xC9D1;](../.gitbook/assets/2020-08-07-3.34.33.png)

### Schedules

Collectorがデータを収集する周期を競ってします。

Scheduleを指定した場合、毎日指定された時間にCollectorの Cloud Resource 収集が実行されます。

![Collector Schedule &#xAD00;&#xB9AC; &#xD0ED;](../.gitbook/assets/2020-08-07-3.39.39.png)

**追加**

* Add をクリックすると、スケージュール追加画面が表示されます。

名前/Timezone/収集時間が選択で起案す。

Collecting Timeは24時間基準で指定し、1時間単位で選択できます。

![Collector Schedule &#xCD94;&#xAC00; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-3.46.11.png)

#### スケージュール変更、削除

スケージュールを選択した後、 _**Action**_ **&gt; Update/Delete** を通して既存スケージュールが変更/削除できます。

![Collector Schedule &#xBCC0;&#xACBD;](../.gitbook/assets/2020-08-07-3.58.22.png)

## Cloud Resource収集

Collectorを通してご希望の時点にCloud Resourceが収集できます。ユーザーは様々な方法でProject内の Inventory データが最新化されるようにすることができます。

### 即時収集

Collectorを選択した後、 _**Action &gt; Collect Data**_ メニューをクリックして収集します。

![Collect Data &#xBA54;&#xB274;](../.gitbook/assets/2020-08-07-4.02.39.png)

下記のようなCollect Data画面が出力されますが、 _**Confirm**_ をクリックして収集を開始します。

![&#xC989;&#xC2DC; &#xC218;&#xC9D1; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-07-4.03.34.png)

Collectが実行されている状況はMain Dashboardから確認できます。画面が自動的にRefreshされないよう、周期的に_**Reload**_ をクリックします。

![Collector &#xC218;&#xC9D1; &#xC9C4;&#xD589;&#xC0C1;&#xD669;](../.gitbook/assets/2020-08-07-4.04.46.png)

### スケージュール収集

上記の _**Schedules**_ に登録されたスケージュールでSpaceONE が自動的にCloud Resource 収集作業を行います。

最終遂行時間はCollector リストから確認できます。

![Schedule &#xCD5C;&#xC885; &#xC218;&#xD589;&#xC2DC;&#xAC04; &#xD655;&#xC778;](../.gitbook/assets/2020-08-07-4.08.17-.png)


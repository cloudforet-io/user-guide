---
description: SpaceONEを初めてご利用されるお客様のためのQuick Guideです。
---

# A Compass To SpaceONE Universe Traveler

## 概要 <a id="overview"></a>

SpaceONEを利用するために、下記の順に従って設定してください。

* [**ユーザーの追加**](getting-started-2.md#adding-user)
* [**プロジェクト作成**](getting-started-2.md#creating-project)
* [**Service Account作成**](getting-started-2.md#creating-service-account)
* [**Cloud Resource収集** ](getting-started-2.md#discovering-cloud-resource)

## ユーザーの追加 <a id="adding-user"></a>

### ドメイン管理者としてログイン

SpaceONEサービスはお客様毎にドメインが割り当てられ、そのドメインで接続してご利用できます。

サービス申請後、管理者から割り当てられたサービスURLとAdmin ID/Passwordでサービスにアクセスします。

\(現在、CBT中なので、サービス申請は別途ご案内いたします。\)

![spaceone console &#xB85C;&#xADF8;&#xC778; &#xD654;&#xBA74;](../.gitbook/assets/2020-07-31-3.42.25.png)

下記の通り、Sign In boxの下の_Sign-in using root account credentials_ ボタンをクリックして Domain Administrator 権限でログインします。

![](../.gitbook/assets/2020-07-31-3.43.11.png)

SpaceONEサービス管理者から付与されたID/Passwordでログインします。

![Domain Administrator &#xC811;&#xC18D; &#xD654;&#xBA74;](../.gitbook/assets/2020-07-31-3.44.00.png)

### 一般ユーザーの追加

一般ユーザーを追加してみましょう。追加した後には、追加されたユーザーでSpaceONEにログインしてユーザー別作業ができます。

上部の「Global Navation Bar」で「Identity &gt; User」をクリック

![](../.gitbook/assets/2020-07-31-3.46.38.png)

下記のイメージのように、初めてのログインなので、登録されたユーザーがありません。_Create_ ボタンをクリックしてユーザーを追加します。

![User &amp;gt; Create &#xD074;&#xB9AD;&#xD558;&#xAE30;](../.gitbook/assets/2020-07-31-3.48.11.png)

IDの場合、必須事項で、メール形式で入力してください。他の項目の場合、下記の例をご参照ください。

ユーザ名を入力した後、_check user id_ をクリックして重複しているかチェックしてください。

![&#xC0AC;&#xC6A9;&#xC790; &#xC0DD;&#xC131; &#xD654;&#xBA74;](../.gitbook/assets/2020-07-31-3.50.40.png)

ユーザー登録が終わったらログオフして追加したユーザーでログインします。

![&#xC0AC;&#xC6A9;&#xC790; Profile &#xD654;&#xBA74;](../.gitbook/assets/2020-07-31-3.52.50.png)

より詳しいユーザー管理機能はIDENTITY &gt; USER ページをご参照ください。

{% page-ref page="../identity/user.md" %}

### 一般ユーザーでログイン

追加したユーザーでログインしてサービスを利用しましょう。_Sign in with Google_ ボタンをクリックしてログインします。

![](../.gitbook/assets/2020-08-03-11.07.25.png)

ログインすれば下記のイメージのように、まだデータが収集されてないので、Dashboardには何も表示されていません。

SpaceONEを通してCloud Resourceを収集してみます。まず、Get Started\_ ボタンをクリックしてProjectを作成します。

![Domain Dashboard &#xCD5C;&#xCD08; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-11.12.14.png)

## プロジェクトの作成 <a id="creating-project"></a>

Project作成は_Project Group_ を作成した後できます。

Project ページの左側の_Create_ ボタンをクリックしてProject Groupを作成します。

![Project Group &#xC0DD;&#xC131; &#xBC84;&#xD2BC;](../.gitbook/assets/2020-08-03-11.18.38.png)

下記のように入力してProject Groupを作成します。

![Project Group &#xC0DD;&#xC131; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-11.20.02.png)

作成したProject Group を選択した後、_Create Project_ ボタンをクリックしてProjectを作成します。

![](../.gitbook/assets/2020-08-03-11.31.43.png)

下記のようにProject名を入力して作成します。

![Project &#xC0DD;&#xC131;&#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-11.33.06.png)

下記のイメージのようにProjectの設定が完了されました。

![Project &#xAD00;&#xB9AC; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-11.37.38.png)

より詳しいProject管理機能については、IDENTITY &gt; Projectページをご参照ください。

次に、Service Accountを設定します。

## Service Account作成 <a id="creating-service-account"></a>

Cloud Resourceを収集するために、Credentials\(APIKey Pair\)を入力します。Getting Started GuideではAWSを基準で作成します。

Identity &gt; Service Account &gt; AWSを選択した後_Add_ ボタンをクリックします。

![](../.gitbook/assets/2020-08-03-3.39.10.png)

Add Service Account入力フォームに下記のようにAWS Service Accountを登録するための項目を入力します。

赤い「\*」で表示されているところは必須項目です。その他項目はオプションで、入力しなくても利用に問題ありません。

![](../.gitbook/assets/2020-08-03-3.50.06.png)

全ての項目を入力した後、 Project 項目に事前に作成した Projectを指定した後、下の _Save_ ボタンをクリックします。

![Service Account &#xC0DD;&#xC131; &#xD398;&#xC774;&#xC9C0; &#xB0B4;&#xC758; Project &#xC120;&#xD0DD; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-3.47.38.png)

AWS Service Accountが正しく作成されたら、 Collectorを作成して Cloud Resourceが収集できます。Service Accountの詳しい情報は下記のリンクをご参照ください。

{% page-ref page="../identity/service-account/" %}

## Cloud Resource 収集 <a id="discovering-cloud-resource"></a>

### Collector 作成

Plugin &gt; Collectorに移動し、初めてログインした場合、Collectorないので、情報は表示されません。

Createをクリックして必要な Collectorを選択します。

![](../.gitbook/assets/2020-08-03-4.18.54.png)

下記のように _**Official MarketPlace**_からインストールできるCollector Listが確認できます。ここでは_**aws-ec2**_ Collectorをインストールしてみます。aws-ec2 collectorの _**Create**_をクリックします。

![collector &#xC0DD;&#xC131; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-4.19.39.png)

下記のようにCollector作成Wizardが表示されます。

選択したCollectorの名前とバージョンが選択できます。他のところは特に変更する必要がないので、名前を入力して_**Confirm**_をクリックして作成します。

![Collector &#xC124;&#xC815; &#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-4.22.39.png)

同じ方法でAWS-Cloud-Service Collectorも作成します。下記のように作成されたCollectorが照会できます。

![](../.gitbook/assets/2020-08-03-4.33.11.png)

### Collector実行

次に、Cloud Resourceを収集します。

以前作成したCollectorを選択した後、_**Action &gt; Collect Data**_をクリックすれば、下記のように_**Collect Data**_ 画面が照会できます。 Confirmをクリックして収集を実行します。

![Collect Data &#xC120;&#xD0DD;&#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-4.42.48.png)

![Collector &#xC2E4;&#xD589;&#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-4.41.59.png)

実行中のCollectorの状況は_**Domain Dashboard &gt; Collection**_ 画面で下記のように確認できます。

![Collector Running &#xD654;&#xBA74;](../.gitbook/assets/2020-08-03-4.46.13.png)

収集は約3分以内で完了されます。収集が正しく完了された場合、Inventory &gt; Server, Cloud Serviceから収集されたリソースが照会できます。

![&#xC218;&#xC9D1;&#xB41C; Cloud Resource &#xC815;&#xBCF4;](../.gitbook/assets/2020-08-03-4.51.30.png)

Collectorのより詳しい説明は Plugin &gt; Collector ページをご参照ください。

{% page-ref page="../plugin/collector.md" %}

## Next

ここまではSpaceONEを利用するための基本的な設定です。

次は今まで設定してきた各機能を詳しく見てみます。


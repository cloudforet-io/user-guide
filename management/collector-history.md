description: 作成したCollectorの月別historyを照会及び管理します。
---

# Collector History

## 概要

Collector History ページではSpaceONEのCollector Pluginを通して収集された様々なResourceの月別の変化が照会できます。



## Collector History照会

下記の画面のように、Collector収集した月別Job現況を表示します。ここで Jobとは、作成したCollectorの作業を設定したScheduleに従って遂行した結果を意味します。

![](../.gitbook/assets/image%20%2826%29.png)

メイングラフは収集された Job数を表示します。成功、失敗したJob数がグラフに表示され、点をクリックすれば、下記の表のように、詳細内訳がJobリストに表示されます。

グラフの右上の `< >`  を通して月の移動ができます。



#### Collector History詳細照会

![Collector History &#xC0C1;&#xC138; &#xC870;&#xD68C; ](../.gitbook/assets/image%20%2827%29.png)

 Jobの状態により成功/失敗したJobリストが照会できます。

検索バーを利用して、Collector Historyを通して収集されたjobが、Job ID, Status, Start Time別に検索できます。

![Job &#xAC80;&#xC0C9; &#xD654;&#xBA74;](../.gitbook/assets/image%20%2821%29.png)



Collector Historyページで照会できるJobの情報は次の通りです。

| Title | Description |
| :--- | :--- |
| Job ID | Job id |
| Collector Name | 該当するjobを遂行したcollector名 |
| Status | collectorのjob遂行結果を表す状態 |
| Task \(completed / total\) | 全Taskの内、完了したtask数 |
| Start Time | 該当するJobが開始した時間 |
| Duration | Jobが実行された時間 |



## Jobの詳細情報の照会

![](../.gitbook/assets/image%20%2854%29.png)

Collector historyページのJobリストで個別Jobをクリックすれば、Job managementページから詳細情報が照会できます。

ページの上部にJobを収集したcollectorとcloud providerが表示されます。



#### Task検索

Collector Historyを通して収集されたjobのtaskをservice account, project, status別に検索できます。

![](../.gitbook/assets/image%20%2851%29.png)

#### 

#### Taskリスト照会

ページの下部にJob statusのTaskリストが表示されます。このページで照会できるTaskの情報は次の通りです。

| item | Description |
| :--- | :--- |
| No | task順番 |
| Service account | taskが属しているService Account |
| Project | taskが属しているプロジェクト |
| Status | taskの遂行状態 |
| Created | createされたresource数 |
| Updated | updateされたresource数 |
| Error | task失敗 |
| Start time | task開始時間 |
| Duration | taskが遂行された時間 |



状態がFailureのJobの場合、taskが失敗した原因が下部のError listから確認できます。

![Error List](../.gitbook/assets/image%20%2820%29.png)






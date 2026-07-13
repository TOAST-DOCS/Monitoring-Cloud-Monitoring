<!-- pre-align:aligned sig=fec11ef6ccc5 -->

<a id="monitoring-cloud-monitoring-release-notes"></a>
## Monitoring > Cloud Monitoring > リリースノート { #monitoring-cloud-monitoring-release-notes }

<a id="april-28-2026"></a>
### 2026. 04. 28. { #april-28-2026 }

<a id="april-28-2026-added-a-dashboard-template-feature"></a>
#### ダッシュボードテンプレート機能の追加

ダッシュボード作成時に、あらかじめ構成されたテンプレートを選択して簡単にダッシュボードを作成できます。
サービスごとのテンプレートを選択し、プレビューでウィジェットの構成とレイアウトを確認できます。

<a id="april-28-2026-added-a-dynamic-filter-feature"></a>
#### 動的フィルタ機能の追加

ダッシュボード上部の動的フィルタを使用して、ダッシュボード内の全てのウィジェットのデータを一括でフィルタリングできます。
動的フィルタ管理モーダルでフィルタを追加または変更でき、ウィジェットごとに動的フィルタの適用有無を設定できます。

<a id="april-28-2026-added-an-aggregation-feature"></a>
#### 集計機能の追加

ウィジェット及び通知で収集された指標データを、平均、最小、最大などの集計関数で自動計算して表示できます。
照会期間に応じてデータ間隔が自動調整される際、間隔内の全てのデータを集計して反映するため、データを取りこぼすことなく全体的な流れを把握できます。
指標ごとに集計の使用有無を選択でき、集計を使用しない場合は従来と同様に元のデータを表示します。

<a id="september-23-2025"></a>
### 2025. 09. 23. { #september-23-2025 }

<a id="september-23-2025-release-of-a-new-cloud-monitoring-agent"></a>
#### 新規Cloud Monitoring Agentのリリース

Cloud MonitoringのInstance向け新規Agentがリリースされました。
* [新規Agentインストールガイド](new-instance-metric.md)を参照してインストールできます。

<a id="july-29-2025"></a>
### 2025. 07. 29. { #july-29-2025 }

<!-- TODO: translate body -->

<a id="july-29-2025-added-a-new-service-to-view-metrics"></a>
#### 指標照会が可能なサービスの追加

<!-- TODO: translate body -->

<a id="june-24-2025"></a>
### 2025. 06. 24. { #june-24-2025 }

<a id="june-24-2025-added-a-new-service-to-view-metrics"></a>
#### 指標照会可能サービス追加

Cloud Monitoringで指標照会が可能なサービスを追加しました。
下記のサービスの指標は、指標管理画面で収集設定を行った後、ダッシュボードで確認できます。

* SMS

<a id="june-10-2025"></a>
### 2025. 06. 10. { #june-10-2025 }

<a id="june-10-2025-added-sms-notification-content"></a>
#### SMS通知内容追加

通知送信時にSMSの内容に項目が追加されました。
通知が発生したサービスがInstanceの場合、Instance Name項目が追加されました。

<a id="may-27-2025"></a>
### 2025. 05. 27. { #may-27-2025 }

<a id="may-27-2025-added-a-new-service-to-view-metrics"></a>
#### 指標照会可能サービス追加

Cloud Monitoringで指標照会が可能なサービスを追加しました。
下記のサービスの指標は、指標管理画面で収集設定を行った後、ダッシュボードで確認できます。

* VPC
* Subnet
* Floating IP

<a id="may-4-2025"></a>
### 2025. 03. 04. { #may-4-2025 }

<a id="may-4-2025-add-new-service-to-view-metrics"></a>
#### 指標照会可能なサービスを追加

Cloud Monitoringで指標照会が可能なサービスが追加されました。
下記のサービスの指標は、指標管理画面で収集設定後、ダッシュボードで確認できます。

* Direct Connect

<a id="february-11-2025"></a>
### 2025. 02. 11. { #february-11-2025 }

<a id="february-11-2025-add-new-service-to-view-metrics"></a>
#### 指標照会可能なサービスを追加

Cloud Monitoringで指標照会が可能なサービスが追加されました。
下記のサービスの指標は、指標管理画面で収集設定後、ダッシュボードで確認できます。

* Colocation Gateway
* Load Balancer

<a id="october-29-2024"></a>
### 2024. 10. 29. { #october-29-2024 }

<a id="october-29-2024-apply-permission-segmentation"></a>
#### 権限の細分化を適用

Cloud Monitoringにプロジェクトサービス利用ロールを追加しました。

* Cloud Monitoring ADMIN: Cloud MonitoringサービスCreate(作成), Read(読み取り), Update(更新), Delete(削除)
* Cloud Monitoring VIEWER: Cloud Monitoring Read(読み取り)

<a id="october-29-2024-support-for-custom-webhooks"></a>
#### カスタムWebフックサポート

通知受信グループのカスタムWebフックを使用してCloud Monitoring通知をWebフックで受け取ることができます。

<a id="august-27-2024"></a>
### 2024. 08. 27. { #august-27-2024 }

<a id="august-27-2024-add-new-service-to-view-metrics"></a>
#### 指標照会可能なサービスを追加

Cloud Monitoringで指標照会が可能なサービスが追加されました。 
下記のサービスの指標は、指標管理画面で収集設定後、ダッシュボードで確認できます。

* Transit Hub
* Internet Gateway

<a id="july-23-2024"></a>
### 2024. 07. 23. { #july-23-2024 }

<a id="july-23-2024-bug-fixes"></a>
#### バグ修正

* [Console]ウィジェット及び通知追加/修正ページのテキスト入力ウィンドウでEnterキーを押すと、意図せずに保存が試行される現象を修正しました。

<a id="may-28-2024"></a>
### 2024. 05. 28. { #may-28-2024 }

<a id="may-28-2024-release-of-a-new-service"></a>
#### 新規サービスリリース

Cloud Monitoringは、NHN Cloudのリソースの指標を収集/提供し、異常に対する通知を提供するサービスです。

* Instance、GPU Instance、NCSなどNHN Cloud内のリソースに対するシステム及びサービス指標を収集・提供します。
* 柔軟なダッシュボードの作成及び管理機能により、リソースの状態を簡単に把握できます。
* 組織及びプロジェクトのダッシュボードやモニタリングコンソールに好きな形の指標チャートを構成することができ、指標が特定のしきい値に達した場合、事前に指定した通知受信対象にメール、SMSなどを通じて通知を送るように設定できます。

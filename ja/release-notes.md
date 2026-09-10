<!-- machine_translated: true -->

<!-- pre-align:aligned sig=31661ef58a0f -->

<a id="monitoring-cloud-monitoring-release-notes"></a>
## Monitoring > Cloud Monitoring > リリースノート { #monitoring-cloud-monitoring-release-notes }

<a id="september-29-2026"></a>
## 2026. 09. 29. { #september-29-2026 }

<a id="september-29-2026-added-features"></a>
### 新規機能追加 { #september-29-2026-added-features }

* 異常検知機能の追加
    * Cloud Monitoringが収集した指標データの過去のパターンを学習し、通常とは異なる異常兆候を自動的に検知する異常検知機能が追加されました。
    * 異常検知する指標とリソースを選択して異常検知項目を作成すると、異常検知ダッシュボードのウィジェットチャートで指標値とScore、Scoreのしきい値を確認できます。
    * 作成した異常検知項目で通知を設定し、異常発生時に通知を受信できます。

<a id="july-28-2026"></a>
## 2026. 07. 28. { #july-28-2026 }

<a id="feature-updates"></a>
### 機能改善・変更 { #feature-updates }

* ウィジェットの凡例領域拡張機能を追加
    * ウィジェットの凡例項目が多い場合、凡例領域にマウスを合わせると、拡張された状態の凡例領域が表示されます。
    * 拡張された領域で凡例項目を一目で確認し、任意の項目を選択してデータを簡単にフィルタリングできます。
* 通知メールの発生日時のタイムゾーンを変更
    * 通知メールに表示される発生日時が、UTCから韓国時間(KST)基準に変更されました。

<a id="june-23-2026"></a>
## 2026. 06. 23. { #june-23-2026 }

<a id="added-features"></a>
### 新機能の追加 { #added-features }

* GPU Instance詳細メトリクスの追加
* 新規Cloud Monitoring Agentを通じて、GPU Instanceの詳細メトリクスを収集できます。
* DCGM(Data Center GPU Manager)ベースで、GPU性能、GPU状態、GPUクロックイベント領域のメトリクスを提供します。
    * [新規Agentインストールガイド](new-instance-metric.md)を参照してインストールできます。

<a id="april-28-2026"></a>
## 2026. 04. 28. { #april-28-2026 }

<a id="april-28-2026-added-features"></a>
### 新機能の追加 { #april-28-2026-added-features }

* ダッシュボードテンプレート機能の追加
    * ダッシュボード作成時に、事前に構成されたテンプレートを選択してダッシュボードを簡単に作成できます。
    * サービス別のテンプレートを選択し、プレビューでウィジェットの構成とレイアウトを確認できます。
* 動的フィルタ機能の追加
    * ダッシュボード上部の動的フィルタを使用して、ダッシュボード内の全てのウィジェットのデータを一括でフィルタリングできます。
    * 動的フィルタ管理モーダルでフィルタを追加または変更でき、ウィジェットごとに動的フィルタを適用するかどうかを設定できます。
* 集計機能の追加
* ウィジェット及び通知で収集されたメトリクスデータを、平均、最小、最大などの集計関数で自動計算して表示できます。
    * 検索期間に応じてデータ間隔が自動調整される際、間隔内の全てのデータを集計して反映するため、データを取りこぼすことなく全体的な流れを把握できます。
* メトリクスごとに集計を使用するかどうかを選択でき、集計を使用しない場合は従来と同様に元のデータを表示します。

<a id="september-23-2025"></a>
## 2025. 09. 23. { #september-23-2025 }

<a id="september-23-2025-added-features"></a>
### 新機能の追加 { #september-23-2025-added-features }

* 新規Cloud Monitoring Agentのリリース
    * Cloud Monitoringの新規Instance用Agentがリリースされました。
    * [新規Agentインストールガイド](new-instance-metric.md)を参照してインストールできます。

<a id="july-29-2026"></a>
## 2025. 07. 29. { #july-29-2026 }

<a id="july-29-2026-added-features"></a>
### 新機能の追加 { #july-29-2026-added-features }

* メトリクスを参照可能なサービスの追加
* Cloud Monitoringでメトリクスの参照が可能なサービスが追加されました。
* 以下のサービスのメトリクスは、メトリクス管理画面で収集設定を行った後、ダッシュボードで確認できます。
        * Cloud Functions

<a id="june-24-2025"></a>
## 2025. 06. 24. { #june-24-2025 }

<a id="june-24-2025-added-features"></a>
### 新機能の追加 { #june-24-2025-added-features }

* メトリクスを参照可能なサービスの追加
* Cloud Monitoringでメトリクスの参照が可能なサービスが追加されました。
* 以下のサービスのメトリクスは、メトリクス管理画面で収集設定を行った後、ダッシュボードで確認できます。
        * SMS

<a id="june-10-2025"></a>
## 2025. 06. 10. { #june-10-2025 }

<a id="june-10-2025-feature-updates"></a>
### 機能の改善/変更 { #june-10-2025-feature-updates }

* SMS通知内容の追加
    * 通知の送信時にSMS内容に項目が追加されました。
    * 通知が発生したサービスがInstanceである場合、Instance Name項目が追加されました。

<a id="may-27-2025"></a>
## 2025. 05. 27. { #may-27-2025 }

<a id="may-27-2025-added-features"></a>
### 新機能の追加 { #may-27-2025-added-features }

* メトリクスを参照可能なサービスの追加
* Cloud Monitoringでメトリクスの参照が可能なサービスが追加されました。
* 以下のサービスのメトリクスは、メトリクス管理画面で収集設定を行った後、ダッシュボードで確認できます。
        * VPC
        * Subnet
        * Floating IP

<a id="march-4-2025"></a>
## 2025. 03. 04. { #march-4-2025 }

<a id="march-4-2025-added-features"></a>
### 新機能の追加 { #march-4-2025-added-features }

* メトリクスを参照可能なサービスの追加
* Cloud Monitoringでメトリクスの参照が可能なサービスが追加されました。
* 以下のサービスのメトリクスは、メトリクス管理画面で収集設定を行った後、ダッシュボードで確認できます。
        * Direct Connect

<a id="february-11-2025"></a>
## 2025. 02. 11. { #february-11-2025 }

<a id="february-11-2025-added-features"></a>
### 新機能の追加 { #february-11-2025-added-features }

* メトリクスを参照可能なサービスの追加
* Cloud Monitoringでメトリクスの参照が可能なサービスが追加されました。
* 以下のサービスのメトリクスは、メトリクス管理画面で収集設定を行った後、ダッシュボードで確認できます。
        * Colocation Gateway
        * Load Balancer

<a id="october-29-2024"></a>
## 2024. 10. 29. { #october-29-2024 }

<a id="october-29-2024-added-features"></a>
### 新機能の追加 { #october-29-2024-added-features }

* カスタムWebhookのサポート
    * 通知受信グループのカスタムWebhookを使用して、Cloud Monitoringの通知をWebhookで受け取ることができます。

<a id="october-29-2024-feature-updates"></a>
### 機能の改善/変更 { #october-29-2024-feature-updates }

* 権限の細分化を適用
    * Cloud Monitoringにプロジェクトサービス利用ロールが追加されました。
    * Cloud Monitoring ADMIN: Cloud MonitoringサービスのCreate(作成)、Read(読み取り)、Update(更新)、Delete(削除)
    * Cloud Monitoring VIEWER: Cloud MonitoringサービスのRead(読み取り)

<a id="august-27-2024"></a>
## 2024. 08. 27. { #august-27-2024 }

<a id="august-27-2024-added-features"></a>
### 新機能の追加 { #august-27-2024-added-features }

* メトリクスを参照可能なサービスの追加
* Cloud Monitoringでメトリクスの参照が可能なサービスが追加されました。
* 以下のサービスのメトリクスは、メトリクス管理画面で収集設定を行った後、ダッシュボードで確認できます。
        * Transit Hub
        * Internet Gateway

<a id="july-23-2024"></a>
## 2024. 07. 23. { #july-23-2024 }

<a id="bug-fixes"></a>
### バグ修正 { #bug-fixes }

* [コンソール] ウィジェット及び通知の追加/変更ページのテキスト入力ウィンドウで、Enterキー入力時に意図せず保存が試行される現象を修正しました。

<a id="may-28-2024"></a>
## 2024. 05. 28. { #may-28-2024 }

<a id="may-28-2024-added-features"></a>
### 新機能の追加 { #may-28-2024-added-features }

* 新規サービスのリリース
* Cloud Monitoringは、NHN Cloudのリソースメトリクスを収集・提供し、異常が発生した際に通知を提供するサービスです。
* Instance、GPU Instance、NCSなど、NHN Cloud内のリソースのシステム及びサービスメトリクスを収集、提供します。
    * 柔軟なダッシュボードの作成及び管理機能により、リソースの状態を簡単に把握できます。
* 組織及びプロジェクトダッシュボード、またはモニタリングコンソールで任意の形式のメトリクスチャートを構成でき、メトリクスが特定のしきい値に到達した場合に、あらかじめ指定した通知受信対象にメール、SMSなどで通知を送信するように設定できます。

## Monitoring > Cloud Monitoring > リリースノート

### 2024. 10. 29.

#### 権限の細分化を適用
Cloud Monitoringにプロジェクトサービス利用ロールを追加しました。
- Cloud Monitoring ADMIN: Cloud MonitoringサービスCreate(作成), Read(読み取り), Update(更新), Delete(削除)
- Cloud Monitoring VIEWER: Cloud Monitoring Read(読み取り)

#### カスタムWebフックサポート
通知受信グループのカスタムWebフックを使用してCloud Monitoring通知をWebフックで受け取ることができます。

### 2024. 07. 25.

#### 新規サービスリリース
Cloud Monitoringは、NHN Cloudのリソースの指標を収集/提供し、異常に対する通知を提供するサービスです。
* Instance、GPU Instance、NCSなどNHN Cloud内のリソースに対するシステム及びサービス指標を収集・提供します。
* 柔軟なダッシュボードの作成及び管理機能により、リソースの状態を簡単に把握できます。
* 組織及びプロジェクトのダッシュボードやモニタリングコンソールに好きな形の指標チャートを構成することができ、指標が特定のしきい値に達した場合、通知の受信対象を指定し、メール、SMSなどを通じて通知を送るように設定できます。

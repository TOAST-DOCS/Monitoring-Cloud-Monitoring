## Monitoring > Cloud Monitoring > リリースノート

### 2025. 03. 04.

#### 指標照会可能なサービスを追加

Cloud Monitoringで指標照会が可能なサービスが追加されました。
下記のサービスの指標は、指標管理画面で収集設定後、ダッシュボードで確認できます。
* Direct Connect

### 2025. 02. 11.

#### 指標照会可能なサービスを追加

Cloud Monitoringで指標照会が可能なサービスが追加されました。
下記のサービスの指標は、指標管理画面で収集設定後、ダッシュボードで確認できます。
* Colocation Gateway
* Load Balancer

### 2024. 10. 29.

#### 権限の細分化を適用
Cloud Monitoringにプロジェクトサービス利用ロールを追加しました。
- Cloud Monitoring ADMIN: Cloud MonitoringサービスCreate(作成), Read(読み取り), Update(更新), Delete(削除)
- Cloud Monitoring VIEWER: Cloud Monitoring Read(読み取り)

#### カスタムWebフックサポート
通知受信グループのカスタムWebフックを使用してCloud Monitoring通知をWebフックで受け取ることができます。

### 2024. 08. 27.

#### 指標照会可能なサービスを追加

Cloud Monitoringで指標照会が可能なサービスが追加されました。 
下記のサービスの指標は、指標管理画面で収集設定後、ダッシュボードで確認できます。
* Transit Hub
* Internet Gateway

### 2024. 07. 23.

#### バグ修正
* [Console]ウィジェット及び通知追加/修正ページのテキスト入力ウィンドウでEnterキーを押すと、意図せずに保存が試行される現象を修正しました。

### 2024. 05. 28.

#### 新規サービスリリース
Cloud Monitoringは、NHN Cloudのリソースの指標を収集/提供し、異常に対する通知を提供するサービスです。
* Instance、GPU Instance、NCSなどNHN Cloud内のリソースに対するシステム及びサービス指標を収集・提供します。
* 柔軟なダッシュボードの作成及び管理機能により、リソースの状態を簡単に把握できます。
* 組織及びプロジェクトのダッシュボードやモニタリングコンソールに好きな形の指標チャートを構成することができ、指標が特定のしきい値に達した場合、事前に指定した通知受信対象にメール、SMSなどを通じて通知を送るように設定できます。

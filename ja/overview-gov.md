## Monitoring > Cloud Monitoring > 概要
**Monitoring > Cloud Monitoring**サービスでは、InstanceサーバーをはじめとするNHN Cloud内のリソースに対するシステム/サービス指標を収集、提供します。
組織及びプロジェクトダッシュボード、モニタリングコンソールに好きな形の指標チャートを構成することができ、
指標が特定のしきい値に達した場合、通知の受信対象を指定し、メール、SMSなどの方法で通知を送るように設定できます。

## 提供機能
### Compute > Instanceサーバーモニタリング
インスタンスサーバーの場合、Cloud Monitoringは各インスタンスサーバーに設置されたCloud Monitoring Agentでシステム指標を収集します。
基本的にAgentはインスタンスのイメージに含まれているため、インスタンス駆動時に自動的に収集を開始します。

### 指標ダッシュボードの提供
**Compute > Instance**で作成したサーバーインスタンスの各種システム指標及びNHN Cloud内のリソースに関するチャートを提供し、各サーバーの状態を把握できます。
指標ウィジェットを選択してダッシュボードに配置することができ、複数のダッシュボードを作成して目的に応じて管理できます。

指標は1分単位で収集され、最大52週間保管されます。

### 指標通知条件設定
収集された指標のしきい値を設定することで、NHN Cloudのリソースを常に監視し、異常な兆候を把握きます。
例えば、インスタンスサーバーのCPU使用率が90%を超えた場合、特定のNICの使用量が1000ppsを超えた場合など、サーバーの状態を把握できる様々な監視項目を提供します。

### 通知方法の選択：メール、SMS
設定した通知条件を満たす状況が発生したとき、どのような方法で通知を受けるかを選択できます。
メールやSMSで通知を受けることができます。

## 用語説明
| 用語     | 説明                                                                                               |
|----------|----------------------------------------------------------------------------------------------------|
| 指標     | Cloud Monitoringで収集する各リソースの指標です。インスタンスサーバーの場合、CPU使用率、平均負荷(load average)1m、メモリ使用量などがあります。 | 
| ダッシュボード   | 指標ウィジェットの束です。ユーザーが好きなようにウィジェットを配置することができ、複数のダッシュボードを作成し、目的に応じて管理できます。                        |                     
| 通知受信グループ | イベントが発生したときに通知を受け取るユーザーのリストです。                                                                      |                                                                       
| 通知グループ  | しきい値を設定し、どのインスタンスを監視するか、イベント発生時にどの通知受信グループに通知を送るかを指定します。通知条件設定｜各指標の閾値を設定します。                                     |                                      
| 通知条件設定 | 各指標のしきい値の詳細設定です。                                                                                |                                                                                 
## Monitoring > Cloud Monitoring > Instance新規メトリクス連携ガイド

## 概要

Cloud MonitoringサービスでInstanceの詳細なメトリクスを収集するには、新しいAgentをインストールする必要があります。
新しいAgentは既存のAgentとは別に動作し、より正確で詳細なインスタンスのメトリクスを提供します。

> [注意]
> オートスケールグループに属するインスタンスの場合、オートスケーリング機能が正常に動作しない可能性があります。

全体の流れは以下の通りです。
1. 新規Agentのインストール
2. 旧Agentの削除（任意）

## 新規Agentインストールガイド

### LinuxインスタンスへのAgentインストール

#### インストールスクリプト
```bash
rm -f ./install-nhncloud-telegraf.sh
curl -s -o install-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/install-nhncloud-telegraf.sh'
chmod 755 ./install-nhncloud-telegraf.sh
sudo ./install-nhncloud-telegraf.sh
```

#### インストールの確認
```bash
sudo systemctl status nhncloud-telegraf
```

### WindowsインスタンスへのAgentインストール
* PowerShellを管理者権限で実行
   - スタートメニューで**PowerShell**を検索します。
   - **Windows PowerShell**を右クリックし、**管理者として実行**を選択します。

#### インストールスクリプト
```powershell
Remove-Item install-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/install-nhncloud-telegraf.ps1' -OutFile 'install-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File install-nhncloud-telegraf.ps1
```

#### インストールの確認
```powershell
Get-Service -Name "nhncloud-telegraf"
```

## 旧Agent削除ガイド（任意）

> [参考]
> 新規Agentと旧Agentは、同時に使用することも可能です。

既存のSystem Monitoring Agentをアンインストールするための削除ガイドです。新規Agentと旧Agentは、同時にインストールされていても問題なく動作します。

### 削除時の注意事項
- **削除前の必須確認事項**：新規Agentが正常にインストールされ、動作しているかを確認

### Linuxインスタンスの旧Agent削除

#### 削除スクリプト
```bash
curl -s -o uninstall-sysmon-agent.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-sysmon-agent.sh'
chmod 755 ./uninstall-sysmon-agent.sh
sudo ./uninstall-sysmon-agent.sh
```

#### 削除の確認
* 旧Agentのサービス状態を確認（サービスが存在しないのが正常な状態です）
```bash
sudo systemctl status toast-sysmon
```

### Windowsインスタンスの旧Agent削除
#### 削除スクリプト
```powershell
& "C:\Program Files (x86)\NHN\TOAST\uninst.exe"
```

#### 削除の確認
* 旧Agentのプロセス終了を確認
```powershell
Get-Process -Name "toastmon" -ErrorAction SilentlyContinue
```

### 新規Agentの削除（必要な場合）

#### Linuxインスタンスの新規Agent削除

##### 削除スクリプト
```bash
rm -f ./uninstall-nhncloud-telegraf.sh
curl -s -o uninstall-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-nhncloud-telegraf.sh'
chmod 755 ./uninstall-nhncloud-telegraf.sh
sudo ./uninstall-nhncloud-telegraf.sh
```

#### Windowsインスタンスの新規Agent削除

##### 削除スクリプト
```powershell
Remove-Item uninstall-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/uninstall-nhncloud-telegraf.ps1' -OutFile 'uninstall-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File uninstall-nhncloud-telegraf.ps1
```

## Metric Dictionary

|メトリクス名|リソース名|デフォルトの凡例(Legend)|単位(Unit)|
|-------|-------|------|------|
|CPU使用率 (%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|CPUコア数|CPU (New)|{{nhncloud_instance_id}}|数値|
|コア別CPU使用率 (%)|CPU (New)|{{nhncloud_instance_id}} cpu={{cpu}}|パーセント(0-100)|
|CPU平均負荷(1m)|CPU (New)|{{nhncloud_instance_id}} - 1m|数値|
|CPU平均負荷(5m)|CPU (New)|{{nhncloud_instance_id}} - 5m|数値|
|CPU平均負荷(15m)|CPU (New)|{{nhncloud_instance_id}} - 15m|数値|
|CPU詳細(user) (%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|CPU詳細(nice) (%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|CPU詳細(system) (%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|CPU詳細(iowait) (%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|CPU詳細(steal) (%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|メモリ使用率 (%)|Memory (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|メモリ詳細(used) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(available) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(free) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(cached) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(buffered) (Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|ディスク使用率 (%)|Disk (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|デバイス別ディスク使用率 (%)|Disk (New)|{{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}}|パーセント(0-100)|
|ディスク読み取り (B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|バイト/秒(bytes/s)|
|ディスク書き込み (B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|バイト/秒(bytes/s)|
|デバイス別ディスク読み取り (B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|バイト/秒(bytes/s)|
|デバイス別ディスク書き込み (B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|バイト/秒(bytes/s)|
|デバイス別処理中のタスク数|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|数値|
|デバイス別IO使用率 (%)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|パーセント(0-100)|
|ネットワークデータ受信量 (B/s)|Network (New)|{{nhncloud_instance_id}}|バイト/秒(bytes/s)|
|ネットワークデータ送信量 (B/s)|Network (New)|{{nhncloud_instance_id}}|バイト/秒(bytes/s)|
|デバイス別ネットワークデータ受信量 (B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|バイト/秒(bytes/s)|
|デバイス別ネットワークデータ送信量 (B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|バイト/秒(bytes/s)|
|ネットワークデータ受信量 (bps)|Network (New)|{{nhncloud_instance_id}}|ビット/秒(bit/s)|
|ネットワークデータ送信量 (bps)|Network (New)|{{nhncloud_instance_id}}|ビット/秒(bit/s)|
|デバイス別ネットワークデータ受信量 (bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|ビット/秒(bit/s)|
|デバイス別ネットワークデータ送信量 (bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|ビット/秒(bit/s)|
|ネットワークパケット受信数 (pps)|Network (New)|{{nhncloud_instance_id}}|パケット/秒(packets/s)|
|ネットワークパケット送信数 (pps)|Network (New)|{{nhncloud_instance_id}}|パケット/秒(packets/s)|
|デバイス別ネットワークパケット受信数 (pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|パケット/秒(packets/s)|
|デバイス別ネットワークパケット送信数 (pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|パケット/秒(packets/s)|
|稼働時間 (s)|System (New)|{{nhncloud_instance_id}}|ミリ秒(second)|
|スワップ使用率 (%)|Swap (New)|{{nhncloud_instance_id}}|パーセント(0-100)|
|スワップ使用量(used) (Bytes)|Swap (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|スワップ使用量(free) (Bytes)|Swap (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|スワップ使用量(total) (Bytes)|Swap (New)|{{nhncloud_instance_id}}|バイト(bytes)|

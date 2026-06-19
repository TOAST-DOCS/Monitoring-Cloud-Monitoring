## Monitoring > Cloud Monitoring > Instance 新規メトリクス連携ガイド

## 概要

Cloud Monitoring サービスで Instance の詳細メトリクスを収集するには、新規 Agent をインストールする必要があります。
新規 Agent は既存의 Agent とは別個で動作し、より正確で詳細なインスタンスメトリクスを提供します。

> [注意]
> オートスケーリンググループに属するインスタンスの場合、オートスケーリング機能が正常に動作しないことがあります。

全体の進行手順は次の通りです。
1. 新規 Agent のインストール
2. 既存の Agent の削除(任意)

## 新規 Agent インストールガイド

### Linux インスタンス Agent インストール

#### インストールスクリプト
```bash
rm -f ./install-nhncloud-telegraf.sh
curl -s -o install-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/install-nhncloud-telegraf.sh'
chmod 755 ./install-nhncloud-telegraf.sh
sudo ./install-nhncloud-telegraf.sh
```

#### インストール確認
```bash
sudo systemctl status nhncloud-telegraf
```

### Windows インスタンス Agent インストール
* PowerShell を管理者権限で実行
   - スタートメニューから **PowerShell** を検索します。
   - **Windows PowerShell** を右クリックし、**管理者として実行**を選択します。

#### インストールスクリプト
```powershell
Remove-Item install-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/install-nhncloud-telegraf.ps1' -OutFile 'install-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File install-nhncloud-telegraf.ps1
```

#### インストール確認
```powershell
Get-Service -Name "nhncloud-telegraf"
```

## 既存の Agent 削除ガイド(任意)

> [参考]
> 新規 Agent と既存の Agent を同時に使用することもできます。

既存の System Monitoring Agent を削除するガイドです。新規 Agent と既存の Agent は、同時にインストールされていても問題なく動作します。

### 削除時の注意事項
既存の Agent を削除する前に、新規 Agent が正常にインストールされて動作しているか必ず確認します。

### Linux インスタンス 既存の Agent 削除

#### 削除スクリプト
```bash
curl -s -o uninstall-sysmon-agent.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-sysmon-agent.sh'
chmod 755 ./uninstall-sysmon-agent.sh
sudo ./uninstall-sysmon-agent.sh
```

#### 削除確認
既存の Agent のサービス状態を確認します(サービスがない状態が正常です)。
```bash
sudo systemctl status toast-sysmon
```

### Windows インスタンス 既存の Agent 削除
#### 削除スクリプト
```powershell
& "C:\Program Files (x86)\NHN\TOAST\uninst.exe"
```

#### 削除確認
既存の Agent プロセスが終了したか確認します。
```powershell
Get-Process -Name "toastmon" -ErrorAction SilentlyContinue
```

### 新規 Agent 削除(必要な場合)

#### Linux インスタンス 新規 Agent 削除

##### 削除スクリプト
```bash
rm -f ./uninstall-nhncloud-telegraf.sh
curl -s -o uninstall-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-nhncloud-telegraf.sh'
chmod 755 ./uninstall-nhncloud-telegraf.sh
sudo ./uninstall-nhncloud-telegraf.sh
```

#### Windowsインスタンス新規Agent削除

##### 削除スクリプト
```powershell
Remove-Item uninstall-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/uninstall-nhncloud-telegraf.ps1' -OutFile 'uninstall-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File uninstall-nhncloud-telegraf.ps1
```

## Metric Dictionary

|メトリクス名|リソース名|デフォルト凡例(Legend)|単位(Unit)|
|-------|-------|------|------|
|CPU 使用率(%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|CPU コア数|CPU (New)|{{nhncloud_instance_id}}|数値|
|コア別 CPU 使用率(%)|CPU (New)|{{nhncloud_instance_id}} cpu={{cpu}}|パーセント(0～100)|
|CPU 平均負荷(1m)|CPU (New)|{{nhncloud_instance_id}} - 1m|数値|
|CPU 平均負荷(5m)|CPU (New)|{{nhncloud_instance_id}} - 5m|数値|
|CPU 平均負荷(15m)|CPU (New)|{{nhncloud_instance_id}} - 15m|数値|
|CPU 詳細(user)(%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|CPU 詳細(nice)(%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|CPU 詳細(system)(%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|CPU 詳細(iowait)(%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|CPU 詳細(steal)(%)|CPU (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|メモリ使用率(%)|Memory (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|メモリ詳細(used)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(available)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(free)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(cached)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|メモリ詳細(buffered)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|ディスク使用率(%)|Disk (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|デバイス別ディスク使用率(%)|Disk (New)|{{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}}|パーセント(0～100)|
|ディスク読み取り(B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|毎秒バイト(bytes/s)|
|ディスク書き込み(B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|毎秒バイト(bytes/s)|
|デバイス別ディスク読み取り(B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|毎秒バイト(bytes/s)|
|デバイス別ディスク書き込み(B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|毎秒バイト(bytes/s)|
|デバイス別処理中のタスク数|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|数値|
|デバイス別 IO 使用率(%)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|パーセント(0～100)|
|ネットワークデータ受信(B/s)|Network (New)|{{nhncloud_instance_id}}|毎秒バイト(bytes/s)|
|ネットワークデータ送信(B/s)|Network (New)|{{nhncloud_instance_id}}|毎秒バイト(bytes/s)|
|デバイス別ネットワークデータ受信(B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|毎秒バイト(bytes/s)|
|デバイス別ネットワークデータ送信(B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|毎秒バイト(bytes/s)|
|ネットワークデータ受信(bps)|Network (New)|{{nhncloud_instance_id}}|毎秒ビット(bit/s)|
|ネットワークデータ送信(bps)|Network (New)|{{nhncloud_instance_id}}|毎秒ビット(bit/s)|
|デバイス別ネットワークデータ受信(bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|毎秒ビット(bit/s)|
|デバイス別ネットワークデータ送信(bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|毎秒ビット(bit/s)|
|ネットワークパケット受信(pps)|Network (New)|{{nhncloud_instance_id}}|毎秒パケット(packets/s)|
|ネットワークパケット送信(pps)|Network (New)|{{nhncloud_instance_id}}|毎秒パケット(packets/s)|
|デバイス別ネットワークパケット受信(pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|毎秒パケット(packets/s)|
|デバイス別ネットワークパケット送信(pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|毎秒パケット(packets/s)|
|稼働時間(s)|System (New)|{{nhncloud_instance_id}}|時間(second)|
|スワップ使用率(%)|Swap (New)|{{nhncloud_instance_id}}|パーセント(0～100)|
|スワップ使用量(used)(Bytes)|Swap (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|スワップ使用量(free)(Bytes)|Swap (New)|{{nhncloud_instance_id}}|バイト(bytes)|
|スワップ使用量(total)(Bytes)|Swap (New)|{{nhncloud_instance_id}}|バイト(bytes)|

## GPU Instance Metric Dictionary

> [参考]
> GPUメトリクスは、GPU InstanceでDCGM(Data Center GPU Manager)ベースで収集され、新規Cloud Monitoring AgentがインストールされたGPU Instanceでのみ確認できます。
> GPUモデル(V100/A100/T4)およびドライバーのバージョンによっては、一部のメトリクスが収集されない場合があります。

|メトリクス名|リソース名|デフォルト凡例(Legend)|単位(Unit)|
|-------|-------|------|------|
|GPU使用率(%)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|パーセント(0～100)|
|GPUメモリ使用率(%)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|パーセント(0～100)|
|GPUメモリ帯域幅使用率(%)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|パーセント(0～100)|
|GPU電力使用量(W)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|ワット(W)|
|GPU温度(°C)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|摂氏(°C)|
|GPUメモリ温度(°C)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|摂氏(°C)|
|SMクロック(MHz)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|メガヘルツ(MHz)|
|メモリクロック(MHz)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|メガヘルツ(MHz)|
|エンコーダー使用率(%)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|パーセント(0～100)|
|デコーダー使用率(%)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|パーセント(0～100)|
|GPU空きメモリ(MiB)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|メビバイト(MiB)|
|GPU予約メモリ(MiB)|GPU性能|{{nhncloud_instance_id}} - gpu={{gpu}}|メビバイト(MiB)|
|PCIe再送レート(count/s)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒カウント(count/s)|
|XIDエラー|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|ECCシングルビットエラー - 累積(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|ECCシングルビットエラー - 変動(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|ECCダブルビットエラー - 累積(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|ECCダブルビットエラー - 変動(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|隔離ページ - SBE(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|隔離ページ - DBE(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|隔離待機ページ(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|リマッピング行 - 訂正可能(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|リマッピング行 - 訂正不可(count)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|リマッピング失敗の有無|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|数値|
|NVLink CRC Flitエラーレート(count/s)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒カウント(count/s)|
|NVLink CRC Dataエラーレート(count/s)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒カウント(count/s)|
|NVLink Replayエラーレート(count/s)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒カウント(count/s)|
|NVLink Recoveryエラーレート(count/s)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒カウント(count/s)|
|NVLink帯域幅 - Total(KiB/s)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒キビバイト(KiB/s)|
|NVLink帯域幅 - L0(B/s)|GPU状態|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒バイト(bytes/s)|
|電力スロットリング比率(µs/s)|GPUクロックイベント|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒マイクロ秒(µs/s)|
|温度スロットリング比率(µs/s)|GPUクロックイベント|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒マイクロ秒(µs/s)|
|ボード制限スロットリング比率(µs/s)|GPUクロックイベント|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒マイクロ秒(µs/s)|
|低使用率スロットリング比率(µs/s)|GPUクロックイベント|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒マイクロ秒(µs/s)|
|同期ブーストスロットリング比率(µs/s)|GPUクロックイベント|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒マイクロ秒(µs/s)|
|信頼性スロットリング比率(µs/s)|GPUクロックイベント|{{nhncloud_instance_id}} - gpu={{gpu}}|毎秒マイクロ秒(µs/s)|

### GPU Instanceフィルタ(Filter)

|フィルタ名|説明|
|------|------|
|リージョン|GPU Instanceが配置されているリージョン|
|インスタンス|GPU Instanceの名前|
|GPU|インスタンス内のGPUデバイス番号|

### GPU Instance凡例(Legend)

|凡例名|説明|
|------|------|
|nhncloud_instance_id|GPU Instanceの名前|
|GPU|インスタンス内のGPUデバイス番号|

## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- NHN Cloud内のサービスに対するモニタリングのための指標を定義したリストです。
- 指標辞典を通じてモニタリング対象サービスの指標を確認し、理解できます。
- ウィジェット構成時に必要な指標を検索して使用できます。詳細は[コンソール使用ガイド](console-guide-gov.md)を参照してください。
- **Metric List**で各サービス別の指標の事前リストを確認できます。

### フィルタ(Filter)
- 指標に対してフィルタを適用できます。
- フィルタを適用すると、そのフィルタに合う指標だけが表示されます。
  - 例えば、リージョンフィルターにkr1を適用すると、指標のうちkr1リージョンに該当する指標のみ表示されます。
- 共通フィルタは次のとおりです。

| フィルタ名 | 説明         | 値                            |
|-----|--------------|------------------------------|
| リージョン | NHN Cloudリージョン | kr1:韓国(パンギョ), kr2:韓国(ピョンチョン) |

### 凡例(Legend)
- 指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。
  - 例えば、凡例に{{nhncloud_region}}を適用すると、各指標の名前がkr1、kr2のように地域名で表示されます。
- 共通凡例は次のとおりです。

| フィルタ名           | 説明         | 値                            |
|-----------------|--------------|------------------------------|
| nhncloud_region | NHN Cloudリージョン | kr1:韓国(パンギョ), kr2:韓国(ピョンチョン) |

## Instance
- NHN Cloudで提供するインスタンスサーバー指標についての辞書です。

### Metric List
| 韓国語            | リソース名  | 基本凡例(Legend)                                                              | 単位(Unit)         |
|------------------|---------|----------------------------------------------------------------------------|------------------|
| CPU使用率        | CPU     |                                                                            | パーセンテージ(0-100)       |
| コア別CPU使用率    | CPU     | {{nhncloud_instance_id}} cpu={{cpu}}                                       | パーセンテージ(0-100)       |
| CPU詳細(user)     | CPU     | {{nhncloud_instance_id}}                                                   | 比率(0.00 - 1.00)  |
| CPU詳細(nice)     | CPU     | {{nhncloud_instance_id}}                                                   | 比率(0.00 - 1.00)  |
| CPU詳細(system)   | CPU     | {{nhncloud_instance_id}}                                                   | 比率(0.00 - 1.00)  |
| CPU詳細(iowait)   | CPU     | {{nhncloud_instance_id}}                                                   | 比率(0.00 - 1.00)  |
| CPU平均負荷(1m)    | CPU     | {{nhncloud_instance_id}}                                                   | 数字             |
| CPU平均負荷(5m)    | CPU     | {{nhncloud_instance_id}}                                                   | 数字             |
| CPU平均負荷(15m)   | CPU     | {{nhncloud_instance_id}}                                                   | 数字             |
| ディスク使用率        | Disk    | {{nhncloud_instance_id}}                                                   | 比率(0.00 - 1.00)  |
| マウント別ディスク使用率   | Disk    | {{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}} | 比率(0.00 - 1.00)  |
| ディスクの読み取り          | Disk    | {{nhncloud_instance_id}}                                                   | 毎秒バイト(bytes/s)  |
| ディスク書き込み          | Disk    | {{nhncloud_instance_id}}                                                   | 毎秒バイト(bytes/s)  |
| 装置別ディスク読み取り      | Disk    | {{nhncloud_instance_id}} fstype={{fstype}}                                 | 毎秒バイト(bytes/s)  |
| 装置別ディスク書き込み      | Disk    | {{nhncloud_instance_id}} fstype={{fstype}}                                 | 毎秒バイト(bytes/s)  |
| メモリ使用率        | Memory  | {{nhncloud_instance_id}}                                                   | パーセンテージ(0-100)       |
| メモリ詳細(used)     | Memory  | {{nhncloud_instance_id}}                                                   | バイト(bytes)       |
| メモリ詳細(buffered) | Memory  | {{nhncloud_instance_id}}                                                   | バイト(bytes)       |
| メモリ詳細(cached)   | Memory  | {{nhncloud_instance_id}}                                                   | バイト(bytes)       |
| メモリ詳細(free)     | Memory  | {{nhncloud_instance_id}}                                                   | バイト(bytes)       |
| ネットワークデータ送信    | Network | {{nhncloud_instance_id}}                                                   | 毎秒バイト(bytes/s)  |
| ネットワークデータ受信    | Network | {{nhncloud_instance_id}}                                                   | 毎秒バイト(bytes/s)  |
| 装置別ネットワークデータ送信 | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 毎秒バイト(bytes/s)  |
| 装置別ネットワークデータ受信 | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 毎秒バイト(bytes/s)  |
| ネットワークパケット送信     | Network | {{nhncloud_instance_id}}                                                   | 毎秒パケット(packets/s) |
| ネットワークパケット受信     | Network | {{nhncloud_instance_id}}                                                   | 毎秒パケット(packets/s) |
| 装置別ネットワークパケット送信 | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 毎秒パケット(packets/s) |
| 装置別ネットワークパケット受信 | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 毎秒パケット(packets/s) |
| プロセス数        | Process | {{nhncloud_instance_id}}                                                   | 数字             |
| スワップ使用量(used)     | Swap    | {{nhncloud_instance_id}}                                                   | バイト(bytes)       |
| スワップ使用量(free)     | Swap    | {{nhncloud_instance_id}}                                                   | バイト(bytes)       |
| スワップ使用量(total)    | Swap    | {{nhncloud_instance_id}}                                                   | バイト(bytes)       |
| スワップ使用率         | Swap    | {{nhncloud_instance_id}}                                                   | 比率(0.00 - 1.00)  |

### Instanceフィルタ(Filter)
- Instance指標に対してフィルタを適用できます。
- フィルタを適用すると、そのフィルタに合う指標だけが表示されます。

| フィルタ名 | 説明                                    |
|------|-----------------------------------------|
| インスタンス | NHN Cloud Instanceサービスで使用中のインスタンスの名前 |

### Instance凡例(Legend)
- Instance指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。

| 凡例名                 | 説明                |
|----------------------|---------------------|
| nhncloud_instance_id | インスタンスの名前          |
| cpu                  | インスタンスのCPU番号      |
| device               | インスタンスのディスク装置      |
| fstype               | インスタンスのファイルシステムの種類   |
| path                 | インスタンスのディスクマウントパス  |
| interface            | インスタンスのネットワークインターフェイス名 |

## NHN Container Service(NCS)
- NCSの指標についての辞書です。

### Metric List
| 韓国語         | リソース名 | 基本凡例(Legend)                                                            | 単位(Unit)        |
|---------------|------|--------------------------------------------------------------------------|-----------------|
| CPU使用率     | NCS  | {{label_ncs_container_nhncloud_com_workload_id}} container={{container}} | パーセンテージ(0-100)      |
| ワークロードに割り当てられたCPU | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 数字            |
| メモリ使用率     | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | パーセンテージ(0-100)      |
| ワークロードに割り当てられたメモリ | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | メビバイト(MiB)      |
| GPU使用率     | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | パーセンテージ(0-100)      |
| GPUメモリ使用率 | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | パーセンテージ(0-100)      |
| GPU電力使用量  | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | メガワット(mW)        |
| GPU温度      | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 摂氏(℃)           |
| ワークロードに割り当てられたGPU | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 数字            |
| ネットワークデータ受信 | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 毎秒バイト(bytes/s) |
| ネットワークデータ送信 | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 毎秒バイト(bytes/s) |
| ディスク使用率     | NCS  | {{workload_id}} {{type}}                                                 | パーセンテージ(0-100)      |
| 有効化状態別作業数 | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 数字            |
| コンテナのプロセス数 | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 数字            |

### NCS Filter
- NCS指標に対してフィルタを適用できます。
- フィルタを適用すると、そのフィルタに合う指標だけが表示されます。

| フィルタ名 | 説明                             |
|------|----------------------------------|
| ワークロード | NHN Cloud NCS内で使用中のワークロードの名前 |
| タイプ | ストレージ種類                        |


### NCS Legend
- NCS指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。

| 凡例名                                         | 説明                           |
|----------------------------------------------|--------------------------------|
| label_ncs_container_nhncloud_com_workload_id | NHN Cloud NCSで使用中のワークロードの名前 |
| workload_id                                  | NHN Cloud NCSで使用中のワークロードの名前 |
| type                                         | ストレージ種類                      |
| container                                    | コンテナ名                     |

## GPU
- NHN Cloudが提供するGPUサービスの指標についての辞書です。

### Metric List
| 韓国語       | リソース名 | 基本凡例(Legend) | 単位(Unit)   |
|-------------|------|---------------|------------|
| GPU使用率   | GPU  | なし           | パーセンテージ(0-100) |
| GPU温度    | GPU  | なし           | 摂氏(℃)      |
| GPUメモリ使用率 | GPU  | なし           | パーセンテージ(0-100) |
| GPU電力使用量 | GPU  | なし           | ワット(W)      |

### GPUフィルタ(Filter)
- GPU指標に対してフィルタを適用できます。
- フィルタを適用すると、そのフィルタに合う指標だけが表示されます。

| フィルタ名 | 説明         |
|------|--------------|
| インスタンス | GPUインスタンスの名前 |

### GPU凡例(Legend)
- GPU指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。

| フィルタ名                | 説明         |
|----------------------|--------------|
| nhncloud_instance_id | GPUインスタンスの名前 |

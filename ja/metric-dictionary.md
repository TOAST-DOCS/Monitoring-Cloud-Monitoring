## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- NHN Cloud内のサービスに対するモニタリングのための指標を定義したリストです。
- 指標辞典を通じてモニタリング対象サービスの指標を確認し、理解できます。
- ウィジェット構成時に必要な指標を検索して使用できます。詳細は[コンソール使用ガイド](console-guide.md)を参照してください。
- **Metric List**で各サービス別の指標の事前リストを確認できます。

### フィルタ(Filter)
- 指標に対してフィルタを適用できます。
- フィルタを適用すると、そのフィルタに合う指標だけが表示されます。
  - 例えば、リージョンフィルターにkr1を適用すると、指標のうちkr1リージョンに該当する指標のみ表示されます。
- 共通フィルタは次のとおりです。

| フィルタ名 | 説明         | 値                                                                |
|-----|--------------|--------------------------------------------------------------------|
| リージョン | NHN Cloudリージョン | kr1:韓国(パンギョ), kr2:韓国(ピョンチョン), kr3:韓国(光州), us1:米国(カリフォルニア), jp1:日本(東京) |

### 凡例(Legend)
- 指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。
  - 例えば、凡例に{{nhncloud_region}}を適用すると、各指標の名前がkr1、kr2のように地域名で表示されます。
- 共通凡例は次のとおりです。

| フィルタ名           | 説明         | 値                                                                |
|-----------------|--------------|--------------------------------------------------------------------|
| nhncloud_region | NHN Cloudリージョン | kr1:韓国(パンギョ), kr2:韓国(ピョンチョン), kr3:韓国(光州), us1:米国(カリフォルニア), jp1:日本(東京) |

## Instance
- NHN CloudのInstanceサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List
| 指標名            | リソース名  | 基本凡例(Legend)                                                              | 単位(Unit)         |
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

| フィルタ名 | 説明                                     |
|------|------------------------------------------|
| インスタンス | NHN CloudのInstanceサービスで使用中のインスタンスの名前 |

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
- NHN CloudのNCSサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List
| 指標名         | リソース名 | 基本凡例(Legend)                                                            | 単位(Unit)        |
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

| フィルタ名 | 説明                                |
|------|-------------------------------------|
| ワークロード | NHN CloudのNCSサービスで使用中のワークロードの名前 |
| タイプ | ストレージ種類                           |


### NCS Legend
- NCS指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。

| 凡例名                                         | 説明                           |
|----------------------------------------------|--------------------------------|
| label_ncs_container_nhncloud_com_workload_id | NHN CloudのNCSサービスで使用中のワークロードの名前 |
| workload_id                                  | NHN CloudのNCSサービスで使用中のワークロードの名前 |
| type                                         | ストレージ種類                      |
| container                                    | コンテナ名                     |

## GPU
- NHN CloudのGPUサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List
| 指標名       | リソース名 | 基本凡例(Legend) | 単位(Unit)   |
|-------------|------|---------------|------------|
| GPU使用率   | GPU  | なし           | パーセンテージ(0-100) |
| GPU温度    | GPU  | なし           | 摂氏(℃)      |
| GPUメモリ使用率 | GPU  | なし           | パーセンテージ(0-100) |
| GPU電力使用量 | GPU  | なし           | ワット(W)      |

### GPUフィルタ(Filter)
- GPU指標に対してフィルタを適用できます。
- フィルタを適用すると、そのフィルタに合う指標だけが表示されます。

| フィルタ名 | 説明                                 |
|------|-------------------------------------|
| インスタンス | NHN CloudのGPUサービスで使用中のインスタンスの名前 |

### GPU凡例(Legend)
- GPU指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。

| フィルタ名                | 説明         |
|----------------------|--------------|
| nhncloud_instance_id | GPUインスタンスの名前 |

## Transit Hub
- NHN CloudのTransit Hubサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List
| 指標名                               | リソース名 | 基本凡例(Legend) | 単位(Unit)   |
|------------------------------------|------|---------------|------------|
| ネットワーク送信バイト                       | トランジットハブ | {{id}} | 5分累積バイト |
| ネットワーク受信バイト                       | トランジットハブ | {{id}} | 5分累積バイト |
| ネットワーク送信パケット                        | トランジットハブ | {{id}} | 5分累積パケット |
| ネットワーク受信パケット                        | トランジットハブ | {{id}} | 5分累積パケット |
| 経路が一致しないため、削除されたネットワークパケット           | トランジットハブ | {{id}} | 5分累積パケット |
| 経路が一致しないため、削除されたネットワークバイト          | トランジットハブ | {{id}} | 5分累積バイト |
| ブラックホール経路と一致したため、削除されたネットワークパケット          | トランジットハブ | {{id}} | 5分累積パケット |
| ブラックホール経路と一致したため、削除されたネットワークバイト数         | トランジットハブ | {{id}} | 5分累積バイト |
| ネットワーク送信バイト                       | 接続 | {{id}} | 5分累積バイト |
| ネットワーク受信バイト                       | 接続 | {{id}} | 5分累積バイト |
| ネットワーク送信パケット                        | 接続 | {{id}} | 5分累積パケット |
| ネットワーク受信パケット                        | 接続 | {{id}} | 5分累積パケット |
| 経路が一致しないため、削除されたネットワークパケット           | 接続 | {{id}} | 5分累積パケット |
| 経路が一致しないため、削除されたネットワークバイト          | 接続 | {{id}} | 5分累積バイト |
| ブラックホール経路と一致したため、削除されたネットワークパケット          | 接続 | {{id}} | 5分累積パケット |
| ブラックホール経路と一致したため、削除されたネットワークバイト         | 接続 | {{id}} | 5分累積バイト |
| ネットワーク送信 ビット/秒(bps)               | トランジットハブ | {{id}} |  ビット/秒(bits/s)  |
| ネットワーク受信 ビット/秒(bps)               | トランジットハブ | {{id}} |  ビット/秒(bits/s)  |
| ネットワーク送信 パケット/秒(pps)               | トランジットハブ | {{id}} |  パケット/秒(packets/s)  |
| ネットワーク受信 パケット/秒(pps)               | トランジットハブ | {{id}} |  パケット/秒(packets/s)  |
| 経路が一致しないため、削除されたネットワーク パケット/秒(pps)  | トランジットハブ | {{id}} |  パケット/秒(packets/s)  |
| 経路が一致しないため、削除されたネットワーク ビット/秒(bps)  | トランジットハブ | {{id}} |  ビット/秒(bits/s)  |
| ブラックホール経路と一致したため、削除されたネットワーク パケット/秒(pps) | トランジットハブ | {{id}} |  パケット/秒(packets/s)  |
| ブラックホール経路と一致したため、削除されたネットワーク ビット/秒(bps) | トランジットハブ | {{id}} |  ビット/秒(bits/s)  |
| ネットワーク送信 ビット/秒(bps)               | 接続 | {{id}} |  ビット/秒(bits/s)  |
| ネットワーク受信 ビット/秒(bps)               | 接続 | {{id}} | ビット/秒(bits/s)  |
| ネットワーク送信 パケット/秒(pps)               | 接続 | {{id}} |  パケット/秒(packets/s)  |
| ネットワーク受信 パケット/秒(pps)               | 接続 | {{id}} |  パケット/秒(packets/s)  |
| 経路が一致しないため、削除されたネットワーク パケット/秒(pps)  | 接続 | {{id}} |  パケット/秒(packets/s)  |
| 経路が一致しないため、削除されたネットワーク ビット/秒(bps)  | 接続 | {{id}} |  ビット/秒(bits/s)  |
| ブラックホール経路と一致したため、削除されたネットワーク パケット/秒(pps) | 接続 | {{id}} |  パケット/秒(packets/s)  |
| ブラックホール経路と一致したため、削除されたネットワーク ビット/秒(bps) | 接続 | {{id}} |  ビット/秒(bits/s)  |


### Transit Hubフィルタ(Filter)
- Transit Hub指標に対してフィルタを適用できます。
- フィルタを適用すると、該当フィルタ条件に該当する指標のみ表示されます。

#### リソースタイプ > トランジットハブの場合に適用可能なフィルタ

| フィルタ名 | 説明 |
| --- | --- |
| トランジットハブ | NHN CloudのNetworkサービスで使用中のトランジットハブ |

#### リソースタイプ > 接続の場合、適用可能なフィルタ

| フィルタ名 | 説明                                     |
| --- |-----------------------------------------|
| トランジットハブ | 接続に関連するトランジットハブ |
| 接続 | NHN CloudのNetworkサービスで使用中のトランジットハブ接続 |

### Transit Hub凡例(Legend)
- Transit Hub指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。

| 凡例名           | 説明                        |
|----------------|----------------------------|
| id             | トランジットハブまたは接続名           |
| transit_hub_id | トランジットハブ名(リソースが`接続`の場合) |

## Internet Gateway
- NHN CloudのInternet Gatewayサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List

| 指標名                         | リソース名   | 基本凡例(Legend)          | 単位(Unit)         |
|------------------------------|---------|------------------------|------------------|
| ネットワーク送信バイト                | ルーティングテーブル | {{id}} | 5分累積バイト       |
| ネットワーク受信バイト                | ルーティングテーブル | {{id}} | 5分累積バイト       |
| ネットワーク送信パケット                 | ルーティングテーブル | {{id}} | 5分累積パケット        |
| ネットワーク受信パケット                 | ルーティングテーブル | {{id}} | 5分累積パケット        |
| ネットワーク送信 ビット/秒(bps)        | ルーティングテーブル | {{id}} | ビット/秒(bits/s)    | 
| ネットワーク受信 ビット/秒(bps)	    | ルーティングテーブル | {{id}} | ビット/秒(bits/s)    | 
| ネットワーク送信 パケット/秒(pps)	    | ルーティングテーブル | {{id}} | パケット/秒(packets/s) | 
| ネットワーク受信 パケット/秒(pps)	    | ルーティングテーブル | {{id}} | パケット/秒(packets/s) | 

### Internet Gatewayフィルタ(Filter)
- Internet Gateway指標に対してフィルタを適用できます。
- フィルタを適用すると、該当フィルタ条件に該当する指標のみ表示されます。

| フィルタ名 | 説明 |
| --- | --- |
| ルーティングテーブル | NHN CloudのNetworkサービスで使用中のルーティングテーブル |

### Internet Gateway凡例(Legend)
- Internet Gateway指標に対して凡例を適用できます。
- 凡例を適用すると、該当指標が凡例形式で適用されます。

| 凡例名           | 説明                                    |
|----------------|----------------------------------------|
| id             | ルーティングテーブル名 |

## Colocation Gateway
- NHN CloudのColocation Gatewayサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List

| 指標名                   | リソース名      | 基本凡例(Legend) | 単位(Unit)          |
|-----------------------|------------|--------------|-------------------|
| ネットワーク送信バイト           | ルーティングテーブル | {{id}}       | 5分累積バイト           |
| ネットワーク受信バイト           | ルーティングテーブル | {{id}}       | 5分累積バイト           |
| ネットワーク送信パケット          | ルーティングテーブル | {{id}}       | 5分累積パケット          |
| ネットワーク受信パケット          | ルーティングテーブル | {{id}}       | 5分累積パケット          |
| ネットワーク送信 ビット/秒(bps)   | ルーティングテーブル | {{id}}       | ビット/秒(bits/s)     | 
| ネットワーク受信 ビット/秒(bps)	  | ルーティングテーブル | {{id}}       | ビット/秒(bits/s)     | 
| ネットワーク送信 パケット/秒(pps)  | ルーティングテーブル | {{id}}       | パケット/秒(packets/s) | 
| ネットワーク受信 パケット/秒(pps)	 | ルーティングテーブル | {{id}}       | パケット/秒(packets/s) | 

### Colocation Gatewayフィルタ(Filter)

| フィルタ名         | 説明                                      |
|---------------|-----------------------------------------|
| コロケーションゲートウェイ | NHN CloudのNetworkサービスで使用中のコロケーションゲートウェイ |

### Colocation Gateway凡例(Legend)

| 凡例名 | 説明             |
|-----|----------------|
| id  | コロケーションゲートウェイ名 |

## Load Balancer
- NHN CloudのLoad Balancerサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List

| 指標名                                 | リソース名    | 基本凡例(Legend)                                                  | 単位(Unit)      |
|-------------------------------------|----------|---------------------------------------------------------------|---------------|
| ネットワーク受信バイト                         | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積バイト       |
| ネットワーク送信バイト                         | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積バイト       |
| ネットワーク受信ビット/秒(bps)                  | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | ビット/秒(bits/s) |
| ネットワーク送信ビット/秒(bps)                  | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | ビット/秒(bits/s) |
| 処理待機中のリクエスト数                        | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 数字            |
| 接続状態にあるセッション数                       | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 数字            |
| HTTP 100番台レスポンスをした回数                | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積数値        |
| HTTP 200番台レスポンスをした回数                | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積数値        |
| HTTP 300番台レスポンスをした回数                | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積数値        |
| HTTP 400番台レスポンスをした回数                | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積数値        |
| HTTP 500番台レスポンスをした回数                | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積数値        |
| HTTPレスポンスのうち、100番～500番以外のレスポンスをした回数 | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5分累積数値        |
| 当該メンバーでロードバランシングされた合計回数             | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 数字            |
| エラー発生接続回数                           | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 数字            |
| 平均レスポンス時間                           | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | ミリ秒           |
| 該当メンバーのアクティブ状態値                     | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 数字            |
| HTTPレスポンスが正常に返された合計回数               | ロードバランサー | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 数字            |

### Load Balancerフィルタ(Filter)

| フィルタ名    | 説明                                 |
|----------|------------------------------------|
| ロードバランサー | NHN CloudのNetworkサービスで使用中のロードバランサー |

### Load Balancer凡例(Legend)

| 凡例名             | 説明        |
|-----------------|-----------|
| loadbalancer_id | ロードバランサー名 |
| listener_id     | リスナー名     |
| pool_id         | メンバーグループ名 |
| member_id       | メンバー名     |

## Direct Connect
- NHN CloudのDirect Connectサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List

| 指標名                 | リソース名   | 基本凡例(Legend) | 単位(Unit)      |
|---------------------|---------|--------------|---------------|
| 接続状態                | Network | {{orderId}}  | 数字            |
| 接続受信エラー数            | Network | {{orderId}}  | 数字            |
| 接続送信エラー数            | Network | {{orderId}}  | 数字            |
| ネットワーク送信バイト         | Network | {{orderId}}  | 5分累積バイト       |
| ネットワーク受信バイト         | Network | {{orderId}}  | 5分累積バイト       |
| ネットワーク送信 ビット/秒(bps) | Network | {{orderId}}  | ビット/秒(bits/s) |
| ネットワーク受信 ビット/秒(bps) | Network | {{orderId}}  | ビット/秒(bits/s) |

### Direct Connectフィルタ(Filter)

| フィルタ名  | 説明                                        |
|--------|-------------------------------------------|
| サービスID | NHN CloudのDirect Connectサービスで使用中のサービス申請ID |


### Direct Connect凡例(Legend)

| 凡例名     | 説明       |
|---------|----------|
| orderId | サービス申請ID |

## VPC
- NHN CloudのVPCサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List

| 指標名                 | リソース名   | 基本凡例(Legend) | 単位(Unit)      |
|---------------------|---------|--------------|---------------|
|VPC全体のIP数|VPC|{{vpc_id}}|数字|
|サブネット割り当てIP数|VPC|{{vpc_id}}|数字|
|VPC使用率|VPC|{{vpc_id}}|パーセンテージ(0-100)|


### VPCフィルタ(Filter)

| フィルタ名 | 説明                        |
|-------|---------------------------|
| VPC   | NHN CloudのNetworkサービスで使用中のVPC |


### VPC凡例(Legend)

| 凡例名    | 説明       |
|--------|----------|
| vpc_id | VPCの名前 |

## Subnet
- NHN CloudのSubnetサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List

| 指標名                 | リソース名   | 基本凡例(Legend) | 単位(Unit)      |
|---------------------|---------|--------------|---------------|
|サブネット全体のIP数|Subnet|{{subnet_id}}|数字|
|リソース割り当てIP数|Subnet|{{subnet_id}}|数字|
|サブネット使用率|Subnet|{{subnet_id}}|パーセンテージ(0-100)|


### Subnetフィルタ(Filter)

| フィルタ名 | 説明                        |
|-------|---------------------------|
| サブネット   | NHN CloudのNetworkサービスで使用中のサブネット |


### Subnet凡例(Legend)

| 凡例名    | 説明       |
|--------|----------|
| subnet_id | サブネットの名前 |

## Floating IP
- NHN CloudのFloating IPサービスに対してモニタリングできる指標を定義した辞書です。

### Metric List

| 指標名                 | リソース名   | 基本凡例(Legend) | 単位(Unit)      |
|---------------------|---------|--------------|---------------|
|全体Floating IP数|Floating IP|{{nhncloud_region}} - total|数字|
|接続されたFloating IP数|Floating IP|{{nhncloud_region}} - {{status}}|数字|
|接続されていないFloating IP数|Floating IP|{{nhncloud_region}} - {{status}}|数字|

## Monitoring > Cloud Monitoring > コンソール使用ガイド

コンソール使用ガイドでは、Cloud Monitoringサービスの基本的な使用方法を案内します。

## ダッシュボード

**Monitoring > Cloud Monitoring > ダッシュボード**では、NHN Cloudサービスで作成したリソースから収集した様々な指標をチャートウィジェットで作成し、ダッシュボードを構成して指標を確認できます。

![照会期間自動更新](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01-1.png)

ユーザーが構成したダッシュボードの指標データの照会期間は、基本的に現在時刻から5分前までのデータを照会します。基本設定された自動更新間隔は1分です。

![照会期間ユーザー指定](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01-2.png)

ユーザー指定期間を設定すると、自動更新は使用できません。

### 照会モード/編集モード

![ダッシュボード照会モード](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-1.png)

![ダッシュボード編集モード](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-2.png)

ダッシュボードは照会モードと編集モードの2つのモードがあります。

![照会モードヘッダ](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-3.png)

ダッシュボードは基本的に照会モードで表示され、ダッシュボードやウィジェットを修正するには、編集モードのトグルをクリックして編集モードに切り替える必要があります。

![編集モードヘッダ](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-4.png)

編集モードでは、ダッシュボードの名前や説明を修正したり、ダッシュボードを複製または削除できます。各ウィジェットを修正したり、ウィジェットの位置移動や複製を行うこともできます。

![全体保存通知モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-5.png)

ウィジェットを追加したり、ウィジェットの位置やサイズなどを修正した内容は、全体保存をクリックすることで適用されます。保存しなかった場合、保存通知モーダルが表示され、保存しなかった変更内容は消えます。

### ダッシュボードの作成

![ダッシュボード追加モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-1.png)

照会モードで**ダッシュボード**タブの右側の**+**ボタンをクリックすると、ダッシュボード追加モーダルが開きます。

![空のダッシュボード](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-2.png)

作成されたダッシュボードがない場合、**+ダッシュボード作成**ボタンが表示されます。

![ダッシュボード作成後](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-3.png)

**ダッシュボード名**と**ダッシュボード説明**を入力してください。**ダッシュボード名**は必ず入力しなければならない必須値であり、重複した名前で設定できますが、なるべくユニークな名前を使用することを推奨します。
**ダッシュボードの説明**は選択値で、そのダッシュボードを説明できる内容を入力します。

### ダッシュボード構成

![ダッシュボード例](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-1.png)

ダッシュボードにはウィジェットとウィジェットグループを追加できます。ウィジェットはダッシュボードごとに12個まで追加でき、追加するとダッシュボードの最下段に追加されます。

![ウィジェット例](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-2.png)

ウィジェットはダッシュボードを構成する最小単位です。**+ ウィジェットの追加**をクリックするか、そのボタンのドロップダウンリストから**ウィジェットの追加**、**ウィジェットテンプレートの追加**を選択して作成できます。ウィジェットのサイズと位置は、ダッシュボード編集モードで自由に変更できます。

![ウィジェットグループ例](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-3.png)

ウィジェットグループを使用すると、複数のウィジェットをグループ化して管理できます。ウィジェットグループを折りたたんだり広げたりして、複数のウィジェットを隠したり、表示したりすることができ、ウィジェットグループの高さと幅はグループ内のウィジェットサイズに応じて自動的に調整されます。

#### ウィジェット及びウィジェットグループの追加/修正

![ウィジェット追加ボタン領域](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a-1.png)

ウィジェットおよびウィジェットグループは、照会モードと編集モードの両方で追加することができます。ただし、ウィジェットおよびウィジェットグループを修正するには、編集モードに切り替える必要があります。

##### ウィジェットの追加

![ウィジェット追加画面の基本情報](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-1.png)

ウィジェットの追加で、好きな指標とフィルタを適用して自由にチャートウィジェットを作成できます。
ウィジェット名、グラフタイプ、サービス、指標設定 > 指標の項目は必須項目なので、必ず入力してください。
一つのウィジェットは単一のサービスのみ表現できます。ただし、指標項目は複数選択できます。

![ウィジェット追加画面指標項目選択後](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-2.png)

指標項目を選択するたびに、画面下部に指標項目のフィルタと凡例を設定できる要素が追加されます。
指標のフィルタラベルは種類ごとに1つだけ指定可能で、すべてのフィルタは「&」演算の形で最終適用されます。したがって、フィルタを複数適用する場合、条件値の検索結果は、以前に設定したフィルタ条件をすべて満たす検索結果のみ表示されます。先に追加したフィルタの演算子と条件値によって、選択できる条件値がなくなる場合があります。

凡例は、各指標項目で照会した指標データを区別するための名前です。指標項目を追加すると、基本的に推奨される名前が自動的に入力されます。`{{ }}`二重中括弧の文法で囲まれたプレースホルダの前後に好きなフレーズを追加できます。何もテキストを入力しない場合は、指標項目が持っているラベル属性を全て連結して表示します。
単位を選択してチャートに表示するY軸タイトルと単位を指定できます。単位による個別のフォーマットはサポートせず、指標項目の実際の値を小数点以下15桁まで表示します(16桁目まで切り上げ、`Percent(0.0~1.0)`を選択した場合のみ例外的に0～100に値を変換して表示します)。Y軸位置設定で指標項目のY軸位置を**自動** / **左** / **右**の中から選択できます。指標項目追加時、基本的に自動値が選択されています。すべての指標項目が自動的に選択されている場合、順次Y軸を左または右の位置に分けて配置します。もしY軸位置が左または右に指定された指標が存在する場合、同じY軸方向に配置します。この時、単位とY軸位置が同じ指標項目がある場合、同じY軸で表現します。

![ウィジェット追加画面プレビューレイヤー](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-3.png)

グラフタイプを変更したり、指標項目フィルタを修正した後、変更点が反映されたチャートウィジェットの様子をプレビューできます。画面右上の**プレビュー**トグルをクリックすると、フィルタと凡例値を適用したチャートウィジェットをリアルタイムで確認できるプレビューレイヤーを開閉できます。プレビューレイヤーは左右の幅を調整できます。

##### ウィジェットテンプレートの追加

![ウィジェットテンプレート追加モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_02-1.png)

ウィジェットテンプレートは、あらかじめ設定したウィジェットの指標項目を利用してウィジェットを簡単に作成できる機能です。ウィジェットを追加した後、ウィジェット修正を通じて指標項目にフィルタを追加したり、指標項目や名前を変更できます。
ただし、一部のウィジェットテンプレートで追加したウィジェットは削除のみ可能で、修正ができない場合があります。

##### ウィジェットグループ追加

![ウィジェットグループ追加モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_03-1.png)

ウィジェットグループ追加でダッシュボードにウィジェットグループを追加できます。ウィジェットをウィジェットグループに追加するには、編集モードでウィジェット上部のタイトル領域をドラッグしてウィジェットグループ内に移動します。

ウィジェットグループはウィジェットと同様に修正が可能で、ウィジェットグループを修正するには編集モードに切り替える必要があります。

![ウィジェットグループcontextメニュー](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_03-2.png)

- **修正**をクリックすると、**ウィジェットグループの修正**モーダルが開きます。
- **グループ削除**をクリックすると、ウィジェットの位置やサイズ情報はそのまま残り、グループのみ削除されます。
- **グループ及び下位ウィジェット全体削除**をクリックすると、グループ内のウィジェットまで削除されます。

#### ウィジェットの移動/複製/削除

![ウィジェットサイズ調整](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-1.gif)

編集モードに切り替えた後、ウィジェットの右下隅をドラッグしてサイズを調整したり、ウィジェットの上部領域をドラッグして位置を移動させることができます。

![ウィジェットcontextメニュー](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-3.png)

- **削除**をクリックしてウィジェットを削除できます。
- **ダッシュボード内のウィジェット複製**をクリックしてダッシュボードにウィジェットを複製できます。複製されたウィジェットは最下段に追加されます。
- **他のダッシュボードにウィジェットを複製**をクリックして他のダッシュボードにウィジェットを複製できます。この時、ウィジェットを追加するダッシュボードを選択できるモーダルが開きます。

![他のダッシュボードにウィジェット複製モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-2.png)

#### 通知作成

![ウィジェットcontextメニュー](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-3.png)

**通知作成**をクリックすると、**通知管理** > **通知作成**画面に移動します。ウィジェット名、サービス、指標項目、指標項目フィルタ情報など、当該ウィジェットの情報が入力された状態で簡単に通知を作成できます。
通知条件と通知受信対象を入力するだけで、簡単に通知を作成できます。

![ウィジェット通知作成でアクセスした場合](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_c-1.png)

### ダッシュボード管理

![照会モードヘッダ](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-1.png)

![ダッシュボード管理モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-2.png)

**ダッシュボード管理**をクリックすると、ダッシュボード管理モーダルが表示されます。ダッシュボードの名前、説明、作成日時、プロジェクトダッシュボードの公開設定有無を確認したり、編集することができます。

![ダッシュボード管理モーダル > 編集モード](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-3.png)

各ダッシュボードの**編集**列の修正または削除アイコンをクリックして、そのダッシュボードの名前と説明を修正したり、ダッシュボードを削除することができます。
**プロジェクトダッシュボードの表示設定**トグルをクリックして、プロジェクトカスタムダッシュボード画面でそのダッシュボードの表示の有無を設定できます。公開設定を解除しても、Cloud Monitoringサービスでは常に公開されます。

### ウィジェットデータのダウンロード

![ウィジェットデータダウンロードメニュー](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_05-1.png)

ダッシュボードのすべてのウィジェットデータを.png、.csv、.xlsxファイルでダウンロードできます。ファイル名はダッシュボード名で保存され、.csvファイルの場合、ダッシュボード名で圧縮した.zipファイルでダウンロードされます。内部には、各ウィジェット名の個別.csvファイルが含まれています。
.csv、.xlsxファイルの場合、開始日時を基準に最大3か月間のデータのみダウンロードできます。照会期間が1か月未満の場合、5分間隔でデータを提供し、1か月以上は1日間隔でデータを提供します。
指定した照会期間が長かったり、ウィジェットとウィジェットに含まれる指標データが多いほど、ダウンロードにかかる時間が長くなる場合があります。

## 通知管理

**Monitoring > Cloud Monitoring > 通知設定**では、NHN Cloudリソースに通知を追加することができ、通知の発生履歴を確認できます。

![通知設定リスト画面](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01-1.png)

### 通知設定

![通知設定リスト画面 - 作成済み](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-4.png)

通知設定画面では、作成した通知の情報を確認できるテーブルが表示され、通知名、通知の使用可否、作成日時でテーブルのソートを変更できます。
- **通知の使用有無**トグルをクリックして、通知を有効または無効にできます。
- **通知詳細表示**列の**表示**をクリックすると、**通知詳細情報**モーダルが表示されます。
- **修正**列の**修正**をクリックすると、**通知修正**画面に移動します。
- 各通知行をクリックすると、**通知発生履歴**タブに移動し、その通知が自動照会されて表示されます。

#### 通知の作成/修正

![通知作成/修正画面](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-1.png)

通知基本情報の名前、サービスと通知設定の指標項目と通知条件、通知の受信対象は必須値なので必ず入力する必要があります。
通知のサービスは単一選択のみ可能で、指標項目は複数選択できます。

![通知作成/修正画面 - 指標選択する](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-2.png)

指標項目のフィルタは入力しなくてもよいですが、条件は必ず1つ以上入力する必要があります。通知を受けたい条件を比較方法、しきい値、持続時間の組み合わせで設定します。

![通知設定リスト画面 - 通知受信対象](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-3.png)

通知受信対象は1つ以上選択する必要があります。通知受信対象タイプは、通知受信グループのみサポートされ、**プロジェクト管理 > 通知受信グループ管理** 画面で管理できます。[[ガイドへ]](/nhncloud/ja/console-guide/#_34)

通知受信グループのカスタムWebフックを通じてWebフックで通知を受け取ることができます。

- カスタムWebフックリクエストデータとして提供するパラメータリスト

| 値 | 説明 | タイプ | 備考 |
| --- | --- | --- | --- |
| orgName | 組織名 | String |  |
| projectName | プロジェクト名 | String |  |
| tenantType | サービスタイプ | String | `organization`(カスタムダッシュボード)<br>`project`(Cloud Monitoring) |
| referenceKey | 組織またはプロジェクトID | String |  |
| serviceName | サービス名 | String |  |
| alertName | 通知名 | String |  |
| alertId | 通知ID | String |  |
| eventsCount | 発生イベント数 | Integer |  |
| events | 通知イベント | List<Object\> | eventsパラメータリスト参照 |

- eventsパラメータリスト

| 値 | 説明 | タイプ | 備考 |
| --- | --- | --- | --- |
| events[].resourceTypeName | リソースタイプ名(En) | String | |
| events[].enMetricName | 指標名(En) | String | |
| events[].threshold | しきい値 | String | Double形式の文字列 |
| events[].operator | 比較方法 | String | Enum (`EQUAL`, `NOT_EQUAL`, `GREATER_THAN`, `LESS_THAN`, `GREATER_THAN_OR_EQUAL`, `LESS_THAN_OR_EQUAL`) |
| events[].duration | 持続時間 | String | 条件に設定された値 |
| events[].result | 検出された値 | String | Double形式の文字列 |
| events[].startAt | イベント発生日時 | String | ex) `2024-10-29T08:44:22Z` |
| events[].endAt | イベント終了日時 | String | ex) `2024-10-29T08:44:22Z` |
| events[].contMinutes | イベント持続時間(分) | Integer | イベントが発生した時間と現在時間との差(分) |
| events[].labels | 発生位置 | Map<String, String\> | |

#### 通知詳細表示モーダル

![通知詳細表示モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_b-1.png)

通知詳細表示モーダルでは、設定した通知の詳細情報を確認できます。通知の名前、説明、サービス、指標項目フィルタおよび通知条件、通知受信対象を確認できます。

### 通知発生履歴

![通知発生履歴照会画面](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02-1.png)

発生した通知の履歴を照会できる検索フィルタとテーブルを使用して発生した通知を多様に照会することができ、検索フィルタで照会した通知情報を確認できるテーブルを提供します。
通知名、発生日時、終了日時、サービス、リソース、指標項目、結果値、持続時間を確認できます。発生日時、終了日時でテーブルの並べ替えを変更できます。

> 参考：持続時間は、通知発生時点から通知終了時点までの時間を示します。
> 通知が発生した状態で、その通知が終了する前に通知を無効にすると、明示的に通知が終了していないため、持続時間が継続的に増加する可能性があります。

#### 通知発生履歴照会

![通知発生履歴照会検索フィルタ](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02_a-1.png)

通知名、通知状態、指標項目、発生時間フィルタを使用して通知発生履歴を照会できます。**初期化**を押すと、検索フィルタが初期化されます。

#### 通知送信履歴表示モーダル

![通知発生履歴照会画面](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02-1.png)
各通知で**通知送信履歴を表示**列の**表示**をクリックすると、**通知送信履歴を表示**モーダルが開きます。

![通知送信履歴表示モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02_b-1.png)

通知送信履歴表示モーダルでは、当該通知の**発生日時**、**継続時間**、**指標項目**、**結果値**、**通知条件**などの通知設定情報と**発生位置**を詳細に確認できます。

通知を実際に送信した履歴も表形式で提供します。各通知送信履歴の通知送信日時、通知方法、受信対象、通知送信結果を確認できます。
通知送信日時、通知方法でテーブルのソートを変更できます。

## 指標管理

**Monitoring > Cloud Monitoring > 指標管理**では、NHN Cloudリソースのサービス別の指標を収集するかどうかを設定できます。

### 指標収集設定

![指標管理画面](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-1.png)

サービス別の指標収集を設定できるテーブルが表示されます。
サービスごとに**カテゴリ**、**サービス**、**サービス有効化有無**、**指標収集設定**の内容を確認することができ、**指標収集設定**トグルをクリックして指標収集の有無を設定できます。

![指標収集開始確認モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-2.png)

![指標収集中断確認モーダル](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-3.png)

指標の収集を開始/中断する場合、確認モーダルが開きます。

![指標が中断されたウィジェットの例](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-4.png)

![指標収集中のウィジェットの例](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-5.png)

指標の収集を中断した場合、当該サービスの指標を使用して作成したウィジェットでは、当該指標が表示されなくなり、当該指標の凡例が無効になります。

## 例画面

![ダッシュボード例](https://static.toastoven.net/prod_cloud_monitoring/Overview.png)

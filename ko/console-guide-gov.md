## Monitoring > Cloud Monitoring > 콘솔 사용 가이드

콘솔 사용 가이드에서는 Cloud Monitoring 서비스의 기본적인 사용법을 안내합니다.

## 대시보드

**Monitoring > Cloud Monitoring > 대시보드**에서는 NHN Cloud 서비스에서 생성한 자원에서 수집한 다양한 지표를 차트 위젯으로 만들고 대시보드를 구성해서 지표를 확인할 수 있습니다.

![조회 기간 자동 새로고침](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01-1.png)

사용자가 구성한 대시보드의 지표 데이터 조회 기간은 기본적으로 현재 시각으로부터 5분 전까지의 데이터를 조회합니다. 기본 설정된 자동 새로고침 간격은 1분입니다.

![조회 기간 사용자 지정](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01-2.png)

사용자 지정 기간을 설정하면 자동 새로고침은 사용할 수 없습니다.

### 조회 모드/편집 모드

![대시보드 조회 모드](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-1.png)

![대시보드 편집 모드](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-2.png)

대시보드는 조회 모드와 편집 모드 2가지의 모드가 있습니다.

![조회 모드 헤더](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-3.png)

대시보드는 기본적으로 조회 모드로 보여지며, 대시보드나 위젯을 수정하려면 편집 모드 토글을 클릭해 편집 모드로 전환해야 합니다.

![편집 모드 헤더](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-4.png)

편집 모드에서는 대시보드의 이름 또는 설명을 수정하거나, 대시보드를 복제 또는 삭제할 수 있습니다. 각 위젯을 수정하거나 위젯의 위치 이동 및 복제를 수행할 수도 있습니다.

![전체 저장 알림 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_01-5.png)

위젯을 추가하거나 위젯의 위치 및 크기 등을 수정한 내용은 전체 저장을 클릭해야 적용됩니다. 저장하지 않은 경우 저장 알림 모달이 표시되며, 저장하지 않은 변경 사항은 사라집니다.

### 대시보드 생성

![대시보드 추가 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-1.png)

조회 모드에서 **대시보드** 탭 오른쪽의 **+** 버튼을 클릭하면 대시보드 추가 모달이 열립니다.

![빈 대시보드](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-2.png)

생성된 대시보드가 없을 경우 **+ 대시보드 생성** 버튼이 표시됩니다.

![대시보드 생성 후](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_02-3.png)

**대시보드 이름**과 **대시보드 설명**을 입력하십시오. **대시보드 이름**은 반드시 입력해야 하는 필수 값이며, 중복된 이름으로 설정할 수 있으나 되도록 고유한 이름을 사용할 것을 권장합니다.
**대시보드 설명**은 선택 값으로, 해당 대시보드를 설명할 수 있는 내용을 입력합니다.

### 대시보드 구성

![대시보드 예시](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-1.png)

대시보드에는 위젯과 위젯 그룹을 추가할 수 있습니다. 위젯은 대시보드마다 12개까지 추가할 수 있으며, 추가 시 대시보드의 최하단에 추가됩니다.

![위젯 예시](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-2.png)

위젯은 대시보드를 구성하는 최소 단위입니다. **+ 위젯 추가**를 클릭하거나 해당 버튼의 드롭다운 목록에서 **위젯 추가**, **위젯 템플릿 추가**를 선택해 생성할 수 있습니다. 위젯의 크기와 위치는 대시보드 편집 모드에서 자유롭게 변경할 수 있습니다.

![위젯 그룹 예시](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03-3.png)

위젯 그룹을 사용하면 여러 위젯을 그룹으로 묶어 관리할 수 있습니다. 위젯 그룹을 접거나 펼쳐서 여러 위젯을 숨기고 나타낼 수 있으며, 위젯 그룹의 높이 및 너비는 그룹 내의 위젯 크기에 따라 자동으로 조절됩니다.

#### 위젯 및 위젯 그룹 추가/수정

![위젯 추가 버튼 영역](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a-1.png)

위젯 및 위젯 그룹은 조회 모드와 편집 모드 상태 모두에서 추가할 수 있습니다. 단, 위젯 및 위젯 그룹을 수정하려면 편집 모드로 전환해야 합니다.

##### 위젯 추가

![위젯 추가 화면 기본 정보](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-1.png)

위젯 추가를 통해 원하는 지표와 필터를 적용해서 자유롭게 차트 위젯을 생성할 수 있습니다.
위젯 이름, 그래프 유형, 서비스, 지표 설정 > 지표 항목은 필수 값이므로 반드시 입력해야 합니다.
하나의 위젯은 단일 서비스만 표현할 수 있습니다. 단, 지표 항목은 복수 개 선택할 수 있습니다.

![위젯 추가 화면 지표 항목 선택 후](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-2.png)

지표 항목을 선택할 때마다 화면 하단에 지표 항목의 필터와 범례를 설정할 수 있는 요소가 추가됩니다.
지표 필터 레이블은 종류별로 1개만 지정 가능하고, 모든 필터는 `&` 연산 형태로 최종 적용됩니다. 따라서 필터를 복수 개 적용할 때, 조건 값의 검색 결과는 이전에 설정한 필터 조건들을 모두 충족하는 검색 결과만 노출됩니다. 앞서 추가한 필터의 연산자와 조건 값에 따라 더 이상 선택할 수 있는 조건 값이 없을 수 있습니다.

범례는 각 지표 항목으로 조회한 지표 데이터를 구분하기 위한 이름입니다. 지표 항목 추가하면 기본적으로 추천되는 이름을 자동으로 채워 넣습니다. `{{ }}` 이중 중괄호 문법으로 감싸진 플레이스 홀더 앞/뒤로 원하는 문구를 추가할 수 있습니다. 아무 텍스트도 입력하지 않으면 지표 항목이 가지고 있는 레이블 속성을 모두 연결해서 노출합니다.
단위를 선택해서 차트에 노출할 Y축 타이틀 및 단위를 지정할 수 있습니다. 단위에 따른 별도 포매팅은 지원하지 않고 지표 항목의 실제 값을 소수점 15자리까지 노출합니다(16번째 자리에서 반올림하며, `Percent(0.0~1.0)`를 선택한 경우만 예외적으로 0~100으로 값을 변환하여 노출합니다). Y축 위치 설정을 통해서 지표 항목의 Y축 위치를 **자동** / **좌** / **우** 중에서 선택할 수 있습니다. 지표 항목 추가 시, 기본적으로 자동 값이 선택되어 있습니다. 모든 지표 항목이 자동으로 선택되어 있다면, 순차적으로 Y축을 좌 또는 우 위치로 나눠서 배치합니다. 만약 Y축 위치가 좌 또는 우로 지정된 지표가 존재한다면 같은 Y축 방향으로 배치합니다. 이때, 단위와 Y축 위치가 같은 지표 항목이 있다면 같은 Y축으로 표현합니다.

![위젯 추가 화면 미리 보기 레이어](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_01-3.png)

그래프 유형을 변경하거나 지표 항목 필터를 수정한 뒤 변경점이 반영된 차트 위젯의 모습을 미리 확인할 수 있습니다. 화면 우측 상단의 **미리 보기** 토글을 클릭해 필터와 범례 값을 적용한 차트 위젯을 실시간으로 확인할 수 있는 미리 보기 레이어를 열거나 닫을 수 있습니다. 미리 보기 레이어는 좌우 너비를 조정할 수 있습니다.

##### 위젯 템플릿 추가

![위젯 템플릿 추가 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_02-1.png)

위젯 템플릿은 미리 구성한 위젯의 지표 항목들을 이용해 위젯을 더운 간편하게 생성할 수 있는 기능입니다. 위젯을 추가한 뒤, 위젯 수정을 통해서 지표 항목에 필터를 추가하거나 지표 항목 및 이름을 변경할 수 있습니다.
단, 일부 위젯 템플릿을 통해 추가한 위젯은 삭제만 가능하고 수정이 불가능할 수 있습니다.

##### 위젯 그룹 추가

![위젯 그룹 추가 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_03-1.png)

위젯 그룹 추가를 통해 대시보드에 위젯 그룹을 추가할 수 있습니다. 위젯을 위젯 그룹에 추가하려면 편집 모드에서 위젯 상단의 타이틀 영역을 드래그해서 위젯 그룹 내부로 옮기면 됩니다.

위젯 그룹은 위젯과 마찬가지로 수정이 가능하며, 위젯 그룹을 수정하려면 편집 모드로 전환해야 합니다.

![위젯 그룹 context 메뉴](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_a_03-2.png)

- **수정**을 클릭하면 **위젯 그룹 수정** 모달이 열립니다.
- **그룹 삭제**를 클릭하면 위젯의 위치나 크기 정보는 그대로 남고, 그룹만 제거됩니다.
- **그룹 및 하위 위젯 전체 삭제**를 클릭하면 그룹 내의 위젯까지 전체 삭제됩니다.

#### 위젯 이동/복제/삭제

![위젯 크기 조정](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-1.gif)

편집 모드로 전환한 뒤, 위젯 우측 하단 모서리를 드래그해서 크기를 조정하거나 위젯 상단 영역을 드래그해서 위치를 이동시킬 수 있습니다.

![위젯 context 메뉴](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-3.png)

- **삭제**를 클릭해 위젯을 삭제할 수 있습니다.
- **대시보드 내 위젯 복제**를 클릭해 대시보드에 위젯을 복제할 수 있습니다. 복제된 위젯은 최하단에 추가됩니다.
- **다른 대시보드에 위젯 복제**를 클릭해 다른 대시보드에 위젯을 복제할 수 있습니다. 이때, 위젯을 추가할 대시보드를 선택할 수 있는 모달이 열립니다.

![다른 대시보드에 위젯 복제 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-2.png)

#### 알림 생성

![위젯 context 메뉴](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_b_01-3.png)

**알림 생성**을 클릭하면 **알림 관리** > **알림 생성** 화면으로 이동합니다. 위젯 이름, 서비스, 지표 항목, 지표 항목 필터 정보 등 해당 위젯의 정보가 입력된 상태로 간편하게 알림을 생성할 수 있습니다.
알림 조건 및 알림 수신 대상만 입력하면 간편하게 알림을 생성할 수 있습니다.

![위젯 알림 생성으로 접근한 경우](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_03_c-1.png)

### 대시보드 관리

![조회 모드 헤더](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-1.png)

![대시보드 관리 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-2.png)

**대시보드 관리**를 클릭하면 대시보드 관리 모달이 표시됩니다. 대시보드의 이름, 설명, 생성 일시, 프로젝트 대시보드 노출 설정 여부를 확인하거나 편집할 수 있습니다.

![대시보드 관리 모달 > 편집 모드](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_04-3.png)

각 대시보드 **편집** 열의 수정 또는 삭제 아이콘을 클릭해 해당 대시보드의 이름 및 설명을 수정하거나 대시보드를 삭제할 수 있습니다.
**프로젝트 대시보드 노출 설정** 토글을 클릭해 프로젝트 커스텀 대시보드 화면에서 해당 대시보드의 노출 여부를 설정할 수 있습니다. 노출 설정을 해제하더라도 Cloud Monitoring 서비스에서는 항상 노출됩니다.

### 위젯 데이터 다운로드

![위젯 데이터 다운로드 메뉴](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_01_05-1.png)

대시보드의 모든 위젯 데이터를 .png, .csv, .xlsx 파일로 내려받을 수 있습니다. 파일명을 대시보드 이름으로 저장되며, .csv 파일의 경우 대시보드 이름으로 압축한 .zip 파일로 다운로드됩니다. 내부에는 각 위젯 이름으로 된 개별 .csv 파일이 들어 있습니다.
.csv, .xlsx 파일의 경우 시작 일시를 기준으로 최대 3개월간의 데이터만 다운로드할 수 있습니다. 조회 기간이 1개월 미만일 경우 5분 간격으로 데이터를 제공하며, 1개월 이상은 1일 간격으로 데이터를 제공합니다.
지정한 조회 기간이 길거나 위젯과 위젯에 포함된 지표 데이터가 많을수록 다운로드에 소요되는 시간이 오래 걸릴 수 있습니다.

## 알림 관리

**Monitoring > Cloud Monitoring > 알림 설정**에서는 NHN Cloud 자원에 알림을 추가할 수 있고, 알림 발생 이력을 확인할 수 있습니다.

![알림 설정 목록 화면](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01-1.png)

### 알림 설정

![알림 설정 목록 화면 - 생성 함](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-4.png)

알림 설정 화면에서는 생성한 알림의 정보를 확인할 수 있는 테이블이 노출되며, 알림명, 알림 사용 여부, 생성 일시로 테이블의 정렬을 변경할 수 있습니다.
- **알림 사용 여부** 토글을 클릭해 알림을 활성화하거나 비활성화할 수 있습니다.
- **알림 상세 보기** 열의 **보기**를 클릭하면 **알림 상세 정보** 모달이 표시됩니다.
- **수정** 열의 **수정**을 클릭하면 **알림 수정** 화면으로 이동합니다.
- 각 알림 행을 클릭하면 **알림 발생 이력** 탭으로 이동하며, 해당 알림이 자동 조회되어 노출됩니다.

#### 알림 생성/수정

![알림 생성/수정 화면](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-1.png)

알림 기본 정보의 이름, 서비스와 알림 설정의 지표 항목 및 알림 조건, 알림 수신 대상은 필수값이므로 반드시 입력해야 합니다.
알림의 서비스는 단일 선택만 가능하고, 지표 항목은 복수 개 선택할 수 있습니다.

![알림 생성/수정 화면 - 지표 선택함](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-2.png)

지표 항목의 필터는 입력하지 않아도 되지만 조건은 반드시 1개 이상 입력해야 합니다. 알림을 받고자 하는 조건을 비교 방법, 임계치, 지속 시간 조합으로 설정합니다.

![알림 설정 목록 화면 - 알림 수신 대상](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_a-3.png)

알림 수신 대상은 1개 이상 선택해야 합니다. 알림 수신 대상 유형은 알림 수신 그룹만 지원되며, **프로젝트 관리 > 알림 수신 그룹 관리** 화면에서 관리할 수 있습니다.

#### 알림 상세 보기 모달

![알림 상세 보기 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_01_b-1.png)

알림 상세 보기 모달에서는 설정한 알림의 상세 정보를 확인할 수 있습니다. 알림의 이름, 설명, 서비스, 지표 항목 필터 및 알림 조건, 알림 수신 대상을 확인할 수 있습니다.

### 알림 발생 이력

![알림 발생 이력 조회 화면](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02-1.png)

발생한 알림의 이력을 조회할 수 있는 검색 필터와 테이블을 사용해서 발생한 알림을 다양하게 조회할 수 있으며, 검색 필터로 조회한 알림 정보를 확인할 수 있는 테이블을 제공합니다.
알림명, 발생 일시, 종료 일시, 서비스, 리소스, 지표 항목, 결과값, 지속 시간을 확인할 수 있습니다. 발생 일시, 종료 일시로 테이블 정렬을 변경할 수 있습니다.

> 참고: 지속 시간은 알림 발생 시점에서 알림 종료 시점까지의 시간을 나타냅니다.
> 알림이 발생한 상태에서 해당 알림이 종료되기 전에 알림을 비활성화한다면, 명시적으로 알림이 종료되지 않았기 때문에 지속 시간이 계속 증가할 수 있습니다.

#### 알림 발생 이력 조회

![알림 발생 이력 조회 검색 필터](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02_a-1.png)

알림명, 알림 상태, 지표 항목, 발생 시간 필터를 사용해서 알림 발생 이력을 조회할 수 있습니다. **초기화**를 누르면 검색 필터가 초기화됩니다.

#### 알림 발송 이력 보기 모달

![알림 발생 이력 조회 화면](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02-1.png)
각 알림에서 **알림 발송 이력 보기** 열의 **보기**를 클릭하면 **알림 발송 이력 보기** 모달이 열립니다.

![알림 발송 이력 보기 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_02_02_b-1.png)

알림 발송 이력 보기 모달에서는 해당 알림의 **발생일시**, **지속시간**, **지표 항목**, **결과값**, **알림 조건** 등의 알림 설정 정보와 **발생 위치**를 상세하게 확인할 수 있습니다.

알림을 실제로 발송한 이력도 테이블 형태로 제공합니다. 각 알림 발송 이력의 알림 발송 일시, 알림 방법, 수신 대상, 알림 발송 결과를 확인할 수 있습니다.
알림 발송 일시, 알림 방법으로 테이블 정렬을 변경할 수 있습니다.

## 지표 관리

**Monitoring > Cloud Monitoring > 지표 관리**에서는 NHN Cloud 자원에 대한 서비스별 지표 수집 여부를 설정할 수 있습니다.

### 지표 수집 설정

![지표 관리 화면](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-1.png)

서비스별 지표 수집을 설정할 수 있는 테이블이 노출됩니다.
서비스마다 **카테고리**, **서비스**, **서비스 활성화 여부**, **지표 수집 설정** 내용을 확인할 수 있고, **지표 수집 설정** 토글을 클릭해 지표 수집 여부를 설정할 수 있습니다.

![지표 수집 시작 확인 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-2.png)

![지표 수집 중단 확인 모달](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-3.png)

지표 수집을 시작/중단하는 경우 확인 모달이 열립니다.

![지표 중단된 위젯의 예시](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-4.png)

![지표 수집 중일 때 위젯의 예시](https://static.toastoven.net/prod_cloud_monitoring/cloud_monitoring_03_01-5.png)

지표 수집을 중단한 경우, 해당 서비스의 지표를 사용해서 생성해 둔 위젯에서 해당 지표가 더 이상 노출되지 않고 해당 지표의 범례가 비활성화됩니다.

## 예시 화면

![대시보드 예시](https://static.toastoven.net/prod_cloud_monitoring/Overview.png)

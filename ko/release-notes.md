<!-- pre-align:aligned sig=1ffdaddde230 -->

## Monitoring > Cloud Monitoring > 릴리스 노트

<a id="june-23-2026"></a>

## 2026. 06. 23.

<a id="added-features"></a>

### 신규 기능 추가

* GPU Instance 상세 지표 추가
    * 신규 Cloud Monitoring Agent를 통해 GPU Instance의 상세 지표를 수집할 수 있습니다.
    * DCGM(Data Center GPU Manager) 기반으로 GPU 성능, GPU 상태, GPU 클럭 이벤트 영역의 지표를 제공합니다.
    * [신규 Agent 설치 가이드](new-instance-metric.md)를 참고하여 설치할 수 있습니다.

<a id="april-28-2026"></a>

## 2026. 04. 28.

<a id="added-features-2"></a>

### 신규 기능 추가

* 대시보드 템플릿 기능 추가
    * 대시보드 생성 시 미리 구성된 템플릿을 선택하여 대시보드를 간편하게 생성할 수 있습니다.
    * 서비스별 템플릿을 선택하고 미리보기로 위젯 구성과 레이아웃을 확인할 수 있습니다.
* 동적 필터 기능 추가
    * 대시보드 상단의 동적 필터로 대시보드 내 모든 위젯의 데이터를 일괄적으로 필터링할 수 있습니다.
    * 동적 필터 관리 모달에서 필터를 추가하거나 수정할 수 있으며, 위젯별로 동적 필터 적용 여부를 설정할 수 있습니다.
* 집계 기능 추가
    * 위젯 및 알림에서 수집된 지표 데이터를 평균, 최소, 최대 등의 집계 함수로 자동 계산하여 표시할 수 있습니다.
    * 조회 기간에 따라 데이터 간격이 자동 조정될 때, 간격 내 모든 데이터를 집계하여 반영하므로 데이터 누락 없이 전체적인 흐름을 파악할 수 있습니다.
    * 지표별로 집계 사용 여부를 선택할 수 있으며, 집계를 사용하지 않는 경우 기존과 동일하게 원본 데이터를 표시합니다.

<a id="september-23-2025"></a>

## 2025. 09. 23.

<a id="added-features-3"></a>

### 신규 기능 추가

* 신규 Cloud Monitoring Agent 출시
    * Cloud Monitoring 신규 Instance용 Agent가 출시되었습니다.
    * [신규 Agent 설치 가이드](new-instance-metric.md)를 참고하여 설치할 수 있습니다.

<a id="july-29-2026"></a>

## 2025. 07. 29.

<a id="added-features-4"></a>

### 신규 기능 추가

* 지표 조회 가능 서비스 추가
    * Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.
    * 아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.
        * Cloud Functions

<a id="june-24-2025"></a>

## 2025. 06. 24.

<a id="added-features-5"></a>

### 신규 기능 추가

* 지표 조회 가능 서비스 추가
    * Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.
    * 아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.
        * SMS

<a id="june-10-2025"></a>

## 2025. 06. 10.

<a id="feature-updates"></a>

### 기능 개선/변경

* SMS 알림 내용 추가
    * 알림 발송 시 SMS 내용에 항목이 추가되었습니다.
    * 알림이 발생한 서비스가 Instance인 경우 Instance Name 항목이 추가되었습니다.

<a id="may-27-2025"></a>

## 2025. 05. 27.

<a id="added-features-6"></a>

### 신규 기능 추가

* 지표 조회 가능 서비스 추가
    * Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.
    * 아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.
        * VPC
        * Subnet
        * Floating IP

<a id="march-4-2025"></a>

## 2025. 03. 04.

<a id="added-features-7"></a>

### 신규 기능 추가

* 지표 조회 가능 서비스 추가
    * Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.
    * 아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.
        * Direct Connect

<a id="february-11-2025"></a>

## 2025. 02. 11.

<a id="added-features-8"></a>

### 신규 기능 추가

* 지표 조회 가능 서비스 추가
    * Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.
    * 아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.
        * Colocation Gateway
        * Load Balancer

<a id="october-29-2024"></a>

## 2024. 10. 29.

<a id="added-features-9"></a>

### 신규 기능 추가

* 커스텀 웹훅 지원
    * 알림 수신 그룹의 커스텀 웹훅을 사용하여 Cloud Monitoring 알림을 웹훅으로 받을 수 있습니다.

<a id="feature-updates-2"></a>

### 기능 개선/변경

* 권한 세분화 적용
    * Cloud Monitoring에 프로젝트 서비스 이용 역할이 추가되었습니다.
    * Cloud Monitoring ADMIN: Cloud Monitoring 서비스 Create(생성), Read(읽기), Update(갱신), Delete(삭제)
    * Cloud Monitoring VIEWER: Cloud Monitoring 서비스 Read(읽기)

<a id="august-27-2024"></a>

## 2024. 08. 27.

<a id="added-features-10"></a>

### 신규 기능 추가

* 지표 조회 가능 서비스 추가
    * Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.
    * 아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.
        * Transit Hub
        * Internet Gateway

<a id="july-23-2024"></a>

## 2024. 07. 23.

<a id="bug-fixes"></a>

### 버그 수정

* [콘솔] 위젯 및 알림 추가/수정 페이지의 텍스트 입력 창에서, 엔터 키 입력 시 의도치 않게 저장이 시도되는 현상을 수정했습니다.

<a id="may-28-2024"></a>

## 2024. 05. 28.

<a id="added-features-11"></a>

### 신규 기능 추가

* 신규 서비스 출시
    * Cloud Monitoring은 NHN Cloud의 리소스 지표를 수집·제공하고, 이상이 발생하면 알림을 제공하는 서비스입니다.
    * Instance, GPU Instance, NCS 등 NHN Cloud 내 리소스의 시스템 및 서비스 지표를 수집, 제공합니다.
    * 유연한 대시보드 생성 및 관리 기능으로 리소스 상태를 쉽게 파악할 수 있습니다.
    * 조직 및 프로젝트 대시보드 또는 모니터링 콘솔에서 원하는 형태의 지표 차트를 구성할 수 있으며, 지표가 특정 임계치에 도달할 경우 미리 지정한 알림 수신 대상에게 이메일, SMS 등으로 알림을 보내도록 설정할 수 있습니다.

## Monitoring > Cloud Monitoring > 릴리스 노트

### 2025. 06. 10.

#### SMS 알림 내용 추가

알림 발송 시 SMS 내용에 항목이 추가되었습니다.
알림 발생한 서비스가 Instance인 경우 Instance Name 항목이 추가되었습니다.

### 2025. 05. 27.

#### 지표 조회 가능 서비스 추가

Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.  
아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.

* VPC
* Subnet
* Floating IP


### 2025. 03. 04.

#### 지표 조회 가능 서비스 추가

Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.  
아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.

* Direct Connect

### 2025. 02. 11.

#### 지표 조회 가능 서비스 추가

Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.  
아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.

* Colocation Gateway
* Load Balancer

### 2024. 10. 29.

#### 권한 세분화 적용
Cloud Monitoring에 프로젝트 서비스 이용 역할이 추가되었습니다.

* Cloud Monitoring ADMIN: Cloud Monitoring 서비스 Create(생성), Read(읽기), Update(갱신), Delete(삭제)
* Cloud Monitoring VIEWER: Cloud Monitoring Read(읽기)

#### 커스텀 웹훅 지원
알림 수신 그룹의 커스텀 웹훅을 사용하여 Cloud Monitoring 알림을 웹훅으로 받을 수 있습니다.

### 2024. 08. 27.

#### 지표 조회 가능 서비스 추가

Cloud Monitoring에서 지표 조회가 가능한 서비스가 추가되었습니다.  
아래 서비스의 지표는 지표 관리 화면에서 수집 설정 후, 대시보드에서 확인할 수 있습니다.

* Transit Hub
* Internet Gateway

### 2024. 07. 23.

#### 버그 수정
* [Console] 위젯 및 알림 추가/수정 페이지의 텍스트 입력 창에서, 엔터 키 입력 시 의도치 않게 저장이 시도되는 현상을 수정했습니다.

### 2024. 05. 28.

#### 신규 서비스 출시
Cloud Monitoring은 NHN Cloud의 리소스에 대한 지표를 수집/제공하고 이상에 대한 알림을 제공하는 서비스입니다.

* Instance, GPU Instance, NCS 등 NHN Cloud 내 리소스에 대한 시스템 및 서비스 지표를 수집, 제공합니다.
* 유연한 대시보드 생성 및 관리기능을 통해 리소스 상태를 쉽게 파악할 수 있습니다.
* 조직 및 프로젝트 대시보드 또는 모니터링 콘솔에서 원하는 형태의 지표 차트를 구성할 수 있으며, 지표가 특정 임계치에 도달할 경우 미리 지정한 알림 수신 대상에게 이메일, SMS 등을 통해 알림을 보내도록 설정할 수 있습니다.

## Monitoring > Cloud Monitoring > 사용 시나리오
대시보드 구성부터 알림 생성까지 전반적인 사용 시나리오를 다룹니다.<br>
Cloud Monitoring을 사용하는 순서는 다음과 같습니다. 

- 서비스 선택<br>
  Cloud Monitoring은 프로젝트 생성 시 기본으로 제공되는 서비스 입니다.<br>
  따라서 별도의 작업 없이 프로젝트를 생성한 후 서비스를 사용할 수 있습니다.<br>
  프로젝트 생성 방법은 [NHN Cloud 콘솔 사용 가이드](https://docs.nhncloud.com/ko/nhncloud/ko/console-guide/)를 참고해주세요.
- 지표 수집 설정<br>
  각 서비스별로 지표 수집을 설정합니다.
- 대시보드 구성<br>
  대시보드에 위젯을 추가하여 자유롭게 구성합니다.
- 알림 생성<br>
  임계치를 설정하여 이벤트 발생 시 알림을 받을 수 있습니다.

## 지표 수집 설정
대시보드를 구성하기 위해 먼저 서비스별로 지표 수집 설정을 합니다.

1. **Cloud Monitoring > 지표 관리**를 선택합니다.
2. 지표 관리 페이지에서 Cloud Monitoring이 제공하는 서비스별 지표를 확인합니다.
3. 원하는 서비스의 **지표 수집 설정 토글을 ON**으로 변경합니다.
4. ‘지표 수집을 시작하시겠습니까?’ 모달이 표시되면 **확인 버튼**을 클릭합니다.
5. 수집이 시작되면 해당 지표를 사용하여 위젯을 추가할 수 있습니다.

![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/bb42aa0c-f8f8-4ed6-bc58-9b9e4a15cec6)

- Instance, GPU Instance 서비스는 기본으로 제공되는 지표입니다.
- 활성화된 서비스만 지표가 수집됩니다. 서비스가 활성화되었는지 확인해주세요.
- 지표 수집 설정 토글을 OFF하면 해당 지표의 수집이 중단되며 대시보드에서 표시되지 않습니다.

## 대시보드 구성
이제 대시보드를 구성할 수 있는 준비가 되었습니다.<br>
대시보드를 생성하고 위젯을 추가해보겠습니다.

### 대시보드 생성
1. **+대시보드 생성** 버튼을 클릭합니다.
2. **대시보드 이름과 설명을 입력**한 후 확인 버튼을 클릭합니다.
3. 생성된 대시보드를 확인합니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/87598547-0d55-498b-8a61-02eca1bdb5db)
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/58097ff9-1f6c-4693-a2f3-82cdf382056f)



### 위젯 추가
1. **위젯 추가** 버튼을 클릭하여 위젯 추가 페이지로 이동합니다.
2. **위젯의 이름** 입력하고, **그래프 유형과 서비스를 선택**합니다.
   - 지표 관리에서 수집 설정된 서비스만 선택할 수 있습니다.
3. 선택한 서비스에 해당하는 **리소스 유형과 지표 항목을 선택**합니다.
   - 선택한 지표 항목별로 필터와 범례를 설정할 수 있는 박스가 표시됩니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/9e20e916-7501-41b2-b24f-6961af8b026d)
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/5b739451-7084-4928-8d36-13a68ee6f9e7)

4. **필터를 설정**하여 원하는 지표만 선택적으로 확인할 수 있습니다.
   - 예시) 한국(판교) 리전에만 있는 특정 인스턴스만 모니터링하고 싶을 경우 다음과 같이 설정합니다.
     - +추가 버튼을 클릭하여 필터를 추가합니다.
     - 레이블, 연산자, 조건 순으로 리전 =  kr1(한국(판교)) 필터를 설정합니다.
     - 필터를 추가하여 인스턴스 = {인스턴스 이름}을 선택합니다.
     - 이렇게 하면 kr1(한국(판교)) 리전의 특정 인스턴스 지표가 그래프에 표시됩니다.
5. 필요에 따라 **범례 명칭, 단위, Y축 위치를 설정**할 수 있습니다.
   - 지표별 단위가 같으면 1개의 Y축으로 표시됩니다.
   - Y축 위치 설정에서 자동은 지표별 단위가 다를 경우 좌측, 우측 순서로 Y축을 자동 배치합니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/c2d9ca1d-45c0-4d6c-92b6-c36c44748925)

6. **미리보기 기능**을 사용하여 원하는 형태의 그래프가 그려졌는지 확인합니다.
7. 확인이 완료되면 **추가** 버튼을 클릭하여 대시보드에 위젯을 추가합니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/3e194309-7b0d-427c-bf93-64fb2fc7a00a)


### 대시보드 편집
대시보드에 추가된 위젯을 확인하고 원하는 형태로 편집합니다.

1. 대시보드를 조회 모드에서 **편집 모드**로 변경합니다.
2. 위젯을 **드래그하여 위치를 변경**하거나, **위젯 그룹을 추가**하여 대시보드를 정리합니다.
   - **위젯 그룹 추가**를 클릭하면 하단에 그룹이 추가됩니다. 위젯을 그룹으로 드래그하여 배치합니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/83543ece-bfd0-434f-bcc6-d117b3f18942)

## 알림 설정
더 효율적인 모니터링을 위해 이벤트 발생 시 알림을 수신 받을 수 있도록 설정합니다.

### 알림 생성
1. **Cloud Monitoring > 알림 관리 > 알림 설정**을 선택합니다.
2. **알림 생성** 버튼을 클릭하여 생성 페이지로 이동합니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/50e2c389-e784-4b9b-84ab-08359da04c1a)

3. **알림 이름**을 입력하고, **서비스를 선택**합니다.
4. 선택한 서비스에 해당하는 **리소스 유형과 지표 항목을 선택**합니다.
   - 선택한 지표 항목별 필터와 알림 조건을 설정할 수 있는 박스가 표시됩니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/23b67551-d97c-4bf9-8a58-009e89d38fbc)

5. 원하는 지표에 알림을 설정하기 위해 **필터를 설정**합니다.
6. 알림을 발생할 조건인 **임계치**와 **지속시간**을 입력합니다.
   - 예시) CPU 사용률이 30% 이상이며, 3분 이상 지속 시 알림을 받고 싶을 경우 다음과 같이 설정합니다.
     - 지표 항목을 CPU 사용률로 선택하고, 필요에 따라 필터를 설정합니다.
     - 비교 방법은 >=(이상)을 선택합니다.
     - 임계치는 30을 입력하고, 지속 시간은 3을 입력합니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/30b3c669-d180-433d-9652-9a65a18f17ba)

7. **알림 수신 대상을 선택**합니다.
   - 프로젝트에서 생성한 알림 수신 그룹을 수신 대상으로 선택할 수 있습니다.
   - 프로젝트 알림 수신 그룹을 먼저 생성해주세요.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/65e5d9ca-86e1-4d0d-b260-fad9817e4ac5)

알림을 설정하기 번거로운 경우, 대시보드 위젯에서 빠르게 설정할 수 있습니다.

1. 위젯 더보기 버튼에서 **알림 생성**을 클릭합니다.
2. 알림 생성 페이지로 이동하며, **위젯 생성 시 선택한 지표별 필터가 그대로 적용**됩니다.
![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/9ef138c3-51ef-4463-ae97-14098331a1e1)

이제 설정한 임계치를 달성하면 알림이 발생되며, 발생 이력은 **알림 관리 > 알림 발생 이력**에서 확인할 수 있습니다.

## 프로젝트 대시보드 노출 설정
Cloud Monitoring 서비스에서 생성한 대시보드를 프로젝트 메인 화면에서 확인할 수 있습니다.

1. **Cloud Monitoring 대시보드 - 대시보드 관리**를 클릭합니다.
2. 테이블 우측에 **프로젝트 대시보드 노출 설정 토글 버튼을 ON**으로 변경합니다.
   ![image](https://github.com/TOAST-DOCS/Monitoring-Cloud-Monitoring/assets/101690965/8e2383b5-99c5-4d7d-ac17-9a406af90869)

**프로젝트 > 커스텀 대시보드**에서도 설정한 대시보드를 확인하여 신속하게 모니터링할 수 있습니다.

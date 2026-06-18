## Monitoring > Cloud Monitoring > Instance 신규 지표 연동 가이드

## 개요

Cloud Monitoring 서비스에서 Instance의 상세 지표를 수집하려면 신규 Agent를 설치해야 합니다.
신규 Agent는 기존 Agent와는 별개로 동작하며, 더 정확하고 상세한 인스턴스 지표를 제공합니다.

> [주의]
> 오토 스케일 그룹에 속한 인스턴스의 경우 오토 스케일링 기능이 정상 동작하지 않을 수 있습니다.

전체 진행 순서는 다음과 같습니다.
1. 신규 Agent 설치
2. 기존 Agent 삭제(선택 사항)

## 신규 Agent 설치 가이드

### Linux 인스턴스 Agent 설치

#### 설치 스크립트
```bash
rm -f ./install-nhncloud-telegraf.sh
curl -s -o install-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/install-nhncloud-telegraf.sh'
chmod 755 ./install-nhncloud-telegraf.sh
sudo ./install-nhncloud-telegraf.sh
```

#### 설치 확인
```bash
sudo systemctl status nhncloud-telegraf
```

### Windows 인스턴스 Agent 설치
* PowerShell을 관리자 권한으로 실행
   - 시작 메뉴에서 **PowerShell**을 검색합니다.
   - **Windows PowerShell**을 마우스 오른쪽 버튼으로 클릭한 뒤 **관리자 권한으로 실행**을 선택합니다.

#### 설치 스크립트
```powershell
Remove-Item install-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/install-nhncloud-telegraf.ps1' -OutFile 'install-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File install-nhncloud-telegraf.ps1
```

#### 설치 확인
```powershell
Get-Service -Name "nhncloud-telegraf"
```

## 기존 Agent 삭제 가이드(선택 사항)

> [참고]
> 신규 Agent와 기존 Agent를 동시에 사용할 수도 있습니다.

기존 System Monitoring Agent를 삭제하는 가이드입니다. 신규 Agent와 기존 Agent는 동시에 설치되어 있어도 문제없이 동작합니다.

### 삭제 시 주의 사항
기존 Agent를 삭제하기 전에 신규 Agent가 정상적으로 설치되고 동작하는지 반드시 확인합니다.

### Linux 인스턴스 기존 Agent 삭제

#### 삭제 스크립트
```bash
curl -s -o uninstall-sysmon-agent.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-sysmon-agent.sh'
chmod 755 ./uninstall-sysmon-agent.sh
sudo ./uninstall-sysmon-agent.sh
```

#### 삭제 확인
기존 Agent의 서비스 상태를 확인합니다(서비스가 없어야 정상).
```bash
sudo systemctl status toast-sysmon
```

### Windows 인스턴스 기존 Agent 삭제
#### 삭제 스크립트
```powershell
& "C:\Program Files (x86)\NHN\TOAST\uninst.exe"
```

#### 삭제 확인
기존 Agent 프로세스가 종료되었는지 확인합니다.
```powershell
Get-Process -Name "toastmon" -ErrorAction SilentlyContinue
```

### 신규 Agent 삭제(필요 시)

#### Linux 인스턴스 신규 Agent 삭제

##### 삭제 스크립트
```bash
rm -f ./uninstall-nhncloud-telegraf.sh
curl -s -o uninstall-nhncloud-telegraf.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-nhncloud-telegraf.sh'
chmod 755 ./uninstall-nhncloud-telegraf.sh
sudo ./uninstall-nhncloud-telegraf.sh
```

#### Windows 인스턴스 신규 Agent 삭제

##### 삭제 스크립트
```powershell
Remove-Item uninstall-nhncloud-telegraf.ps1 -ErrorAction SilentlyContinue
Invoke-WebRequest -Uri 'http://169.254.169.231/monitoring/cloud-agent/windows-amd64/uninstall-nhncloud-telegraf.ps1' -OutFile 'uninstall-nhncloud-telegraf.ps1'
powershell -ExecutionPolicy Bypass -File uninstall-nhncloud-telegraf.ps1
```

## Metric Dictionary

|지표명|리소스명|기본 범례(Legend)|단위(Unit)|
|-------|-------|------|------|
|CPU 사용률(%)|CPU (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 코어 개수|CPU (New)|{{nhncloud_instance_id}}|숫자|
|코어별 CPU 사용률(%)|CPU (New)|{{nhncloud_instance_id}} cpu={{cpu}}|백분율(0-100)|
|CPU 평균 부하(1m)|CPU (New)|{{nhncloud_instance_id}} - 1m|숫자|
|CPU 평균 부하(5m)|CPU (New)|{{nhncloud_instance_id}} - 5m|숫자|
|CPU 평균 부하(15m)|CPU (New)|{{nhncloud_instance_id}} - 15m|숫자|
|CPU 상세(user)(%)|CPU (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(nice)(%)|CPU (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(system)(%)|CPU (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(iowait)(%)|CPU (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(steal)(%)|CPU (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|메모리 사용률(%)|Memory (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|메모리 상세(used)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(available)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(free)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(cached)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(buffered)(Bytes)|Memory (New)|{{nhncloud_instance_id}}|바이트(bytes)|
|디스크 사용률(%)|Disk (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|장치별 디스크 사용률(%)|Disk (New)|{{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}}|백분율(0-100)|
|디스크 읽기(B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|디스크 쓰기(B/s)|Disk I/O (New)|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|장치별 디스크 읽기(B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|초당 바이트(bytes/s)|
|장치별 디스크 쓰기(B/s)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|초당 바이트(bytes/s)|
|장치별 처리 중인 작업 수|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|숫자|
|장치별 IO 사용률(%)|Disk I/O (New)|{{nhncloud_instance_id}} device={{name}}|백분율(0-100)|
|네트워크 데이터 수신(B/s)|Network (New)|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|네트워크 데이터 송신(B/s)|Network (New)|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|장치별 네트워크 데이터 수신(B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|초당 바이트(bytes/s)|
|장치별 네트워크 데이터 송신(B/s)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|초당 바이트(bytes/s)|
|네트워크 데이터 수신(bps)|Network (New)|{{nhncloud_instance_id}}|초당 비트(bit/s)|
|네트워크 데이터 송신(bps)|Network (New)|{{nhncloud_instance_id}}|초당 비트(bit/s)|
|장치별 네트워크 데이터 수신(bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|초당 비트(bit/s)|
|장치별 네트워크 데이터 송신(bps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|초당 비트(bit/s)|
|네트워크 패킷 수신(pps)|Network (New)|{{nhncloud_instance_id}}|초당 패킷(packets/s)|
|네트워크 패킷 송신(pps)|Network (New)|{{nhncloud_instance_id}}|초당 패킷(packets/s)|
|장치별 네트워크 패킷 수신(pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|초당 패킷(packets/s)|
|장치별 네트워크 패킷 송신(pps)|Network (New)|{{nhncloud_instance_id}} interface={{interface}}|초당 패킷(packets/s)|
|가동시간(s)|System (New)|{{nhncloud_instance_id}}|시간(second)|
|스왑 사용률(%)|Swap (New)|{{nhncloud_instance_id}}|백분율(0-100)|
|스왑 사용량(used)(Bytes)|Swap (New)|{{nhncloud_instance_id}}|바이트(bytes)|
|스왑 사용량(free)(Bytes)|Swap (New)|{{nhncloud_instance_id}}|바이트(bytes)|
|스왑 사용량(total)(Bytes)|Swap (New)|{{nhncloud_instance_id}}|바이트(bytes)|

## GPU Instance Metric Dictionary

> [참고]
> GPU 지표는 GPU Instance에서 DCGM(Data Center GPU Manager) 기반으로 수집되며, 신규 Cloud Monitoring Agent가 설치된 GPU Instance에서만 조회할 수 있습니다.
> GPU 모델(V100/A100/T4) 및 드라이버 버전에 따라 일부 지표는 수집되지 않을 수 있습니다.

|지표명|리소스명|기본 범례(Legend)|단위(Unit)|
|-------|-------|------|------|
|GPU 사용률(%)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|백분율(0-100)|
|GPU 메모리 사용률(%)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|백분율(0-100)|
|GPU 메모리 대역폭 사용률(%)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|백분율(0-100)|
|GPU 전력 사용량(W)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|와트(W)|
|GPU 온도(°C)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|섭씨(°C)|
|GPU 메모리 온도(°C)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|섭씨(°C)|
|SM 클럭(MHz)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|메가헤르츠(MHz)|
|메모리 클럭(MHz)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|메가헤르츠(MHz)|
|인코더 사용률(%)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|백분율(0-100)|
|디코더 사용률(%)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|백분율(0-100)|
|GPU 여유 메모리(MiB)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|메비바이트(MiB)|
|GPU 예약 메모리(MiB)|GPU 성능|{{nhncloud_instance_id}} - gpu={{gpu}}|메비바이트(MiB)|
|PCIe 재전송 비율(count/s)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 카운트(count/s)|
|XID 에러|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|ECC 단일비트 에러 - 누적(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|ECC 단일비트 에러 - 변동(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|ECC 이중비트 에러 - 누적(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|ECC 이중비트 에러 - 변동(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|격리 페이지 - SBE(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|격리 페이지 - DBE(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|격리 대기 페이지(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|리매핑 행 - 교정 가능(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|리매핑 행 - 교정 불가(count)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|리매핑 실패 여부|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|숫자|
|NVLink CRC Flit 에러 비율(count/s)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 카운트(count/s)|
|NVLink CRC Data 에러 비율(count/s)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 카운트(count/s)|
|NVLink Replay 에러 비율(count/s)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 카운트(count/s)|
|NVLink Recovery 에러 비율(count/s)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 카운트(count/s)|
|NVLink 대역폭 - Total(KiB/s)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 키비바이트(KiB/s)|
|NVLink 대역폭 - L0(B/s)|GPU 상태|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 바이트(bytes/s)|
|전력 스로틀링 비율(µs/s)|GPU 클럭 이벤트|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 마이크로초(µs/s)|
|온도 스로틀링 비율(µs/s)|GPU 클럭 이벤트|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 마이크로초(µs/s)|
|보드 제한 스로틀링 비율(µs/s)|GPU 클럭 이벤트|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 마이크로초(µs/s)|
|저사용률 스로틀링 비율(µs/s)|GPU 클럭 이벤트|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 마이크로초(µs/s)|
|동기 부스트 스로틀링 비율(µs/s)|GPU 클럭 이벤트|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 마이크로초(µs/s)|
|신뢰성 스로틀링 비율(µs/s)|GPU 클럭 이벤트|{{nhncloud_instance_id}} - gpu={{gpu}}|초당 마이크로초(µs/s)|

### GPU Instance 필터(Filter)

|필터명|설명|
|------|------|
|리전|GPU Instance가 위치한 리전|
|인스턴스|GPU Instance의 이름|
|GPU|인스턴스 내 GPU 장치 번호|

### GPU Instance 범례(Legend)

|범례명|설명|
|------|------|
|nhncloud_instance_id|GPU Instance의 이름|
|gpu|인스턴스 내 GPU 장치 번호|

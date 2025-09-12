## Monitoring > Cloud Monitoring > Instance 신규 지표 연동 가이드

## 개요

Cloud Monitoring 서비스에서 Instance의 상세 지표를 수집하기 위해서는 신규 Agent를 설치해야 합니다. 신규 Agent는 기존 Agent와는 별개로 동작하며, 더 정확하고 상세한 인스턴스 지표를 제공합니다.

**전체 진행 순서:**
1. 신규 Agent 설치
2. 신규 Agent 동작 확인
3. 구 Agent 삭제 (선택사항)

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
   - 시작 메뉴에서 "PowerShell" 검색
   - "Windows PowerShell" 우클릭 후 "관리자 권한으로 실행" 선택

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

## 구 Agent 삭제 가이드 (선택사항)

> 💡 **참고**: 신규 Agent와 구 Agent를 동시에 사용할 수도 있습니다.

기존 System Monitoring Agent를 제거하기 위한 삭제 가이드입니다. **신규 Agent와 구 Agent는 동시에 설치되어 있어도 문제없이 동작합니다.**

### 삭제 시 주의사항
- **삭제 전 필수 확인**: 신규 Agent가 정상적으로 설치되고 동작하는지 확인

### Linux 인스턴스 구 Agent 삭제

#### 삭제 스크립트
```bash
curl -s -o uninstall-sysmon-agent.sh 'http://169.254.169.231/monitoring/cloud-agent/linux-amd64/uninstall-sysmon-agent.sh'
chmod 755 ./uninstall-sysmon-agent.sh
sudo ./uninstall-sysmon-agent.sh
```

#### 삭제 확인
* 구 Agent 서비스 상태 확인 (서비스가 없어야 정상)
```bash
sudo systemctl status toast-sysmon
```

### Windows 인스턴스 구 Agent 삭제
#### 삭제 스크립트
```powershell
& "C:\Program Files (x86)\NHN\TOAST\uninst.exe"
```

#### 삭제 확인
* 구 Agent 프로세스 종료 확인
```powershell
Get-Process -Name "toastmon" -ErrorAction SilentlyContinue
```

### 신규 Agent 삭제 (필요시)

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
> TODO (이용희)
> 신규 지표 사전 추가

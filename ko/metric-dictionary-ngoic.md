## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- NHN Cloud 내 서비스에 대한 모니터링을 위한 지표들을 정의한 목록입니다.
- 지표 사전을 통해 모니터링 대상 서비스의 지표를 확인하고, 이해할 수 있습니다.
- 위젯 구성 시 필요한 지표를 찾아 사용할 수 있습니다. 자세한 내용은 [콘솔 사용 가이드](console-guide-ninc.md)를 참고하십시오.
- **Metric List**에서 각 서비스별 지표 사전 목록을 확인할 수 있습니다.

### 필터(Filter)
- 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.
  - 예를 들어 리전 필터에 kr1을 적용하면 지표들 중 kr1 리전에 해당하는 지표만 표시됩니다.
- 공통 필터는 아래와 같습니다.

| 필터명 | 설명           | 값                        |
|-----|--------------|--------------------------|
| 리전  | NHN Cloud 리전 | kr1: 한국(판교), kr2: 한국(평촌) |

### 범례(Legend)
- 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.
  - 예를 들어 범례에 {{nhncloud_region}}를 적용하면 각 지표들의 이름이 kr1, kr2와 같이 리전명으로 표시됩니다.
- 공통 범례는 아래와 같습니다.

| 필터명             | 설명           | 값                        |
|-----------------|--------------|--------------------------|
| nhncloud_region | NHN Cloud 리전 | kr1: 한국(판교), kr2: 한국(평촌) |

## Instance
- NHN Cloud의 Instance 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List

|지표명|리소스명|기본 범례(Legend)|단위(Unit)|
|-------|-------|------|------|
|CPU 사용률 (%)|CPU|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 코어 개수|CPU|{{nhncloud_instance_id}}|숫자|
|코어별 CPU 사용률 (%)|CPU|{{nhncloud_instance_id}} cpu={{cpu}}|백분율(0-100)|
|CPU 평균 부하(1m)|CPU|{{nhncloud_instance_id}} - 1m|숫자|
|CPU 평균 부하(5m)|CPU|{{nhncloud_instance_id}} - 5m|숫자|
|CPU 평균 부하(15m)|CPU|{{nhncloud_instance_id}} - 15m|숫자|
|CPU 상세(user) (%)|CPU|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(nice) (%)|CPU|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(system) (%)|CPU|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(iowait) (%)|CPU|{{nhncloud_instance_id}}|백분율(0-100)|
|CPU 상세(steal) (%)|CPU|{{nhncloud_instance_id}}|백분율(0-100)|
|메모리 사용률 (%)|Memory|{{nhncloud_instance_id}}|백분율(0-100)|
|메모리 상세(used) (Bytes)|Memory|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(available) (Bytes)|Memory|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(free) (Bytes)|Memory|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(cached) (Bytes)|Memory|{{nhncloud_instance_id}}|바이트(bytes)|
|메모리 상세(buffered) (Bytes)|Memory|{{nhncloud_instance_id}}|바이트(bytes)|
|디스크 사용률 (%)|Disk|{{nhncloud_instance_id}}|백분율(0-100)|
|장치별 디스크 사용률 (%)|Disk|{{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}}|백분율(0-100)|
|디스크 읽기 (B/s)|Disk I/O|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|디스크 쓰기 (B/s)|Disk I/O|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|장치별 디스크 읽기 (B/s)|Disk I/O|{{nhncloud_instance_id}} device={{name}}|초당 바이트(bytes/s)|
|장치별 디스크 쓰기 (B/s)|Disk I/O|{{nhncloud_instance_id}} device={{name}}|초당 바이트(bytes/s)|
|장치별 처리 중인 작업 수|Disk I/O|{{nhncloud_instance_id}} device={{name}}|숫자|
|장치별 IO 사용률 (%)|Disk I/O|{{nhncloud_instance_id}} device={{name}}|백분율(0-100)|
|네트워크 데이터 수신 (B/s)|Network|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|네트워크 데이터 송신 (B/s)|Network|{{nhncloud_instance_id}}|초당 바이트(bytes/s)|
|장치별 네트워크 데이터 수신 (B/s)|Network|{{nhncloud_instance_id}} interface={{interface}}|초당 바이트(bytes/s)|
|장치별 네트워크 데이터 송신 (B/s)|Network|{{nhncloud_instance_id}} interface={{interface}}|초당 바이트(bytes/s)|
|네트워크 데이터 수신 (bps)|Network|{{nhncloud_instance_id}}|초당 비트(bit/s)|
|네트워크 데이터 송신 (bps)|Network|{{nhncloud_instance_id}}|초당 비트(bit/s)|
|장치별 네트워크 데이터 수신 (bps)|Network|{{nhncloud_instance_id}} interface={{interface}}|초당 비트(bit/s)|
|장치별 네트워크 데이터 송신 (bps)|Network|{{nhncloud_instance_id}} interface={{interface}}|초당 비트(bit/s)|
|네트워크 패킷 수신 (pps)|Network|{{nhncloud_instance_id}}|초당 패킷(packets/s)|
|네트워크 패킷 송신 (pps)|Network|{{nhncloud_instance_id}}|초당 패킷(packets/s)|
|장치별 네트워크 패킷 수신 (pps)|Network|{{nhncloud_instance_id}} interface={{interface}}|초당 패킷(packets/s)|
|장치별 네트워크 패킷 송신 (pps)|Network|{{nhncloud_instance_id}} interface={{interface}}|초당 패킷(packets/s)|
|가동시간 (s)|System|{{nhncloud_instance_id}}|시간(second)|
|스왑 사용률 (%)|Swap|{{nhncloud_instance_id}}|백분율(0-100)|
|스왑 사용량(used) (Bytes)|Swap|{{nhncloud_instance_id}}|바이트(bytes)|
|스왑 사용량(free) (Bytes)|Swap|{{nhncloud_instance_id}}|바이트(bytes)|
|스왑 사용량(total) (Bytes)|Swap (New)|{{nhncloud_instance_id}}|바이트(bytes)|

### Instance 필터(Filter)
- Instance 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.

| 필터명  | 설명                                      |
|------|-----------------------------------------|
| 인스턴스 | NHN Cloud의 Instance 서비스에서 사용 중인 인스턴스의 이름 |

### Instance 범례(Legend)
- Instance 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 범례명                  | 설명                  |
|----------------------|---------------------|
| nhncloud_instance_id | 인스턴스의 이름            |
| cpu                  | 인스턴스의 CPU 번호        |
| device               | 인스턴스의 디스크 장치        |
| fstype               | 인스턴스의 파일 시스템 종류     |
| path                 | 인스턴스의 디스크 마운트 경로    |
| interface            | 인스턴스의 네트워크 인터페이스 이름 |

## Load Balancer
- NHN Cloud의 Load Balancer 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List

| 지표명                               | 리소스명      | 기본 범례(Legend)                                                 | 단위(Unit)      |
|-----------------------------------|-----------|---------------------------------------------------------------|---------------|
| 네트워크 수신 바이트                       | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 바이트     |
| 네트워크 송신 바이트                       | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 바이트     |
| 네트워크 수신 초당 비트 수(bps)              | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 초당 비트 (bit/s) |
| 네트워크 송신 초당 비트 수(bps)              | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 초당 비트 (bit/s) |
| 처리 대기 중인 요청 개수                    | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 숫자            |
| 연결 상태에 있는 세션 개수                   | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 숫자            |
| HTTP 100번대 응답을 한 횟수               | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 숫자      |
| HTTP 200번대 응답을 한 횟수               | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 숫자      |
| HTTP 300번대 응답을 한 횟수               | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 숫자      |
| HTTP 400번대 응답을 한 횟수               | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 숫자      |
| HTTP 500번대 응답을 한 횟수               | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 숫자      |
| HTTP 응답 중 100번~500번 외 다른 응답을 한 횟수 | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 5분 누적 숫자      |
| 해당 멤버로 로드 밸런싱된 총횟수                | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 숫자            |
| 오류 발생 연결 횟수                       | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 숫자            |
| 평균 응답시간                           | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | ms            |
| 해당 멤버의 활성 상태 값                    | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 숫자            |
| HTTP 응답이 정상적으로 반환된 총횟수            | 로드 밸런서 멤버 | {{loadbalancer_id}}/{{listener_id}}/{{pool_id}}/{{member_id}} | 숫자            |

### Load Balancer 필터(Filter)

| 필터명    | 설명                                   |
|--------|--------------------------------------|
| 로드 밸런서 | NHN CLoud Network 서비스에서 사용 중인 로드 밸런서 |

### Load Balancer 범례(Legend)

| 범례명             | 설명        |
|-----------------|-----------|
| loadbalancer_id | 로드 밸런서 이름 |
| listener_id     | 리스너 이름    |
| pool_id         | 멤버 그룹 이름  |
| member_id       | 멤버 이름     |

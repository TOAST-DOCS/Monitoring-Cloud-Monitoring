## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- NHN Cloud 내 서비스에 대한 모니터링을 위한 지표들을 정의한 목록입니다.
- 지표 사전을 통해 모니터링 대상 서비스의 지표를 확인하고, 이해할 수 있습니다.
- 위젯 구성 시 필요한 지표를 찾아 사용할 수 있습니다. 자세한 내용은 [콘솔 사용 가이드](console-guide.md)를 참고하십시오.
- **Metric List**에서 각 서비스별 지표 사전 목록을 확인할 수 있습니다.

### 필터(Filter)
- 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.
  - 예를 들어 리전 필터에 kr1을 적용하면 지표들 중 kr1 리전에 해당하는 지표만 표시됩니다.
- 공통 필터는 아래와 같습니다.

| 필터명 | 설명           | 값                                                                  |
|-----|--------------|--------------------------------------------------------------------|
| 리전  | NHN Cloud 리전 | kr1: 한국(판교), kr2: 한국(평촌), kr3: 한국(광주), us1: 미국(캘리포니아), jp1: 일본(도쿄) |

### 범례(Legend)
- 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.
  - 예를 들어 범례에 {{nhncloud_region}}를 적용하면 각 지표들의 이름이 kr1, kr2와 같이 리전명으로 표시됩니다.
- 공통 범례는 아래와 같습니다.

| 필터명             | 설명           | 값                                                                  |
|-----------------|--------------|--------------------------------------------------------------------|
| nhncloud_region | NHN Cloud 리전 | kr1: 한국(판교), kr2: 한국(평촌), kr3: 한국(광주), us1: 미국(캘리포니아), jp1: 일본(도쿄) |

## Instance
- NHN Cloud의 Instance 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List
| 지표명              | 리소스명    | 기본 범례(Legend)                                                              | 단위(Unit)         |
|------------------|---------|----------------------------------------------------------------------------|------------------|
| CPU 사용률          | CPU     |                                                                            | 백분율(0-100)       |
| 코어별 CPU 사용률      | CPU     | {{nhncloud_instance_id}} cpu={{cpu}}                                       | 백분율(0-100)       |
| CPU 상세(user)     | CPU     | {{nhncloud_instance_id}}                                                   | 비율(0.00 - 1.00)  |
| CPU 상세(nice)     | CPU     | {{nhncloud_instance_id}}                                                   | 비율(0.00 - 1.00)  |
| CPU 상세(system)   | CPU     | {{nhncloud_instance_id}}                                                   | 비율(0.00 - 1.00)  |
| CPU 상세(iowait)   | CPU     | {{nhncloud_instance_id}}                                                   | 비율(0.00 - 1.00)  |
| CPU 평균 부하(1m)    | CPU     | {{nhncloud_instance_id}}                                                   | 숫자               |
| CPU 평균 부하(5m)    | CPU     | {{nhncloud_instance_id}}                                                   | 숫자               |
| CPU 평균 부하(15m)   | CPU     | {{nhncloud_instance_id}}                                                   | 숫자               |
| 디스크 사용률          | Disk    | {{nhncloud_instance_id}}                                                   | 비율(0.00 - 1.00)  |
| 마운트별 디스크 사용률     | Disk    | {{nhncloud_instance_id}} device={{device}} fstype={{fstype}} path={{path}} | 비율(0.00 - 1.00)  |
| 디스크 읽기           | Disk    | {{nhncloud_instance_id}}                                                   | 초당 바이트(bytes/s)  |
| 디스크 쓰기           | Disk    | {{nhncloud_instance_id}}                                                   | 초당 바이트(bytes/s)  |
| 장치별 디스크 읽기       | Disk    | {{nhncloud_instance_id}} fstype={{fstype}}                                 | 초당 바이트(bytes/s)  |
| 장치별 디스크 쓰기       | Disk    | {{nhncloud_instance_id}} fstype={{fstype}}                                 | 초당 바이트(bytes/s)  |
| 메모리 사용률          | Memory  | {{nhncloud_instance_id}}                                                   | 백분율(0-100)       |
| 메모리 상세(used)     | Memory  | {{nhncloud_instance_id}}                                                   | 바이트(bytes)       |
| 메모리 상세(buffered) | Memory  | {{nhncloud_instance_id}}                                                   | 바이트(bytes)       |
| 메모리 상세(cached)   | Memory  | {{nhncloud_instance_id}}                                                   | 바이트(bytes)       |
| 메모리 상세(free)     | Memory  | {{nhncloud_instance_id}}                                                   | 바이트(bytes)       |
| 네트워크 데이터 송신      | Network | {{nhncloud_instance_id}}                                                   | 초당 바이트(bytes/s)  |
| 네트워크 데이터 수신      | Network | {{nhncloud_instance_id}}                                                   | 초당 바이트(bytes/s)  |
| 장치별 네트워크 데이터 송신  | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 초당 바이트(bytes/s)  |
| 장치별 네트워크 데이터 수신  | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 초당 바이트(bytes/s)  |
| 네트워크 패킷 송신       | Network | {{nhncloud_instance_id}}                                                   | 초당 패킷(packets/s) |
| 네트워크 패킷 수신       | Network | {{nhncloud_instance_id}}                                                   | 초당 패킷(packets/s) |
| 장치별 네트워크 패킷 송신   | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 초당 패킷(packets/s) |
| 장치별 네트워크 패킷 수신   | Network | {{nhncloud_instance_id}} interface={{interface}}                           | 초당 패킷(packets/s) |
| 프로세스 개수          | Process | {{nhncloud_instance_id}}                                                   | 숫자               |
| 스왑 사용량(used)     | Swap    | {{nhncloud_instance_id}}                                                   | 바이트(bytes)       |
| 스왑 사용량(free)     | Swap    | {{nhncloud_instance_id}}                                                   | 바이트(bytes)       |
| 스왑 사용량(total)    | Swap    | {{nhncloud_instance_id}}                                                   | 바이트(bytes)       |
| 스왑 사용률           | Swap    | {{nhncloud_instance_id}}                                                   | 비율(0.00 - 1.00)  |

### Instance 필터(Filter)
- Instance 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.

| 필터명  | 설명                                       |
|------|------------------------------------------|
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

## NHN Container Service(NCS)
- NHN Cloud의 NCS 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List
| 지표명           | 리소스명 | 기본 범례(Legend)                                                            | 단위(Unit)        |
|---------------|------|--------------------------------------------------------------------------|-----------------|
| CPU 사용률       | NCS  | {{label_ncs_container_nhncloud_com_workload_id}} container={{container}} | 백분율(0-100)      |
| 워크로드에 할당된 CPU | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 숫자              |
| 메모리 사용률       | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 백분율(0-100)      |
| 워크로드에 할당된 메모리 | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 메비바이트(MiB)      |
| GPU 사용률       | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 백분율(0-100)      |
| GPU 메모리 사용률   | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 백분율(0-100)      |
| GPU 전력 사용량    | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 메가와트(mW)        |
| GPU 온도        | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 섭씨(℃)           |
| 워크로드에 할당된 GPU | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 숫자              |
| 네트워크 데이터 수신   | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 초당 바이트(bytes/s) |
| 네트워크 데이터 송신   | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 초당 바이트(bytes/s) |
| 디스크 사용률       | NCS  | {{workload_id}} {{type}}                                                 | 백분율(0-100)      |
| 활성화 상태별 작업 수  | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 숫자              |
| 컨테이너의 프로세스 수  | NCS  | {{label_ncs_container_nhncloud_com_workload_id}}                         | 숫자              |

### NCS Filter
- NCS 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.

| 필터명  | 설명                                  |
|------|-------------------------------------|
| 워크로드 | NHN Cloud의 NCS 서비스에서 사용 중인 워크로드의 이름 |
| 타입   | 스토리지 종류                             |


### NCS Legend
- NCS 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 범례명                                          | 설명                             |
|----------------------------------------------|--------------------------------|
| label_ncs_container_nhncloud_com_workload_id | NHN Cloud의 NCS 서비스에서 사용 중인 워크로드의 이름 |
| workload_id                                  | NHN Cloud의 NCS 서비스에서 사용 중인 워크로드의 이름 |
| type                                         | 스토리지 종류                        |
| container                                    | 컨테이너의 이름                       |

## GPU
- NHN Cloud의 GPU 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List
| 지표명         | 리소스명 | 기본 범례(Legend) | 단위(Unit)   |
|-------------|------|---------------|------------|
| GPU 사용률     | GPU  | 없음            | 백분율(0-100) |
| GPU 온도      | GPU  | 없음            | 섭씨(℃)      |
| GPU 메모리 사용률 | GPU  | 없음            | 백분율(0-100) |
| GPU 전력 사용량  | GPU  | 없음            | 와트(W)      |

### GPU 필터(Filter)
- GPU 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.

| 필터명  | 설명                                  |
|------|-------------------------------------|
| 인스턴스 | NHN Cloud의 GPU 서비스에서 사용 중인 인스턴스의 이름 |

### GPU 범례(Legend)
- GPU 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 필터명                  | 설명           |
|----------------------|--------------|
| nhncloud_instance_id | GPU 인스턴스의 이름 |

## Transit Hub
- NHN Cloud의 Transit Hub 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List
| 지표명                                | 리소스명 | 기본 범례(Legend) | 단위(Unit)   |
|------------------------------------|------|---------------|------------|
| 네트워크 송신 바이트                        | 트랜짓 허브  | {{id}} | 5분 누적 바이트 |
| 네트워크 수신 바이트                        | 트랜짓 허브  | {{id}} | 5분 누적 바이트 |
| 네트워크 송신 패킷                         | 트랜짓 허브  | {{id}} | 5분 누적 패킷  |
| 네트워크 수신 패킷                         | 트랜짓 허브  | {{id}} | 5분 누적 패킷  |
| 경로가 일치하지 않아 삭제된 네트워크 패킷            | 트랜짓 허브  | {{id}} | 5분 누적 패킷  |
| 경로가 일치하지 않아 삭제된 네트워크 바이트           | 트랜짓 허브  | {{id}} | 5분 누적 바이트 |
| 블랙홀 경로와 일치하여 삭제된 네트워크 패킷           | 트랜짓 허브  | {{id}} | 5분 누적 패킷  |
| 블랙홀 경로와 일치하여 삭제된 네트워크 바이트          | 트랜짓 허브  | {{id}} | 5분 누적 바이트 |
| 네트워크 송신 바이트                        | 연결  | {{id}} | 5분 누적 바이트 |
| 네트워크 수신 바이트                        | 연결  | {{id}} | 5분 누적 바이트 |
| 네트워크 송신 패킷                         | 연결  | {{id}} | 5분 누적 패킷  |
| 네트워크 수신 패킷                         | 연결  | {{id}} | 5분 누적 패킷  |
| 경로가 일치하지 않아 삭제된 네트워크 패킷            | 연결  | {{id}} | 5분 누적 패킷  |
| 경로가 일치하지 않아 삭제된 네트워크 바이트           | 연결  | {{id}} | 5분 누적 바이트 |
| 블랙홀 경로와 일치하여 삭제된 네트워크 패킷           | 연결  | {{id}} | 5분 누적 패킷  |
| 블랙홀 경로와 일치하여 삭제된 네트워크 바이트          | 연결  | {{id}} | 5분 누적 바이트 |
| 네트워크 송신 초당 비트 수(bps)               | 트랜짓 허브  | {{id}} |  초당 비트(bits/s)  |
| 네트워크 수신 초당 비트 수(bps)               | 트랜짓 허브  | {{id}} |  초당 비트(bits/s)  |
| 네트워크 송신 초당 패킷 수(pps)               | 트랜짓 허브  | {{id}} |  초당 패킷(packets/s)  |
| 네트워크 수신 초당 패킷 수(pps)               | 트랜짓 허브  | {{id}} |  초당 패킷(packets/s)  |
| 경로가 일치하지 않아 삭제된 네트워크 초당 패킷 수(pps)  | 트랜짓 허브  | {{id}} |  초당 패킷(packets/s)  |
| 경로가 일치하지 않아 삭제된 네트워크 초당 비트 수(bps)  | 트랜짓 허브  | {{id}} |  초당 비트(bits/s)  |
| 블랙홀 경로와 일치하여 삭제된 네트워크 초당 패킷 수(pps) | 트랜짓 허브  | {{id}} |  초당 패킷(packets/s)  |
| 블랙홀 경로와 일치하여 삭제된 네트워크 초당 비트 수(bps) | 트랜짓 허브  | {{id}} |  초당 비트(bits/s)  |
| 네트워크 송신 초당 비트 수(bps)               | 연결  | {{id}} |  초당 비트(bits/s)  |
| 네트워크 수신 초당 비트 수(bps)               | 연결  | {{id}} | 초당 비트(bits/s)  |
| 네트워크 송신 초당 패킷 수(pps)               | 연결  | {{id}} |  초당 패킷(packets/s)  |
| 네트워크 수신 초당 패킷 수(pps)               | 연결  | {{id}} |  초당 패킷(packets/s)  |
| 경로가 일치하지 않아 삭제된 네트워크 초당 패킷 수(pps)  | 연결  | {{id}} |  초당 패킷(packets/s)  |
| 경로가 일치하지 않아 삭제된 네트워크 초당 비트 수(bps)  | 연결  | {{id}} |  초당 비트(bits/s)  |
| 블랙홀 경로와 일치하여 삭제된 네트워크 초당 패킷 수(pps) | 연결  | {{id}} |  초당 패킷(packets/s)  |
| 블랙홀 경로와 일치하여 삭제된 네트워크 초당 비트 수(bps) | 연결  | {{id}} |  초당 비트(bits/s)  |


### Transit Hub 필터(Filter)
- Transit Hub 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터 조건에 해당하는 지표만 표시됩니다.

#### 리소스 유형 > 트랜짓 허브인 경우 적용 가능한 필터

| 필터명 | 설명 |
| --- | --- |
| 트랜짓 허브 | NHN Cloud의 Network 서비스에서 사용 중인 트랜짓 허브 |

#### 리소스 유형 > 연결인 경우 적용 가능한 필터

| 필터명 | 설명                                      |
| --- |-----------------------------------------|
| 트랜짓 허브 | 연결과 관련된 트랜짓 허브 |
| 연결 | NHN Cloud의 Network 서비스에서 사용 중인 트랜짓 허브 연결 |

### Transit Hub 범례(Legend)
- Transit Hub 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 범례명            | 설명                         |
|----------------|----------------------------|
| id             | 트랜짓 허브 또는 연결 이름            |
| transit_hub_id | 트랜짓 허브 이름(리소스가 `연결`인 경우) |

## Internet Gateway
- NHN Cloud의 Internet Gateway 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List

| 지표명                          | 리소스명    | 기본 범례(Legend)          | 단위(Unit)         |
|------------------------------|---------|------------------------|------------------|
| 네트워크 송신 바이트                 | 라우팅 테이블 | {{id}} | 5분 누적 바이트        |
| 네트워크 수신 바이트                 | 라우팅 테이블 | {{id}} | 5분 누적 바이트        |
| 네트워크 송신 패킷                  | 라우팅 테이블 | {{id}} | 5분 누적 패킷         |
| 네트워크 수신 패킷                  | 라우팅 테이블 | {{id}} | 5분 누적 패킷         |
| 네트워크 송신 초당 비트 수(bps)        | 라우팅 테이블 | {{id}} | 초당 비트(bits/s)    | 
| 네트워크 수신 초당 비트 수(bps)	    | 라우팅 테이블 | {{id}} | 초당 비트(bits/s)    | 
| 네트워크 송신 초당 패킷 수(pps)	    | 라우팅 테이블 | {{id}} | 초당 패킷(packets/s) | 
| 네트워크 수신 초당 패킷 수(pps)	    | 라우팅 테이블 | {{id}} | 초당 패킷(packets/s) | 

### Internet Gateway 필터(Filter)
- Internet Gateway 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터 조건에 해당하는 지표만 표시됩니다.

| 필터명 | 설명 |
| --- | --- |
| 라우팅 테이블 | NHN Cloud의 Network 서비스에서 사용 중인 라우팅 테이블 |

### Internet Gateway 범례(Legend)
- Internet Gateway 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 범례명            | 설명                                     |
|----------------|----------------------------------------|
| id             | 라우링 테이블 이름  |

## Colocation Gateway
- NHN Cloud의 Colocation Gateway 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List

| 지표명                   | 리소스명        | 기본 범례(Legend) | 단위(Unit)         |
|-----------------------|-------------|---------------|------------------|
| 네트워크 송신 바이트           | 코로케이션 게이트웨이 | {{id}}        | 5분 누적 바이트        |
| 네트워크 수신 바이트           | 코로케이션 게이트웨이 | {{id}}        | 5분 누적 바이트        |
| 네트워크 송신 패킷            | 코로케이션 게이트웨이 | {{id}}        | 5분 누적 패킷         |
| 네트워크 수신 패킷            | 코로케이션 게이트웨이 | {{id}}        | 5분 누적 패킷         |
| 네트워크 송신 초당 비트 수(bps)  | 코로케이션 게이트웨이 | {{id}}        | 초당 비트(bits/s)    | 
| 네트워크 수신 초당 비트 수(bps)	 | 코로케이션 게이트웨이 | {{id}}        | 초당 비트(bits/s)    | 
| 네트워크 송신 초당 패킷 수(pps)	 | 코로케이션 게이트웨이 | {{id}}        | 초당 패킷(packets/s) | 
| 네트워크 수신 초당 패킷 수(pps)	 | 코로케이션 게이트웨이 | {{id}}        | 초당 패킷(packets/s) |

### Colocation Gateway 필터(Filter)

| 필터명         | 설명                                        |
|-------------|-------------------------------------------|
| 코로케이션 게이트웨이 | NHN Cloud Network 서비스에서 사용 중인 코로케이션 게이트웨이 |

### Colocation Gateway 범례(Legend)

| 범례명 | 설명             |
|-----|----------------|
| id  | 코로케이션 게이트웨이 이름 |

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


## Direct Connect
- NHN Cloud의 Direct Connect 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List

| 지표명                  | 리소스명    | 기본 범례(Legend) | 단위(Unit)      |
|----------------------|---------|---------------|---------------|
| 연결 상태                | Network | {{orderId}}   | 숫자            |
| 연결 수신 오류 수           | Network | {{orderId}}   | 숫자            |
| 연결 송신 오류 수           | Network | {{orderId}}   | 숫자            |
| 네트워크 송신 바이트          | Network | {{orderId}}   | 5분 누적 바이트     |
| 네트워크 수신 바이트          | Network | {{orderId}}   | 5분 누적 바이트     |
| 네트워크 송신 초당 비트 수(bps) | Network | {{orderId}}   | 초당 비트(bits/s) |
| 네트워크 수신 초당 비트 수(bps) | Network | {{orderId}}   | 초당 비트(bits/s) |

### Direct Connect 필터(Filter)

| 필터명    | 설명                                              |
|--------|-------------------------------------------------|
| 서비스 ID | NHN Cloud의 Direct Connect 서비스에서 사용 중인 서비스 신청 ID |

### Direct Connect 범례(Legend)

| 범례명     | 설명        |
|---------|-----------|
| orderId | 서비스 신청 ID |
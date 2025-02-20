## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- NHN Cloud 내 서비스에 대한 모니터링을 위한 지표들을 정의한 목록입니다.
- 지표 사전을 통해 모니터링 대상 서비스의 지표를 확인하고, 이해할 수 있습니다.
- 위젯 구성 시 필요한 지표를 찾아 사용할 수 있습니다. 자세한 내용은 [콘솔 사용 가이드](console-guide-gov.md)를 참고하십시오.
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

| 필터명  | 설명                               |
|------|----------------------------------|
| 워크로드 | NHN Cloud의 NCS 서비스에서 사용 중인 워크로드의 이름 |
| 타입   | 스토리지 종류                          |


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

| 필터명  | 설명           |
|------|--------------|
| 인스턴스 | NHN Cloud의 GPU 서비스에서 사용 중인 인스턴스의 이름 |

### GPU 범례(Legend)
- GPU 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 필터명                  | 설명           |
|----------------------|--------------|
| nhncloud_instance_id | GPU 인스턴스의 이름 |

## Direct Connect
- NHN Cloud의 Direct Connect 서비스에 대해 모니터링할 수 있는 지표를 정의한 사전입니다.

### Metric List

| 지표명                  | 리소스명    | 기본 범례(Legend) | 단위(Unit)      |
|----------------------|---------|---------------|---------------|
| 연결 상태                | Network | {{id}}        | 숫자            |
| 연결 수신 오류 수           | Network | {{id}}        | 숫자            |
| 연결 송신 오류 수           | Network | {{id}}        | 숫자            |
| 네트워크 송신 바이트          | Network | {{id}}        | 5분 누적 바이트     |
| 네트워크 수신 바이트          | Network | {{id}}        | 5분 누적 바이트     |
| 네트워크 송신 초당 비트 수(bps) | Network | {{id}}        | 초당 비트(bits/s) |
| 네트워크 수신 초당 비트 수(bps) | Network | {{id}}        | 초당 비트(bits/s) |

### Direct Connect 필터(Filter)

| 필터명    | 설명                                              |
|--------|-------------------------------------------------|
| 서비스 ID | NHN Cloud의 Direct Connect 서비스에서 사용 중인 서비스 신청 ID |

### Direct Connect 범례(Legend)

| 범례명     | 설명        |
|---------|-----------|
| orderId | 서비스 신청 ID |

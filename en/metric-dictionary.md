## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- 지표사전(Metric Dictionary) 에서는 NHN Cloud에서 제공하는 지표에 대한 설명을 제공합니다.

### 필터(Filter)
- 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.
    - 예를 들어 리전 필터에 kr1을 적용하면 지표들 중 kr1 리전에 해당하는 지표만 표시됩니다.
- 공통 필터는 아래와 같습니다.

| 필터 명 | 설명          | 값                                                              |
|------|-------------|----------------------------------------------------------------|
| 리전   | nhncloud 리전 | kr1:한국(판교), kr2:한국(평촌), kr3: 한국(광주), us1:미국(캘리포니아), jp1:일본(도쿄) |

### 범례(Legend)
- 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.
    - 예를 들어 범례에 {{nhncloud_region}}를 적용하면 각 지표들의 이름이 kr1, kr2와 같이 리전명으로 표시됩니다.
- 공통 범례는 아래와 같습니다.

| 필터 명            | 설명          | 값                                     |
|-----------------|-------------|---------------------------------------|
| nhncloud_region | nhncloud 리전 | kr1:판교, kr2:평촌, kr3: 광주, us:미국, jp:일본 |

## Instance
- NHN Cloud에서 제공하는 인스턴스 서버 지표에 대한 지표사전입니다.

### Metric List
| 한국어              | 리소스명    | 기본 범례(Legend)                                                              | 단위(Unit)         |
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

| 필터 명 | 설명                                          |
|------|---------------------------------------------|
| 인스턴스 | nhncloud instance 서비스 내에서 사용중인 instance의 이름 |

### Instance 범례(Legend)
- Instance 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 범례 명                 | 설명                      |
|----------------------|-------------------------|
| nhncloud_instance_id | instance의 이름            |
| cpu                  | instance의 CPU 번호        |
| device               | instance의 디스크 장치        |
| fstype               | instance의 파일 시스템 종류     |
| path                 | instance의 디스크 마운트 경로    |
| interface            | instance의 네트워크 인터페이스 이름 |

## NCS
- NHN Cloud에서 제공하는 NCS서비스의 지표에 대한 지표사전입니다.

### Metric List
| 한국어           | 리소스명 | 기본 범례(Legend)                                                            | 단위(Unit)        |
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

| 필터 명 | 설명                                 |
|------|------------------------------------|
| 워크로드 | nhncloud NCS 서비스 내에서 사용중인 워크로드의 이름 |
| 타입   | 스토리지 종류                            |


### NCS Legend
- NCS 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 범례 명                                         | 설명                                 |
|----------------------------------------------|------------------------------------|
| label_ncs_container_nhncloud_com_workload_id | nhncloud NCS 서비스 내에서 사용중인 워크로드의 이름 |
| workload_id                                  | nhncloud NCS 서비스 내에서 사용중인 워크로드의 이름 |
| type                                         | 스토리지 종류                            |
| container                                    | 컨테이너의 이름                           |

## GPU
- NHN Cloud에서 제공하는 GPU 서비스의 지표에 대한 지표사전입니다.

### Metric List
| 한국어         | 리소스명 | 기본 범례(Legend) | 단위(Unit)   |
|-------------|------|---------------|------------|
| GPU 사용률     | GPU  | 없음            | 백분율(0-100) |
| GPU 온도      | GPU  | 없음            | 섭씨(℃)      |
| GPU 메모리 사용률 | GPU  | 없음            | 백분율(0-100) |
| GPU 전력 사용량  | GPU  | 없음            | 와트(W)      |

### GPU 필터(Filter)
- GPU 지표에 대해 필터를 적용할 수 있습니다.
- 필터를 적용하면 해당 필터에 맞는 지표만 표시됩니다.

| 필터 명    | 설명                |
|---------|-------------------|
| 인스턴스    | GPU 인스턴스의 이름      |

### GPU 범례(Legend)
- GPU 지표에 대해 범례를 적용할 수 있습니다.
- 범례를 적용하면 해당 지표가 범례 형식으로 적용됩니다.

| 필터 명                 | 설명           |
|----------------------|--------------|
| nhncloud_instance_id | GPU 인스턴스의 이름 |

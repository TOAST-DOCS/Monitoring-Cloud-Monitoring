## Monitoring > Cloud Monitoring > Metric Dictionary

## Metric Dictionary
- 지표사전(Metric Dictionary) 에서는 NHN Cloud에서 제공하는 지표에 대한 설명을 제공합니다.

## Instance
- NHN Cloud에서 제공하는 인스턴스 서버 지표에 대한 지표사전입니다.

### Metric List
| 한국어              | 리소스명    | 기본 범례(Legend)                                                              | 단위(Unit)         |
|------------------|---------|----------------------------------------------------------------------------|------------------|
| CPU 사용률  CPU     | CPU     |                                                                            | 백분율(0-100)       |
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

## GPU
- NHN Cloud에서 제공하는 GPU 서비스의 지표에 대한 지표사전입니다.

### Metric List
| 한국어         | 리소스명 | 기본 범례(Legend) | 단위(Unit)   |
|-------------|------|---------------|------------|
| GPU 사용률     | GPU  | 없음            | 백분율(0-100) |
| GPU 온도      | GPU  | 없음            | 섭씨(℃)      |
| GPU 메모리 사용률 | GPU  | 없음            | 백분율(0-100) |
| GPU 전력 사용량  | GPU  | 없음            | 와트(W)      |
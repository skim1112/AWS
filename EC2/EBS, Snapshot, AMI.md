## Snapshot

EBS를 저장하는 효율적인 방법

특정 시간에 EBS 상태를 저장 -> EBS 사진 찍어놓은 느낌

내가 원하는 시간대에 EBS를 복구 가능

Stored in S3
- 증분식 저장

### 증분식 저장
- 파일에 update가 일어날 때마다 **마지막에 발생했던 액션에 대해서만 저장**
	- 변화한 부분만 저장
- 추척에 용의


## AMI
**개요**
- EC2 인스턴스를 실행하기 위해 필요한 정보를 모은 단위
	- OS, 아키텍쳐 타입(32bit or 64bit), 저장공간 용량 etc
- AMI를 사용하여 EC2를 복제하거나 다리 region -> account로 transfer 가능
- **Snapshot**를 기반으로 AMI 구성 가능

**구성**
- 1개 **이상**의 EBS 스냅샷
- Instance Storage 인스턴스 경우, root volume에 대한 템플릿(OS, Application server, Application etc)
- 사용 권한(어떤 AWS account가 사용할 수 있는 지)
- 블록 디바이스 맵핑(EC2 instance를 위한 볼륨 정보 -> EBS가 무슨 용량으로 몇개 붙는지)

총 두개의 타입
- EBS기반 
- Instance Storage 기반

타입에 따른 AMI의 생성방법
- EBS: Snapshot를 기반으로 Root Device 생성
- Instance Storage: S3에 저장된 template기반으로 생성
